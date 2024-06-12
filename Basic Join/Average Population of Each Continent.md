SELECT Country.Continent, FLOOR(AVG(City.population))<br/>
FROM City<br/>
            INNER JOIN Country ON City.CountryCode = Country.Code<br/>
GROUP BY Country.Continent