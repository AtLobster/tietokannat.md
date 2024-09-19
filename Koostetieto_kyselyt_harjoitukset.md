1.
select max(airport.elevation_ft)
    -> from airport;
  ![image](https://github.com/user-attachments/assets/ce51e00c-6968-48e6-8962-c6b72041de0c)

2.
select country.continent, count(*)
    -> from country
    -> group by continent
    -> having count(*) >= 0;
![image](https://github.com/user-attachments/assets/0bf79d24-3f50-4ca1-bb86-33a0bfcd9b1f)


3.
select game.screen_name, count(goal_reached.goal_id)
    -> from game
    -> join goal_reached on game.id = goal_reached.game_id
    -> join goal on goal_reached.goal_id = goal.id
    -> group by game.screen_name;
![image](https://github.com/user-attachments/assets/4ba26b81-e4c6-4b03-868c-53c416842bfa)

4.
select game.screen_name
    -> from game
    -> where co2_consumed = (
    -> select min(co2_consumed)
    -> from game);
![image](https://github.com/user-attachments/assets/55ccea52-49c7-4e09-a71d-09d2d2650fe1)

5.
select country.name, count(*)
    -> from country
    -> join airport on country.iso_country = airport.iso_country
    -> group by country.name
    -> order by count(*) desc
    -> limit 50;
  ![image](https://github.com/user-attachments/assets/01a974da-4769-4859-90a1-4607fe57bbf4)

6.
select country.name
    -> from country
    -> join airport on country.iso_country = airport.iso_country
    -> group by country.iso_country
    -> having count(*) >= 1000;
![image](https://github.com/user-attachments/assets/ffd14d12-2d78-4f67-a422-b215b8eb18ac)

7.
select name
    -> from airport
    -> join (
    -> select max(elevation_ft) as max_elevation
    -> from airport )
    -> max_elev on airport.elevation_ft = max_elev.max_elevation;
![image](https://github.com/user-attachments/assets/22c7ea0f-4f5f-45bb-bdb4-6df01831386a)

8.
select country.name
    -> from country
    -> join airport on country.iso_country = airport.iso_Country
    -> join (
    -> select max(elevation_ft) as max_elevation
    -> from airport)
    -> max_elev on airport.elevation_ft = max_elev.max_elevation;
![image](https://github.com/user-attachments/assets/35de7af8-a4e9-4f21-8004-0fcc7ec400ac)

9.
select count(*)
    -> from goal_reached
    -> where game_id = "2";
![image](https://github.com/user-attachments/assets/edc27c01-d9ef-4f13-8165-28ff1fdfa5a0)


10.

  
