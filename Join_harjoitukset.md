1.
select country.name "country name", airport.name "airport name"
    -> from airport
    -> join country on airport.iso_country = country.iso_country
    -> where scheduled_service = "yes" and country.name = "Finland";

https://prnt.sc/AUzaB27uUaqg


2.
select game.screen_name, airport.name
    -> from game
    -> join airport on game.location = airport.ident
    -> ;

https://prnt.sc/nqvyQRphERWh

3.
select game.screen_name, country.name
    -> from game
    -> join airport on game.location = airport.ident
    -> join country on airport.iso_country = country.iso_country;

https://prnt.sc/Xb9qL-873yFL

4.
select airport.name, game.screen_name
    -> from airport
    -> left join game on game.location = airport.ident
    -> where airport.name like "%hels%";

https://prnt.sc/sYqGDKYz2ZF5

5.
select goal.name, game.screen_name
    -> from goal
    -> left join goal_reached gr on goal.id = gr.goal_id
    -> left join game on gr.game_id = game.id;

https://prnt.sc/8cfmhyVjynGh


