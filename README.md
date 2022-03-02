Temas en cocideracion para correr y usar este proyecto debe saber sobre  estas librerias ya que el boilertplate tiene integracias para el manejo de autenticacion 
https://jwt.io/libraries?language=Node.js
https://www.passportjs.org/packages/
https://nodemailer.com/about/
https://sequelize.org/

Para correr debemos tener instalado docker  en nuesto equipo.

una vez clonado corremos los siguientes comandos

installar las dependencias del proyecto 
# npm insatall

puedes correr el backend con 
# npm start


Luego creamos nuesto contenedor donde estara alojada la Base de datos
# docker-compose up -d postgresDB

Luego creamos la imagen de nuestro admin de postgres
# docker-compose up -d pgadmin

  Este se alojara en el puerto   http://localhost:5050/ 

luego procedemos a conectar nuestro server en el admin de postgres para ver el host de la instancia puede usar los siguientes comandos 

 con este sacamos el id de nuestro contendor de docker
 # docker ps 
 con este podemos ver a detalle el ip adress de nuestro contenedor y proceder a crear nuestro serve con los datos de nuestra db 
 # docker inspect 5a5e875b0ded 


Una vez ya el proyecto este corriendo en la ruta boilerplate-nodejs-postgres/libs/sequlize.js en la linea 17 quitar lo comentado para crear las tablas y correr el proyecto, cuando ya esten las tablas creadas volver a comentar
 # sequelize.sync();
