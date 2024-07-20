## Install NodeJS in Ubuntu

### Download NodeJS veersion

- Head over to 
- Download .xz/.tar file into say ~/Downloads directory
- extraxt .xz and .tar

### Local installation

- Copy extracted node directory in /usr directory so that it's reachable for all users in this PC/mac
- Use the following command to accomplish this task
```
sudo cp -r node-v18.12.1-linux-x64/{bin,include,lib,share}  /usr/
```
- Check if the installation was successful with the folowing commands
```
find /usr -name node
node --version
```

### Enjoy

Build a simple application to see if all is well
- Create a simple server.js
```
touch server.js
```
- Open the file and add the following contents
```
var http = require('http');

http.createServer(function (req, res) {
res.writeHead(200, {'Content-Type': 'text/plain'});
res.end('Hello World!');
}).listen(8080);
```
- Execute this file
```
nohup node server.js > node.log 2>&1 &
```
- Make a request and see if it's up & running
```
wget -q -O - http://127.0.0.1:8080
```

It's time to read more, enjoy and build more solutions!!