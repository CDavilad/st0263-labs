Crear tabla desde Hive
Se utiliza El servicio hue ya que se me resuktó mpas fpacil de realizar


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/32a5364e-422c-4bc4-b608-f466e9ef2a9b)



![image](https://github.com/CDavilad/st0263-labs/assets/63668850/14668b53-9866-4801-9db3-e2f256ca8398)


Archivo hdi cargado


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/2bef0363-24da-4731-b061-966e5da59c21)


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/82c5da43-8855-4c98-baec-89fb01b46aca)




Join de 2 tablas

select country, gni from hdi where gni > 2000; 


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/eb1d76cb-3b13-4307-b4a3-d09262f9f89f)



wordcount


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/9d5161d8-420e-460b-8b98-22cd7a2fdf99)


ordenadi por palabra:

SELECT word, count(1) AS count FROM (SELECT explode(split(line,' ')) AS word FROM docs) w 
GROUP BY word 
ORDER BY word DESC LIMIT 10;

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/7d02e771-a061-4568-974d-079ffb9d5ab7)


ordenado por frecuencia de menor a mayor

SELECT word, count(1) AS count FROM (SELECT explode(split(line,' ')) AS word FROM docs) w 
GROUP BY word 
ORDER BY count DESC LIMIT 10;

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/05cf02e5-a461-4168-8670-da3ac5118c6e)

Reto


CREATE EXTERNAL TABLE reto (
  word STRING,
  count INT
)
STORED AS TEXTFILE
LOCATION 's3://cristianbucket-labs-telematica/datasets/retowordcount/';


INSERT OVERWRITE TABLE reto
SELECT word, count(1) AS count
FROM (
  SELECT explode(split(line, ' ')) AS word
  FROM docs
) w
GROUP BY word
ORDER BY count DESC
LIMIT 10;


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/785cc74a-fb7f-42bc-9968-f43f6c9bdf49)








