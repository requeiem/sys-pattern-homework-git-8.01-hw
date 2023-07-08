# Домашнее задание к занятию «Индексы»  "`«Индексы»`" - `Чесноков Александр`

---

### Доработка домашнего задания

```CREATE INDEX pay_date ON payment(payment_date);
```

```select * from information_schema.statistics where table_name = 'payment';
```
```
EXPLAIN ANALYZE
select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id)
from payment p, customer c
WHERE payment_date >= '2005-07-30' and payment_date <DATE_ADD('2005-07-30', INTERVAL 1 DAY) and p.customer_id = c.customer_id;
```

-> Limit: 200 row(s)  (cost=0..0 rows=0) (actual time=4.01..4.05 rows=200 loops=1)
    -> Table scan on <temporary>  (cost=2.5..2.5 rows=0) (actual time=4.01..4.04 rows=200 loops=1)
        -> Temporary table with deduplication  (cost=0..0 rows=0) (actual time=4.01..4.01 rows=391 loops=1)
            -> Window aggregate with buffering: sum(payment.amount) OVER (PARTITION BY c.customer_id )   (actual time=2.64..3.77 rows=634 loops=1)
                -> Sort: c.customer_id  (actual time=2.61..2.67 rows=634 loops=1)
                    -> Stream results  (cost=507 rows=634) (actual time=0.047..2.43 rows=634 loops=1)
                        -> Nested loop inner join  (cost=507 rows=634) (actual time=0.0429..2.2 rows=634 loops=1)
                            -> Index range scan on p using pay_date over ('2005-07-30 00:00:00' <= payment_date < '2005-07-31 00:00:00'), with index condition: ((p.payment_date >= TIMESTAMP'2005-07-30 00:00:00') and (p.payment_date < <cache>(('2005-07-30' + interval 1 day))))  (cost=286 rows=634) (actual time=0.0334..1.27 rows=634 loops=1)
                            -> Single-row index lookup on c using PRIMARY (customer_id=p.customer_id)  (cost=0.25 rows=1) (actual time=0.00127..0.0013 rows=1 loops=634)


![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/index1.jpg)
![alt text](https://github.com/requeiem/sys-pattern-homework-git-8.03-hw/blob/main/img/index2.jpg)




