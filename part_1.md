
## Cost Estimation

# Part 1 (1 pt each)

**Q1.1** Assume a table Emp(ssn, name, salary) of employee records, where ssn is the primary key. The total size of the table is 34,560MB. The table (i.e., the records of the table) is stored in a heap file in chunks of 2KB pages (all full of records) on a single disk drive. In all questions below that involve indices, assume that the number of leaf pages for B+-trees and the number of buckets for hash indices are the same with the number of pages required to store the table in the heap.

**Q1.2** We are about to run a query on this Emp table to find the name of the employee with a given ssn, say 1000; i.e., in SQL, "select name from Emp where ssn=1000". In a worst-case scenario, how long this operation will take? Express your answer in both, number of disk accesses (I/O) and in hours.  The disk drive has the following characteristics: average seek time is 8 msecs, average rotational delay is 1 msec, and average transfer rate is 1 msec per 2KB block so, the total time to locate and transfer a disk block of data is 10 msecs.

**Q1.3** Assume that in addition to storing the table as described above, we also have available a B+-tree built for this table on ssn - this is the search key of the B+-tree. A data entry in the tree is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the B+-tree index? 

**Q1.4** Now assume that we have a hash index on ssn for the Emp table. A data entry in the hash is a pair (ssn, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (a) if we use the hash index? 

**Q1.5** Now, consider this query: find the maximum salary in the Emp table; i.e., in SQL, "select max(salary) from Emp". Assuming no indexing of any kind, i.e., we just have the records of the table in the heap, what is the cost of this query (in number of disk accesses)?

**Q1.6** Assume we have available a B+-tree on Emp.salary. A data entry in the tree is a pair (salary, RID of a data record in the heap). What is the approximate cost (in number of disk accesses) of executing the query in (d) if we use this B+-tree index?

**Q1.7** Assume we have available a hash index on Emp.salary. A data entry in the hash index is a pair (salary, RID of a data record in the heap). Is the hash index useful to compute the query? If no, explain. If yes, i.e., you think it is better to use the hash index instead of the heap, explain how you do this search and what is the approximate cost (in number of disk accesses) of executing the query if we use the hash index? 

**Q1.8** Now, consider this update: insert a new employee record (1000, "mike", 100). Assuming no indexing of any kind, i.e., we just have the records of the table in the heap, what is the approximate cost of this operation (in number of disk accesses)?

**Q1.9** For the operation in (g), and assuming there is a B+-tree as described in (e), what is the approximate cost (in number of disk accesses) of executing the operation if we use the B+-tree?

**Q1.10** For the query in (g), and assuming there is a hash index as described in (f), what is the approximate cost (in number of disk accesses) of executing the operation if we use the hash index?  


Note
Assume the cost of everything else besides disk accesses is negligible.
For question (a), to simplify calculations, assume 1 MB = 1,000 KB.
Your answers in cost related questions must be plain numbers (e.g., 5, 90, 90.56) that include no formulas and/or computation of any kind. For example, the following types of answers will automatically get zero with no further consideration:  log base 2 of some N; cube of N square divided by log base 2 of N cube multiplied by log base 10 N; big O(log(N)); etc. However, you must explain how you  came up with your final (number) answer by indicating the steps.

# Submission for Cost estimation

**Please submit this section of HW4 through the following Google form**

https://goo.gl/forms/B1JSTVzI4K3NRxVz2