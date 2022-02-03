# Web Server en NodeJS

### Verificar la version de NodeJS y NPM (Terminal Ubutnu)
```
node -v && npm -v
```
### Crear carpeta donde se almacenara el proyecto
```
mkdir mi-server-web
```
### Acceder a la carpeta
```
cd mi-server-web/
```
### Inicia el Proyecto (Nos pedira datos para personalizar)
```
npm init 
```
### Inicia el Proyecto (Se crea un package.json con valores predeterminados)
```
npm init --yes
```
### Creamos archivos app.js
```
nano app.js
```
### Pegamos el siguiente codigo en app.js
```
const http = require('http');

//Remplazar 127.0.0.1 por la IP donde se encuentra el codigo

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!\n');
});

server.listen(port, hostname, () => {
  console.log(`Servidor Iniciado en http://${hostname}:${port}/`);
});
```
### Ejecutamos desde la terminal app.js
```
node app.js
```
### Como mensaje de salida saldra Servidor Iniciado en http://127.0.0.1:3000/
```
>_ Servidor Iniciado en http://127.0.0.1:3000/
```
