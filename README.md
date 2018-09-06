# session-26-Assignment-26_2--Assignment2
DATA ANALYTICS WITH R, EXCEL AND TABLEAU SESSION 26 ASSIGNMENT 2


                                                Session 10 – RDBMS continued
                                                          Assignment 2
                                                          Assignment 26_2
5. Problem Statement 4. Return the first name, last name and city of all customers who live in Canada. Order the results first by the last then by the first name.  
5. How many customers are from Brazil??  
6. Return the "popular countries"? (that is, the ones with more than 20 customer). For each such country, return its name and its correspond number of customers. Order the result by the number of customers (descending).


Answer:-
26.1.4
Question: Return the first name, last name and city of all customers who live in Canada. Order the re-sults first by the last then by the first name.

Select first_name,last_name,city,country from customer,customer_list where customer.customer_id=customer_list.ID and country='Canada';
====================
26.1.5
Question: How many customers are from Brazil??

Select count(*) from customer_list where country='Brazil';
=======================
26.1.6
Question: Return the "popular countries"? (that is, the ones with more than 20 customer). For each such country, return its name and its correspond number of customers. Order the result by the number of customers (descending).
Select country,count(country) as “cnt” from customer_list group by country having count(country)>20 order by cnt desc;



