# data-engineering-zoomcamp-workshop-1-Public
data-engineering-zoomcamp-workshop-1-Public

Question 1
# 2024-01-01 to 2024-02-01
sql
SELECT MIN(pickup_datetime) AS start_date,
       MAX(pickup_datetime) AS end_date
FROM trips;

Question 2
# 36.66%
sql
SELECT 
  COUNT(*) AS total_trips,
  SUM(CASE WHEN payment_type = 1 THEN 1 ELSE 0 END) AS credit_card_trips,
  1.0 * SUM(CASE WHEN payment_type = 1 THEN 1 ELSE 0 END) / COUNT(*) AS proportion_credit_card
FROM trips;

Question 3
# $8,063.41
sql 
SELECT SUM(tip_amount) AS total_tips
FROM trips;
