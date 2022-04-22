# Sql-Practice-02

create database chetu 
use chetu

create table employee(emp_ID int primary key identity not null, emp_Name varchar(20) ,
emp_Salary money ,emp_Dept varchar(20),emp_Gender varchar(20) )



insert into employee values
('Rohan',20000,'IT','Male'),
('Mohan',25000,'HR','Male'),
('Shweta',30000,'IT','Female'),
('Sita',35000,'CS','Female'),
('Gita',40000,'IT','Female'),
('Jack',45000,'HR','Male')


select *  into emp1 from employee 



select * from employee where emp_salary between 20000 and 40000

create table department (dept_ID int primary key identity not null,dept_Name varchar(20),dept_No int )

insert into department values
('IT',2),
('HR',1),
('CS',4),
('IT',3),
('HR',6),
('IT',5)

select * from employee
union 
select * from emp1

select emp_Name,dept_No , emp_salary from employee group  by dept_No,emp_Name ,emp_salary order by emp_salary desc



select * from employee
except
select * from emp1

select * from employee
union
select * from emp1



select * from dept
select * from employee
select * from emp1


insert  employee values ('deepak',10000,'mc','male',8)


select dept_No,sum(emp_salary) as totalsal from employee group by dept_No having sum(emp_id)>=2

select count(emp_salary) totalemp from employee

select min(emp_salary) totalsal from employee

select max(emp_salary) totalsal from employee

select sum(emp_salary) totalsal from employee

select avg(emp_salary) totalsal from employee
