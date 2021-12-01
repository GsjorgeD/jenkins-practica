# Jenkins-practica
Ejercicio de practica para conexion con Jenkins

## Jenkins en Heroku
### usaremos Heroku para instalar Jenkins

Descargamos la version LTS de Generic Java package (.war) : https://www.jenkins.io/download/

Crearemos con los archivos pom.xml y Procfile basandonos en: https://gist.github.com/jordansissel/2313443 

### Iniciaremos un repositorio local con  los archivos anteriores:

```sh
git init
```

```sh
git add .
```
```sh
git commit -m"initial commit"
```
### Crearemos una nueva aplicacion en heroku 
Para ello ingresa tu cuenta o crea una nueva y desde el panel damos clic en crear nueva app

![](https://miro.medium.com/max/724/1*RRsMnNP4wIi-tLvzd9jGZg.png)

### Desde tu cmd o shell
Nota : es necesario tener intalado el cli de Heroku: https://devcenter.heroku.com/articles/heroku-cli#download-and-install
```sh
heroku login
```
```sh
heroku git:remote -a nombredetuapp
```
```sh
git push heroku master
```
Esperamos y verificamos que se generar correctamente el deploy 

#### Ingresa a tu navegador a la direccion de tu app que generalmente es "nombredetuapp.herokuapp.com"
Te pedira una contraseña para desbloquear
### Ejecuta en el cmd o shell para obtener la contraseña: 
###

```sh
heroku restart
```
```sh
heroku logs
```
#### Te mostrara varios detalles entre ellos tu contraseña

*************************************************************


 Jenkins initial setup is required. An admin user has been created and a password generated.
 Please use the following password to proceed to installation:
```sh
Tu contraseña generada
```
 This may also be found at: /app/.jenkins/secrets/initialAdminPassword
  *************************************************************



