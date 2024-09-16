1.
select country.name "country name", airport.name "airport name"
    -> from airport
    -> join country on airport.iso_country = country.iso_country
    -> where scheduled_service = "yes" and country.name = "Finland";
+--------------+-----------------------------+
| country name | airport name                |
+--------------+-----------------------------+
| Finland      | Enontekio Airport           |
| Finland      | Helsinki Vantaa Airport     |
| Finland      | Ivalo Airport               |
| Finland      | Joensuu Airport             |
| Finland      | Jyväskylä Airport           |
| Finland      | Kemi-Tornio Airport         |
| Finland      | Kajaani Airport             |
| Finland      | Kokkola-Pietarsaari Airport |
| Finland      | Kuusamo Airport             |
| Finland      | Kittilä Airport             |
| Finland      | Kuopio Airport              |
| Finland      | Lappeenranta Airport        |
| Finland      | Mariehamn Airport           |
| Finland      | Oulu Airport                |
| Finland      | Pori Airport                |
| Finland      | Rovaniemi Airport           |
| Finland      | Savonlinna Airport          |
| Finland      | Seinäjoki Airport           |
| Finland      | Tampere-Pirkkala Airport    |
| Finland      | Turku Airport               |
| Finland      | Vaasa Airport               |
| Finland      | Varkaus Airport             |
+--------------+-----------------------------+
https://prnt.sc/AUzaB27uUaqg


2.
select game.screen_name, airport.name
    -> from game
    -> join airport on game.location = airport.ident
    -> ;
+-------------+-------------------------+
| screen_name | name                    |
+-------------+-------------------------+
| Heini       | Helsinki Vantaa Airport |
| Vesa        | Manchester Airport      |
| Ilkka       | London Gatwick Airport  |
+-------------+-------------------------+
https://prnt.sc/nqvyQRphERWh

3.
select game.screen_name, country.name
    -> from game
    -> join airport on game.location = airport.ident
    -> join country on airport.iso_country = country.iso_country;
+-------------+----------------+
| screen_name | name           |
+-------------+----------------+
| Heini       | Finland        |
| Vesa        | United Kingdom |
| Ilkka       | United Kingdom |
+-------------+----------------+
https://prnt.sc/Xb9qL-873yFL

4.
select airport.name, game.screen_name
    -> from airport
    -> left join game on game.location = airport.ident
    -> where airport.name like "%hels%";
+------------------------------------------+-------------+
| name                                     | screen_name |
+------------------------------------------+-------------+
| Winchelsea Airport                       | NULL        |
| Reichelsheim Airport                     | NULL        |
| Flugplatz Michelstadt/Odenwald           | NULL        |
| Helsinki Malmi Airport                   | NULL        |
| Helsinki Vantaa Airport                  | Heini       |
| Helsinki East-Redstone Airport           | NULL        |
| Ängelholm-Helsingborg Airport            | NULL        |
| Shelsley-Beauchamp Airstrip              | NULL        |
| Michels Aviação Agrícola LTDA Airport    | NULL        |
| Michels Farms Airport                    | NULL        |
+------------------------------------------+-------------+
https://prnt.sc/sYqGDKYz2ZF5

5.
select goal.name, game.screen_name
    -> from goal
    -> left join goal_reached gr on goal.id = gr.goal_id
    -> left join game on gr.game_id = game.id;
+--------+-------------+
| name   | screen_name |
+--------+-------------+
| HOT    | NULL        |
| COLD   | NULL        |
| 0DEG   | NULL        |
| 10DEG  | Heini       |
| 10DEG  | Vesa        |
| 20DEG  | NULL        |
| CLEAR  | NULL        |
| CLOUDS | Heini       |
| CLOUDS | Ilkka       |
| WINDY  | NULL        |
+--------+-------------+
https://prnt.sc/8cfmhyVjynGh


