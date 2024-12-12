# DSC_E3.7


Consider the SQL query

select distinct p.a1
from p, r1, r2
where p.a1 = r1.a1 or p.a1 = r2.a1

Under what conditions does the preceding query select values of p.a1 that are either in r1 or in r2? Examine carefully the cases where one of r1 or r2 may be empty.


If r1 and r2 are both non-empty:
The query will return all distinct values of p.a1 that match r1.a1 or r2.a1.
If r1 is empty and r2 is non-empty:
The query will return all distinct values of p.a1 that match r2.a1.
If r2 is empty and r1 is non-empty:
The query will return all distinct values of p.a1 that match r1.a1.
If both r1 and r2 are empty:
The query will return an empty result set since there are no values in r1.a1 or r2.a1 to match p.a1.