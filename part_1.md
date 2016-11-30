
## Cost Estimation

# Part 1 (2 pts each)

Assume a table Emp(**ssn**, name, salary) of employee records, where `ssn` is the primary key.  Assume the following characteristics:

* 100,000 records
* Page size = 1000 bytes
* tuple size = 50 bytes
* directory entry size = 10 bytes
* No other overhead when storing data on pages.
* You can assume that there are no overflow pages in the hash index
* The queries always return a result

Clarification

* assume that each page accessed is from disk (memory only has space for one page)

## Select Queries

Suppose we run `select name from Emp where ssn=1000`.

**(a)**  If there are no indices, how many page accesses does this query cost on average?

**(b)** Assume a primary B+-tree index on `emp(ssn)`, and fill factor of 1. How many page accesses will the query cost?

It will be helpful to compute (you only need to submit the final cost)

* Number of leaf pages
* Fan out 
* Height of the tree

**(c)** Assume only a secondary B+-tree on `emp(ssn)`, and fill factor of 1. How many page accesses will the query cost?

It will be helpful to compute (you only need to submit the final cost)

* Number of leaf pages
* Fan out 
* Height of the tree

**(d)** What are the costs for (b) and (c) if the fill factor is 50%?

**(e)** Assume only a secondary hash index on `Hash(emp.ssn)`. How mayn page accesses will the query cost?

## Aggregation Queries

Suppose we run `select max(salary) from Emp`

**(f)** Assuming no indices, how many disk accesses to run this query?

**(g)** How many disk accesses if there is a secondary B+ tree index on `emp(salary)`?

**(h)** How many disk accesses if there is a secondary hash index on `emp(salary)`?


# Submission for Cost estimation

**Please submit this section of HW4 through the following Google form**

https://goo.gl/forms/B1JSTVzI4K3NRxVz2
