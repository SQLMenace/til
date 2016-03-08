This statement enables the configuration of a number of database configuration settings at the individual database level, independent of these settings for any other database. This statement is available in both SQL Database V12 and in SQL Server 2016 Release Candidate (RC0). These options are:
Clear procedure cache.
Set the MAXDOP parameter to an arbitrary value (1,2, ...) for the primary database based on what works best for that particular database and set a different value (e.g. 0) for all secondary database used (e.g. for reporting queries).
Set the query optimizer cardinality estimation model independent of the database to compatibility level.
Enable or disable parameter sniffing at the database level.
Enable or disable query optimization hotfixes at the database level.

Syntax
```SQL
ALTER DATABASE SCOPED CONFIGURATION
{      
     {  [ FOR SECONDARY] SET <set_options>  }  
}
| CLEAR PROCEDURE_CACHE
[;]  

< set_options > ::=  
{
    MAXDOP = { <value> | PRIMARY}  
    | LEGACY_CARDINALITY_ESTIMATION = { ON | OFF | PRIMARY}  
    | PARAMETER_SNIFFING = { ON | OFF | PRIMARY}  
    | QUERY_OPTIMIZER_HOTFIXES = { ON | OFF | PRIMARY}  
}
```


Examples

```SQL
ALTER DATABASE SCOPED CONFIGURATION SET PARAMETER_SNIFFING =OFF ;
ALTER DATABASE SCOPED CONFIGURATION CLEAR PROCEDURE_CACHE ;
ALTER DATABASE SCOPED CONFIGURATION SET QUERY_OPTIMIZER_HOTFIXES=ON ;

```
