SELECT DISTINCT id, name, countrycode, district, population
FROM city
WHERE population >100000 and countrycode='USA'
