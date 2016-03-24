This is some cool new stuff (already available in SQL Server 2014)

Basically if you have a TVP like this
```SQL
CREATE TYPE dbo.test_disk AS TABLE
(c1 INT NOT NULL,
 c2 CHAR(10));
 ```
 
 
 you can memory optimize this type
 
 ```SQL
 CREATE TYPE dbo.test_memory AS TABLE
(c1 INT NOT NULL INDEX ix_c1,
 c2 CHAR(10))
WITH (MEMORY_OPTIMIZED=ON);
```


All the details are here [Improving temp table and table variable performance using memory optimization](https://blogs.msdn.microsoft.com/sqlserverstorageengine/2016/03/21/improving-temp-table-and-table-variable-performance-using-memory-optimization/)

A must read is also [Microsoft Fixed My Biggest SQL Server Pet Peeve (Two Years Ago)](http://michaeljswart.com/2016/03/microsoft-fixed-my-biggest-sql-server-pet-peeve-two-years-ago/)
