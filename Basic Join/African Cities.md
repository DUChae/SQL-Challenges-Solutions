SELECT City.name <br/>
FROM City <br/>
            INNER JOIN Country ON City.CountryCode = COUNTRY.Code <br/>
WHERE Continent='Africa'