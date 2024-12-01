# Data Lakehouse
Lakehouse is a portmanteau of lake and warehouse.  In this case, a data lake and a data warehouse.  Generically, a data lake is a term used to describe a large and relatively cheap storage container, which can be used to store any format of digital information.   

Data Lakes derive from the original and ground-breaking HDFS, that is the storage layer within the Hadoop ecosystem. Hadoop  was first released by Apache in 2006.   

For data processing, the importance of Hadoop was: 
1. The ability to bring the data into the same infrastructure as the compute resources (CPU and RAM), massively reducing I/O and netowrk latency.
2. Creating a file system with a block size an order of magnitude larger then that of the underlying operating systems, allowing higher throughput of sequential reads for larger files. 
3. Providing a mechanism for duplicating data blocks across hardware nodes where the Map/Reduce resource manager was able to read the same block in parallel, to further increase read performance.

One of the barriers to mass Hadoop adoption was the Map/Reduce programming paradigm, which is signigicantly different to either the set-theory approach of modern relational databases (select, group, order) or the row-based processing of application software.  As of 2024, it is more common to use an in-memory dataframe using vectorised operations to handle large data processing using either Spark (multi-node on Hadoop) or Pandas (single PC or Server). However, although these additional software layers are not as optimal as using native Map/Reduce, they have evolved to dominate data engineering tools.  

## (Big) Data Files
