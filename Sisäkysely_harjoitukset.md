1.
select country.name
    -> from airport
    -> join country on airport.iso_country = country.iso_country
    -> where airport.name like "satsuma%";
  ![image](https://github.com/user-attachments/assets/6f2801c2-6f8c-47f4-931c-35b4ea95cf19)

2.
select airport.name
    -> from country
    -> join airport on country.iso_country = airport.iso_country
    -> where country.name like "monaco";
  ![image](https://github.com/user-attachments/assets/aa691746-6309-430f-bb13-d1ea29056126)

3.
select game.screen_name
    -> from goal
    -> join goal_reached on goal.id = goal_reached.goal_id
    -> join game on goal_reached.game_id = game.id
    -> where goal.name like "clouds";
![image](https://github.com/user-attachments/assets/df7a904f-d35c-408d-b9b3-63efda3013b0)

4.
select country.name
    -> from country
    -> where country.iso_country not in (
    -> select airport.iso_country
    -> from airport
    -> );
 ![image](https://github.com/user-attachments/assets/2805c404-5fcc-4903-813b-cc8298e4f438)

5.
select goal.name
    -> from goal
    -> where goal.id not in (
    -> select goal_reached.goal_id
    -> from goal_reached
    -> where goal_reached.game_id = "1"
    -> );
![image](https://github.com/user-attachments/assets/1b43515b-dba8-4140-bf22-3e552b378bf3)


