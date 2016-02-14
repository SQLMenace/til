To load data from SQL Server into R, you first need to create an ODBC Data Source, I created one named LocalSqlServer, this DSN Data Source points to my local SQL Server 2016 instance.

After that you need to load the (RODBC)
 package, create a connection and execute a query, finally the head function is used to display the first 6 rows. Here is what it lokks like in R


```R
> require(RODBC)
Loading required package: RODBC
Warning message:
package ‘RODBC’ was built under R version 3.2.3 


>db <- odbcConnect("LocalSqlServer")

> Sample <- sqlQuery(db, "select * from sysobjects", stringsAsFactors=FALSE)

> head(Sample)
                        
      name          id xtype uid info status base_schema_ver
1      sp_MSalreadyhavegeneration -1073624922    P    4    0      0               0
2      sp_MSwritemergeperfcounter -1072815163    P    4    0      0               0
3       TABLE_PRIVILEGES -1072372588    V    3    0     	
4       sp_replsetsyncstatus -1071944761    X    4    0      0               0
5       sp_replshowcmds -1070913306    P    4    0      0               0
6       sp_publishdb -1070573756    P    4    0      0               0
```
