  **1-Window Functions vs GROUP BY:**
   GROUP BY reduce number of rows as it take some rows and the result is only one row
 Window function :doesn't reduce number of rows  but also it put the result of
  aggregation to each row
  ***
  
 **2-Clustered vs Non-Clustered Indexes:**
   Clustered :order thw data and it's allowed to have one clustered ondex per table becuase data  can't be order twice or more
   Non-Clustered:saves data in without order
   ***
   **3-Filtered & Unique Indexes:**
     -Filtered Index:it mangae dealing with only subset of a table instead of crossing all the table and it makes search fast and decrease usage of memory
    -Unique Index:it physically slow down INSERT statements becaise it must check all the indices as it must be distinct
     while while speeding up SELECT statements becuase every thing has a unique index and it doesn't have to cross all the table to search the value.
***
**Choosing the Right Index:**
using non-clustered index is the best because ordered data is not very important in this case and non-clustered is faster than clustered
***
**Database Transactions (ACID):**
means that data is like one unit at any time operation failed any changes before it ignored (that's before commit)