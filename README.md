# CANSUS_2011_analysis
Hello Everyone!!
Really excited in sharing the completion of my SQL Portfolio Project.
In this project, I Created Table and import the dataset using the inline import in MySQL Workbench and altered the Datatypes of some columns.


CREATE DATABASE SQL_PROJECT;
SELECT * FROM dataset1;
SELECT * FROM dataset2;
--------------------------------------------------------------------------------------------------------
SELECT SUM(population) 
AS total_population
FROM dataset2;
-----------------------------------------------------------------------------------------------------------
SELECT state, sum(population)
 As total_population 
 from dataset2 
 group by State;
 ------------------------------------------------------------------------------------------------------------
 SELECT state, avg(literacy) 
 as average_literacy_rate 
 from dataset1 
 group by state;
 -------------------------------------------------------------------------------------------------------------
 SELECT state, avg(sex_ratio) 
 as average_sex_ratio
 from dataset1
 group by State;
 ----------------------------------------------------------------------------------------------------------------
 SELECT district, growth
 AS growth_rate
 FROM dataset1
 ORDER BY Growth DESC
 limit 1;
 -------------------------------------------------------------------------------------------------------------------
 SELECT district, literacy
 FROM dataset1
 ORDER BY Literacy DESC
 LIMIT 1;
 SELECT district, literacy
 FROM dataset1
 ORDER BY Literacy ASC
 LIMIT 1;
 ----------------------------------------------------------------------------------------------------------------------
 SELECT *
 FROM dataset1
 INNER JOIN dataset2 ON dataset1.District = dataset2.District;
 ------------------------------------------------------------------------------------------------------------------
 SELECT AVG(sex_ratio) 
 AS overall_averge_sex_ratio
 FROM dataset1;
 -------------------------------------------------------------------------------------------------------------------
 SELECT state, AVG(growth) AS average_growth_rate
FROM dataset1
GROUP BY state
ORDER BY average_growth_rate DESC
LIMIT 1;
SELECT state, AVG(growth) AS average_growth_rate
FROM dataset1
GROUP BY state
ORDER BY average_growth_rate ASC
LIMIT 1;
--------------------------------------------------------------------------------------------------
SELECT District, Area_km2, Population AS population_density
FROM dataset2
ORDER BY population_density DESC
LIMIT 1;
SELECT District, Area_km2, Population As population_density
FROM dataset2
ORDER BY population_density ASC
LIMIT 1;
-------------------------------------------------------------------------------------------------------------

