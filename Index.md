# Initial tasks in PL
## Tasks:
All of these tasks are explained for use it in Ubuntu:

1. Install git
2. Introduction to node.js
3. Install and use Pandoc
4. Install Atom
5. Install MarckDown-Preview-Plus

## 1 install git
In ubuntu install git in very simple. Open your bash terminal and use package manager like this:

`$ sudo apt-get install git`

To ensure it is installed correctly,: write in your terminal:

`$ git --help`

![Imagen 4][4]
And you see something like this:

## 2 Introduction to node.js
Little tutorial to install and example of use node.js based on the tutorial of the officia page(see fonts section)

###Introduction
Node.js is an open source, cross-platform runtime environment for server-side and networking
applications. Node.js applications are written in JavaScript, and can be run within the Node.js
runtime on OS X, Microsoft Windows, Linux, FreeBSD, and IBM i.

Node.js provides an event-driven architecture and a non-blocking I/O API that optimizes an
application's throughput and scalability. These technologies are commonly used for real-time
web applications.

Node.js uses the Google V8 JavaScript engine to execute code, and a large percentage of the basic
modules are written in JavaScript. Node.js contains a built-in library to allow applications to
act as a Web server without software such as Apache HTTP Server or IIS


###Instalation
1-First run  http://nodejs.org/  
2-Push install:  
![Imagen 1][1]

 [1]: images/install.png "Install icon"
 [2]: images/hello.png "example1"  
 [3]: images/echopetition.png "example2"
 [4]: images/git.png "gitHelp"

3-When the file is downloaded open shell and put the following commands:  
  To decompress:  
      `$ tar xzvf node-v0.10.36.tar.gz`  
  To install:  
      `$ cd node-v0.10.36`  
      `$ sudo make`
      `$ sudo make install`  
      `$ sudo ./configure`  
  Delete temporary stuff:  
      `$ cd ..`
      `$ rm -rf node-v0.10.36.tar.gz node-v0.10.36`  
We have now installed node.js

###Ejamples of use
This simple web server written in Node responds with "Hello World" for every request.  
```
var http = require('http');  
http.createServer(function (req, res) {  
  res.writeHead(200, {'Content-Type': 'text/plain'});  
  res.end('Hello World\n');  
}).listen(1337, '127.0.0.1');  
console.log('Server running at http://127.0.0.1:1337/');  
```  
To run the server, put the code into a file example.js and execute it with the node program from the command line.     
`$ node example.js`  
Server running at http://127.0.0.1:1337/  

And you can see in http://127.0.0.1:1337/  
![Imagen 2][2]

Here is an example of a simple TCP server which listens on port 1337 and echoes whatever you send it:  
`$ node`

And write:  

```
>var net = require('net');

>var server = net.createServer(function (socket) {
  socket.write('Echo server\r\n');
  socket.pipe(socket);
});

>server.listen(1337, '127.0.0.1');
```  

Then you can see the petition of the browser, in http://127.0.0.1:1337/  
![Imagen 3][3]  
you can change server configuration inline with command node. This produces a  
loop where the code are written and executed in real time.

##3 Install and use Pandoc
Pandoc is a free and open-source software document converter, widely used as a writing tool.

###Instalation
To install it in ubutu put this command in the terminal.

`$sudo apt-get install pandoc`

###Using Pandoc
To use it to convert marckdown to html5 put something like that:

![pandoc command](images/PandocComand.png)

##4 Install Atom
Atom is a hackable text editor for the 21st century, built on Electron, and based on everything we love about our favorite editors. We designed it to be deeply customizable, but still approachable using the default configuration.

###Ubuntu instructions:

Currently only a 64-bit version is available.

* Download atom-amd64.deb from the Atom releases page.
* Run sudo dpkg --install atom-amd64.deb on the downloaded package.
* Launch Atom using the installed atom command.
* The Linux version does not currently automatically update so you will need to repeat these steps to upgrade to future releases.

![Atom](images/atom.png)

##5 Install MarckDown-Preview-Plus
Markdown Preview Plus (MPP) is a fork of Markdown Preview that provides a real-time preview of markdown documents.

###Instalation

1. Search for and install markdown-preview-plus in Atom's Settings view.
2. Search for and disable the built-in package markdown-preview.
3. (Optional) Install and enable Pandoc.

![MarckDownPreviewPLus](images/markdownPrviwe.png)

###use  
`To use it press Mayus + Ctrl + M`

##Fonts

1. Git
  * Font https://git-scm.com/book/en/v2/Getting-Started-Installing-Git (install)
  * Font Manual git in command man. (usage)

2. NodeJS
  * Font http://es.wikipedia.org/wiki/Node.js (introduction)
  * Font http://nodejs.org/ (examples)
  * Font Manual node in command man. (develop tutorial)

3. Pandoc
  * Font http://pandoc.org/ (install)
  * Font Manual Pandoc in command man. (usage)

4. Atom
  * Font https://github.com/atom/atom (install)

5. MarckDown-Preview-Plus
  * Font https://github.com/Galadirith/markdown-preview-plus(install and use)
