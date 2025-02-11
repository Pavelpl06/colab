# User case
***Диаграмма вариантов использования для приложения по съёму жилья***

![Снимок экрана 2024-12-18 105018](https://github.com/user-attachments/assets/f6f17ee7-e0af-4537-9662-cacb27c643d2)


## Final work


***Программное обеспечение для автомата, печатающего фото из Instagram.***

Требования для автомата печатающего фото из instagram

Глоссарий

Требования функционального характера
+ БТ- бизнес требование
+ ПТ- пользовательские требования
+ ФТ- функциональные требования

Требования нефункционального характера
О- ограничения

Требования функционального характера

- БТ001 Необходимо разработать программное обеспечение для автомата печатающего фото из instagram,в котором пользователь сможет распечатывать фотографии с мобильного телефона и с аккаунта в instagram
- ПТ001 Пользователь должен иметь возможность просматривать фотографии с аккаунта instagram 
- ПТ002 Пользователь должен иметь возможность просматривать фотографии с мобильного телефона
- ПТ003 Пользователь должен иметь возможность распечатать выбранные фотографии 
- ФТ001 Система должна предоставить возможность ввести свой логин  аккаунта instagram
- ФТ002 Система должна предоставить возможность соединить телефон  через кабель зарядки
- ФТ003 Система должна предоставить  два способа “Выбрать фото для печати” - выбрать фото в instagram или загрузить фото с телефона

Требования нефункционального характера

О001 Пользователь не должен иметь возможность распечатать более 100 фотографий




***Диаграмма вариантов использования для “Автомата печатающего фото из instagram”***



![Снимок экрана 2024-11-12 134608](https://github.com/user-attachments/assets/3bee6786-05c6-4d62-b5cc-79f07463ce33)



***Описание варианта использования “печатать фотографии”***

ВИ-1. Печатать фотографии

Краткое описание:Потенциальный клиент воспользовался автоматом для печати фотографий из instagram  

Действующие лица:Клиент

Предусловие:
- У клиента есть своя страница в instagram
- У клиента есть с собой зарядное устройство и мобильный телефон

Основной поток

* Клиент выбирает печать фотографии на сенсорной панели экрана автомата
* Система предлагает на выбор два варианта-  выбрать фото в Instagram или загрузить фото с телефона.
* Клиент входит в аккаунта instagram,либо присоединяет мобильный телефон к автомату через кабель зарядки  
* Если профиль пользователя открыт , то управление переходит на следующий шаг
* Пользователь выбирает фотографии из аккаунта instagram,либо с телефона
* Система позволяет выбрать не более ста фотографий
* Клиент выбирает “распечатать фотографии”
* Система распечатывает фотографии
* Вариант использования завершает свою работу

Альтернативный поток:

4а. Если профиль пользователя закрыт
- Система отображает уведомление  о закрытом профиле
- Управление переходит на шаг 2

Постусловие:
В случае успешного выполнения основного потока клиент распечатывает фотографии
Результат:
В случае успешного ВИ выбранные фотографии распечатаны.

### ***Диаграмма последовательности***

 ![Снимок экрана 2024-11-07 215121](https://github.com/user-attachments/assets/972fc04b-25b8-4684-b2c6-d46af43bd022)
 

#### ***Итоговая работа по SQL***

--1. Выведите название самолетов, которые имеют менее 50 посадочных мест?

select  a.model, count(s.seat_no)
from aircrafts a 
left join seats s on s.aircraft_code = a.aircraft_code 
group by 1
having count(s.seat_no) < 50;

--2. Выведите процентное изменение ежемесячной суммы бронирования билетов, округленной до сотых.

select t.date_trunc,t.sum,   
    round(((t.sum - lag(t.sum, 1,0.) over (order by t.date_trunc))/ 
       lag(t.sum, 1) over (order by t.date_trunc))*100, 2) as "процентное изменение"
from (
	select date_trunc('month', b.book_date)::date, sum(b.total_amount)   
	from bookings b
	group by date_trunc('month', b.book_date)
	order by date_trunc('month', b.book_date)
	) t


--3. Выведите названия самолетов не имеющих бизнес - класс. Решение должно быть через функцию array_agg.
	
	select a.model 
    from (
			select s.aircraft_code, array_agg(fare_conditions) 
			from seats s 
			group by s.aircraft_code
			having array_position (array_agg (fare_conditions),'Business')is null
			) f
left join aircrafts a on a.aircraft_code = f.aircraft_code

-- 4. Вывести накопительный итог количества мест в самолетах по каждому аэропорту на каждый день,
-- учитывая только те самолеты, которые летали пустыми и только те дни, где из одного аэропорта таких самолетов вылетало более одного.
--В результате должны быть код аэропорта, дата, количество пустых мест в самолете и накопительный итог.

select t.departure_airport, t.actual_departure,t. count, t.sum
from (
   select ft.actual_departure, ft.departure_airport,ft.aircraft_code, s.count,
       count(ft.aircraft_code) over (partition by ft.actual_departure, ft.departure_airport) count_dep,
       sum(s.count) over (partition by ft.actual_departure, ft.departure_airport rows between unbounded preceding and current row)
   from (
      select date_trunc('day', f.actual_departure)::date as actual_departure,
      f.departure_airport,f.aircraft_code
      from flights f 
      left join boarding_passes bp on bp.flight_id = f.flight_id
      where bp.boarding_no is null and (f.status = 'Departed' or f. status = 'Arrived')
      group by 1,2,3
      )ft
    left join (
              select aircraft_code, count(seat_no)
              from seats s
              group by 1 )s
              on s.aircraft_code = ft.aircraft_code
    order by 1,2) t 
where count_dep > 1    
              
              
--5. Найдите процентное соотношение перелетов по маршрутам от общего количества перелетов.
-- Выведите в результат названия аэропортов и процентное отношение.
-- Решение должно быть через оконную функцию.

select a.airport_name, round((sum (fa.count)/
sum(sum (fa.count) ) over() )* 100.,2)  as "процент перелётов"
from (
      select f.departure_airport, concat(f.departure_airport,' ',f.arrival_airport), count(f.flight_id)
      from flights f 
      where f.status = 'Arrived'
      group by f.departure_airport, f.arrival_airport 
      )fa
      left join airports a on airport_code = fa.departure_airport
      group by a.airport_code 
      order by a.airport_name
      
--6. Выведите количество пассажиров по каждому коду сотового оператора, если учесть, что код оператора - это три символа после +7
      
select substring(contact_data ->> 'phone' from 3 for 3) as "код"  , count(passenger_id) as "кол.пас."
from tickets 
group by "код" 
order by "код"   

--7. Классифицируйте финансовые обороты (сумма стоимости перелетов) по маршрутам:
 --До 50 млн - low
 -- 50 млн включительно до 150 млн - middle
 --От 150 млн включительно - high
 --Выведите в результат количество маршрутов в каждом полученном классе


select j."class", count(*) as "кол.маршрутов"
from (
     select   case
			when sum(tf.sum) < 50000000 then 'low'
			when sum(tf.sum) < 150000000 then 'middle'
			when sum(tf.sum) >= 150000000 then 'high'
			else 'passenger-free'
            end "class"
	 from flights f   
 left join (
	     select flight_id, sum(amount)
	     from ticket_flights 
	     group by 1 ) tf
    on f.flight_id = tf.flight_id
    where f.status != 'Cancelled'
    group by f.departure_airport, f.arrival_airport) j 
group by j."class"    
order by count(*)    
 
   
--8. Вычислите медиану стоимости перелетов, медиану размера бронирования и отношение медианы бронирования к медиане стоимости перелетов, округленной до сотых
			
 select distinct percentile_cont(0.5) within group (order by tf.amount) as median_ticket,
                 percentile_cont(0.5) within group (order by b.total_amount) as median_booking,
                 round(((percentile_cont(0.5)within group (order by b.total_amount))/
                 (percentile_cont(0.5)within group (order by tf.amount))):: numeric, 2) 
from tickets t 
left join ticket_flights tf on tf.ticket_no = t.ticket_no 
left join bookings b on b.book_ref = t.book_ref 


--9. Найдите значение минимальной стоимости полета 1 км для пассажиров. То есть нужно найти расстояние между аэропортами и с учетом стоимости перелетов получить искомый результат

select round(min(a_cost.min_amount / a_dist.distance)::numeric, 2) as "min cost per km flown"
from (
    select f.flight_id, tf.min_amount,concat(f.departure_airport,' ',f.arrival_airport) as "route"
    from flights f 
    inner join (
          select flight_id, min(amount) as min_amount
          from ticket_flights 
          group by 1)tf
    on tf.flight_id = f.flight_id      
)a_cost
left join (
     select r.dep_a, r.arr_a, r.route,earth_distance(ll_to_earth(a.latitude, a.longitude),
            ll_to_earth(b.latitude, b.longitude) ) / 1000 as distance  
     from (
          select  f.departure_airport as dep_a, f.arrival_airport as arr_a,
          concat(f.departure_airport,' ',f.arrival_airport) as "route"
          from flights f
          group by 1,2) r
      left join airports a on r.dep_a = a.airport_code 
      left join airports b on r.arr_a = b.airport_code 
  )a_dist
  on a_cost.route = a_dist.route
  group by a_dist.route
  order by "min cost per km flown"
  limit 1

