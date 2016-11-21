
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

**(a)** We are about to run a query on this Emp table to find the name of the employee with a given ssn, say 1000; i.e., in SQL, "select name from Emp where ssn=1000". What is the cost of this operation in terms of disk accessess assuming no indices.

**(b)** Assume a primary B+-tree index on `emp(ssn)`. Calculate the cost(in terms of disk access) given the tuple size of running the query discussed in (a)**

**(c)** Now assume we have a secondary B+-tree on `emp(ssn)`. A data entry in the tree is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the B+-tree index? 

**(d)** What would be the case if the fill factor reduced by 50%. Discuss the impact on (b) and (c)

**(e)** Now assume that we have a secondary hash index on `Hash(emp.ssn)` for the Emp table. A data entry in the hash is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the hash index? 

## Aggregation Queries **WE can remove this part below if the above seems like a reasonable exercise**

**(f)** Now, consider this query: find the maximum salary in the Emp table; i.e., in SQL, "select max(salary) from Emp". Assuming no indexing of any kind, i.e., we just have the records of the table in the heap, what is the cost of this query (in number of disk accesses)?

**(g)** Discuss impact on the query in (f) in terms of cost estimation if we use-
		**1. ** Secondary B+-tree index on `emp(ssn)`
		**2. ** Secondary hash index on `Hash(emp.ssn)` 


# Submission for Cost estimation

**Please submit this section of HW4 through the following Google form**

https://goo.gl/forms/B1JSTVzI4K3NRxVz2
