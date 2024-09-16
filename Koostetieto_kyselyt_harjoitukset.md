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

