
## Cost Estimation

# Part 1 (1 pt each)

**(a)** Assume a table Emp(ssn, name, salary) of employee records, where `ssn` is the primary key.  Assume the following characteristics:
  * Table size: ...The total size of the table is 34,560MB. 
  * The table (i.e., the records of the table) is stored in a heap file in chunks of 2KB pages 
  * tuple size
  * directory entry size
  * all data stored on disk.  Assume the cost to access any page is 10ms
  
  In all questions below that involve indices, assume that the number of leaf pages for B+-trees and ...overflow..

## Select 

**(b)** We are about to run a query on this Emp table to find the name of the employee with a given ssn, say 1000; i.e., in SQL, "select name from Emp where ssn=1000". In a worst-case scenario, how long this operation will take? Express your answer in both, number of disk accesses (I/O) and in hours.  The disk drive has the following characteristics: average seek time is 8 msecs, average rotational delay is 1 msec, and average transfer rate is 1 msec per 2KB block so, the total time to locate and transfer a disk block of data is 10 msecs.  **clarify whether or not heap pages are together on disk or if each page should be a 10ms**

**assume primary index on `emp(ssn)`.  calculate the cost**

**(c)** Assume that in addition to storing the table as described above, we also have available a secondary B+ tree built for this table on ssn - this is the search key of the B+-tree. A data entry in the tree is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the B+-tree index? 

**(d)** Now assume that we have a secondary hash index on `Hash(emp.ssn)` for the Emp table. A data entry in the hash is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the hash index? 

## Aggregation Queries

**(e)** Now, consider this query: find the maximum salary in the Emp table; i.e., in SQL, "select max(salary) from Emp". Assuming no indexing of any kind, i.e., we just have the records of the table in the heap, what is the cost of this query (in number of disk accesses)?

**(f)** Assume we have available a secondary B+-tree on Emp.salary.  What is the approximate cost (in number of disk accesses) of executing the query in (d) if we use this B+-tree index?

**(g)** Assume we have available a hash index on Emp.salary. A data entry in the hash index is a pair (salary, RID of a data record in the heap). Is the hash index useful to compute the query? If no, explain. If yes, i.e., you think it is better to use the hash index instead of the heap, explain how you do this search and what is the approximate cost (in number of disk accesses) of executing the query if we use the hash index? 


Note
Assume the cost of everything else besides disk accesses is negligible.
For question (a), to simplify calculations, assume 1 MB = 1,000 KB.
Your answers in cost related questions must be plain numbers (e.g., 5, 90, 90.56) that include no formulas and/or computation of any kind. For example, the following types of answers will automatically get zero with no further consideration:  log base 2 of some N; cube of N square divided by log base 2 of N cube multiplied by log base 10 N; big O(log(N)); etc. However, you must explain how you  came up with your final (number) answer by indicating the steps.

# Submission for Cost estimation

**Please submit this section of HW4 through the following Google form**

https://goo.gl/forms/B1JSTVzI4K3NRxVz2
