SELECT SUM(City.Population) <br/> 
FROM City <br/>
            INNER JOIN Country ON City.CountryCode = Country.Code <br/>
WHERE Continent='Asia'