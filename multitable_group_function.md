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
