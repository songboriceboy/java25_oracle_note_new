### where语句

#### between xxx and yyy

```sql
    select * from emp where sal BETWEEN 1000 and 2000
```

#### in(a,b,c)
```sql
    select * from emp where deptno in (20,30)
```

#### like '%A%'  '%B_'

```sql
    select * from emp where ename like '%A%'
```

#### is null
```sql
  select * from emp where comm is null 
```
### 逻辑运算符

- AND
- OR
- NOT

#### AND
```sql
    select * from emp where sal > 2000 and job = 'CLERK'
```

#### OR
```sql
  select * from emp where sal > 2000 or job = 'CLERK'
```
#### not
not 关键字可以接哪些关键字
- not in
- not like
- not between xxx and yyy
- is not null

### orderby 用来对查询结果排序
- asc 升序， 默认
- desc 降序

### 多列参与排序

```sql
select * from emp order by deptno, sal desc
```

## 多表连接

### 笛卡尔积

 2个表t1,t2的笛卡尔积是t1中的每条记录与t2中的每条记录进行组合，形成的结果集
 
 假设t1中n条记录，t2中有m条记录  
 结果集中记录的个数为n*m  
 
 如何消除笛卡尔积？  
 
 连接2个表时不要忘了加上连接条件，n个表连接，需要至少n-1个连接条件  
 
 ```sql
select emp.ename,dept.dname from emp,dept
where emp.deptno = dept.deptno
```
 
 
 
 
