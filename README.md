# goit-rdb-hw-07
SELECT 
    id,
    DATE_FORMAT(date, '%Y') AS year,
    DATE_FORMAT(date, '%m') AS month,
    DATE_FORMAT(date, '%d') AS day,
    date
FROM 
    orders;
![p_1](https://github.com/NGanch/goit-rdb-hw-07/assets/86801593/b3780f12-85cb-4ffa-9e66-3adcd25a6b0f)

SELECT 
    id,
    date,
    DATE_ADD(date, INTERVAL 1 DAY) AS new_date
FROM 
    orders;
![p_2](https://github.com/NGanch/goit-rdb-hw-07/assets/86801593/0a8d8611-3994-44dc-aa3e-e5a46b4b91c3)

SELECT 
    id,
    date,
    UNIX_TIMESTAMP(date) AS seconds_from_epoch
FROM 
    orders;
![p_3](https://github.com/NGanch/goit-rdb-hw-07/assets/86801593/ac301282-35f4-4440-a648-b360ff08e29a)

SELECT 
    COUNT(*) AS rows_count
FROM 
    orders
WHERE 
    date BETWEEN '1996-07-10 00:00:00' AND '1996-10-08 00:00:00';
![p_4](https://github.com/NGanch/goit-rdb-hw-07/assets/86801593/71a65615-3297-4fbf-8d62-19d87883ff9c)

SELECT 
    id,
    date,
    JSON_OBJECT('id', id, 'date', date) AS json_object
FROM 
    orders;
![p_5](https://github.com/NGanch/goit-rdb-hw-07/assets/86801593/94c32816-7e9a-4309-a628-7f275e9f379d)
