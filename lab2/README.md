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


ordenar por palabra:

SELECT word, count(1) AS count FROM (SELECT explode(split(line,' ')) AS word FROM docs) w 
GROUP BY word 
ORDER BY word DESC LIMIT 10;








