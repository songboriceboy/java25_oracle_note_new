### 左外连接

#### 提出问题

> 找出所有的员工姓名和部门名称，``没有员工的部门也要查出来``

```sql
select emp.ename,dept.dname,emp.sal ,dept.DEPTNO
from dept left join emp on dept.deptno = emp.deptno
```
左外连接，以左边的表为主（左边的表里的所有行，不管是否满足连接条件，都必须出现在最终的结果集中）  
left join  
右外连接同理  
right join  
全外连接 = 左外连接 + 右外连接
full join
[百度](http://www.baidu.com)
![自连接示意图](https://github.com/songboriceboy/java25_oracle_note_new/raw/master/images/self_join.JPG)
### 自连接
#### 提出问题
> 查出所有员工的姓名及其直接经理姓名
```sql
select b.ename 员工姓名, a.ename 经理姓名
from emp a
join emp b on b.mgr = a.empno
```
- 自己和自己连接
- 进行连接的2个表是同一张表，但是,是2个表连接
-- ``a和b到底哪一个代表员工信息，哪一个代表经理，要看连接条件``

### 分组函数

- max（列名） 求所有记录中的最大值，列可以数字或日期或字符串类型
- min(列名) 求所有记录中的最小值，列可以数字或日期或字符串类型
- sum（列名） 求所有记录中该列累计和，列只可以数字
- avg（列名）求所有记录中该列平均值，列只可以数字
- count（*）求记录数