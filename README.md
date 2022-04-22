# Sql-Practice---3

create database employee
use employee

create table employee(emp_ID int primary key identity,emp_Name varchar(20),
emp_salary money, emp_Dept varchar(20),emp_Gender varchar(20),dept_no int)



insert into employee values
('virat',20000,'IT','Male',2),
('rohit',25000,'HR','Male',1),
('rovin',30000,'CS','Male',4),
('riya',35000,'TL','Female',3),
('siya',40000,'IT','Female',6),
('ritika',45000,'HR','Female',5),
('surayansh',50000,'IT','Male',7)


alter table emp add emp_Job varchar(20)
update employee set emp_Job='Clerk' where emp_ID=2
update employee set emp_Job='Salesman' where emp_ID=3
update employee set emp_Job='Driver' where emp_ID=4
update employee set emp_Job='CA' where emp_ID=5
update employee set emp_Job='TL' where emp_ID=6
update employee set emp_Job='FM' where emp_ID=7


select emp_name ,emp_salary/12  Monthly_salary from employee

select * from employee where dept_no=4 or dept_no=7

select * from employee where dept_no=5 and emp_salary>40000

select * from employee where emp_Job not in ('Salesman','Clerk')

select * from employee where emp_Name in ('virat','suryansh','ritika','riya')

select * from employee where emp_name like 'r%' and emp_name like '_________'

select * from employee where emp_Name like '%a' 

select count(emp_salary/12) monthly_salry,COUNT(emp_salary) 
annual_salary from employee

select emp_salary as total_salary from employee

select * from  employee where  emp_salary = any
(select emp_salary from employee where emp_salary<45000)

select emp_Name,emp_salary from employee where emp_salary<45000

select * from employee

