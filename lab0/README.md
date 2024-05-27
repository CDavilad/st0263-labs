Crear Cluster

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/ec4e42b0-518d-4f4e-ad86-16e18010d50f)

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/08fe9c23-3a65-4bb0-adcf-1e8d785fb884)

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/ce7755ad-c882-4232-9166-d7af0fec5659)

m5.xlarge dio problemas:


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/299ab77c-c601-4c4f-9bf5-ce45a56504ab)


Entramos a Hue:


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/e18904cd-3be1-4340-ac14-3338adf871f3)


No podremos acceder al servicio de HDFS por lo que tenemos que configurar el archivo hue.ini de la máquina master

![image](https://github.com/CDavilad/st0263-labs/assets/63668850/c265e041-c19a-440a-8957-db93f9798444)


y reiniciamos le servicio

systemctl restart hue.service


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/847937d8-171a-49e1-bead-514e0001bf05)


Luego ingresamos a JupyterHub, es el puerto 9443


![image](https://github.com/CDavilad/st0263-labs/assets/63668850/0c73f545-d5cc-4847-94d2-eab902035534)


y se crea un Pyspark y se corren las 2 líneas que se ven en la imagen
