When using LEAD and date make sure to use dateadd instead of just values

This works with datetime but not with date data types
```SQL
LEAD(SomeDate-1,1,'99991231')
```

This is the error you get with a date data type
```
Msg 206, Level 16, State 2, Line 2
Operand type clash: date is incompatible with int
```


This works with both date and datetime data types
```SQL
LEAD(dateadd(dd,-1,SomeDate),1,'99991231') 
```
