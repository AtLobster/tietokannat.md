1.
update game
    -> set location = "EGBN", co2_consumed = co2_consumed + 500
    -> where id = "2";

select id, co2_consumed, co2_budget, location, screen_name
    -> from game;
![image](https://github.com/user-attachments/assets/ca8f7f57-5338-453e-9507-cafc958645d4)
