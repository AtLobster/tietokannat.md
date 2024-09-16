1.
select country.name
    -> from airport
    -> join country on airport.iso_country = country.iso_country
    -> where airport.name like "satsuma%";
  
