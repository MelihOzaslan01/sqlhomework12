- SELECT COUNT(*) FROM Film WHERE length >
 (SELECT AVG(length) FROM Film)


- SELECT COUNT(*) FROM Film WHERE rental_rate = 
any (SELECT max(rental_rate) FROM Film);



- SELECT COUNT(*) FROM Film WHERE rental_rate = 
all (SELECT min(rental_rate) FROM Film) and replacement_cost =
 any (SELECT min(replacement_cost) FROM Film)



- SELECT customer_id, count(payment_id)
FROM payment 
GROUP BY customer_id ORDER BY count(payment_id) DESC