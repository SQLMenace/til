This is new in SQL Server 2016 from RC0 on....

```SQL
SELECT * FROM STRING_SPLIT('Hi how are you doing?',')
```
The result is:

```
value
—–
Hi
how
are
you
doing?
```
