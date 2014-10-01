[![Express Logo](https://dl.dropboxusercontent.com/u/68595887/OrangeBox.png)](https://github.com/mirrr/orangebox)   
Light [Node.js](http://nodejs.org) web application framework on clusters with file server.
   
## How To Install   

```bash
npm install --save orangebox
```
or
```bash
cd ./node_modules
git clone https://github.com/mirrr/orangebox.git
```
   

## Quick Start

```js
var app = require('orangebox').app();

app.get('/', function (req, res) {
  res.send('Hello World');
});
app.listen(8080);
```
   
After run your web server will work in 4 threads via clusters. To specify the number of threads use: 

```js
var count = 8;
var app = require('orangebox').app(count);
```

  
## A Little More

### File server

```js
var app = require('orangebox').app();

// Creating a file server
app.fileServer(__dirname + '/public');

app.get('/', function (req, res) {
  res.setHeader('Content-Type', 'text/html');
  res.send('<img src="my.png" />');
});

app.listen(8080);
```
Of course you need to put the picture to the folder *public* 



## License
   
MIT License   
   
Copyright (C) 2014 Oleksiy Chechel (alex.mirrr@gmail.com)   
   
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:   
   
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.   
   
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
