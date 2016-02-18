This is new in SQL Server 2016. 

To truncate 1  partitions in a partitioned table

```SQL
TRUNCATE TABLE PartitionTable1 
WITH (PARTITIONS (2));
GO
```

To truncate 3  partitions in a partitioned table

```SQL
TRUNCATE TABLE PartitionTable1 
WITH (PARTITIONS (2, 4, 6));
GO
```

To truncate a range of partitions in a partitioned table
```SQL
TRUNCATE TABLE PartitionTable1 
WITH (PARTITIONS (6 TO 8));
GO
```

You can combine a range with individual specified partitions as well
```SQL
TRUNCATE TABLE PartitionTable1 
WITH (PARTITIONS (6 TO 8));
GO
```
