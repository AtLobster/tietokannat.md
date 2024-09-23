
1.
select *
    -> from goal;
![image](https://github.com/user-attachments/assets/0f619dc2-40c6-4147-8142-b79519d46522)

2.
select name, type
from airport
where iso_country = "FI"; 
![image](https://github.com/user-attachments/assets/3dba3e2c-f94f-4aac-b60b-ccedf0fb266a)

3.
select name
    -> from airport
    -> where iso_country = 'FI'
    -> order by name asc;
![image](https://github.com/user-attachments/assets/7f2e415c-1a18-4248-ab05-48fe1459abfe)

4.
  select name, type
    -> from airport
    -> where iso_country = 'FI'
    -> order by type asc, name asc;
  ![image](https://github.com/user-attachments/assets/727fd328-0525-436a-a720-09e65a0c8b6a)

5.
select name from country where name like 'F%';
![image](https://github.com/user-attachments/assets/d96c7178-0d66-4177-ac82-a332779ae224)

6.
select name from country where name like '%F%';
![image](https://github.com/user-attachments/assets/8a0cf0cf-f267-4916-90d2-ebfa182c1e1b)

7.
select location from game where location = "EGCC";
![image](https://github.com/user-attachments/assets/43137c67-db0f-4f0e-80fa-2a8ac71c528a)

8.

