
## Cost Estimation

# Part 1 (2 pts each)

Assume a table Emp(**ssn**, name, salary) of employee records, where `ssn` is the primary key.  Assume the following characteristics:
  * 10,000 records
  * Page size = 1000 bytes
  * tuple size = 50 bytes
  * directory entry size = 10 bytes
  * All data stored on disk
  * You can assume that there are no overflow pages in the hash index
  * The query will always return a result

## Select Queries

Suppose we run `select name from Emp where ssn=1000`.

**(a)**  If there are no indices, how many page accesses does this query cost on average?

**(b)** Assume a primary B+-tree index on `emp(ssn)`, and fill factor of 1. How many page accesses will the query cost?

It will be helpful to compute

* Number of leaf pages
* Fan out 
* Height of the tree

**(c)** Assume only a secondary B+-tree on `emp(ssn)`, and fill factor of 1. How many page accesses will the query cost?

**(d)** What are the costs for (b) and (c) if the fill factor is 50%?

**(e)** Assume only a secondary hash index on `Hash(emp.ssn)`. How mayn page accesses will the query cost?

## Aggregation Queries **WE can remove this part below if the above seems like a reasonable exercise**

Suppose we run `select max(salary) from Emp`

**(f)** Assuming no indices, what is the cost of this query (in number of disk accesses)?

**(g)** How many disk accesses if there is a secondary B+ tree index on `emp(ssn)`?

**(h)** How many disk accesses if there is a secondary hash index on `emp(ssn)`?


# Submission for Cost estimation

**Please submit this section of HW4 through the following Google form**

https://goo.gl/forms/B1JSTVzI4K3NRxVz2
