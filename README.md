# deveshgoyal.github.io

Express.js flash notifications that can work with any template engine

# Flash Express

  Flash Messages for your Express Application

## Installation

  Works with Express 3.x.x

    npm install npm install git://github.com/deveshgoyal/flash-express.git

## Usage

  Set it up the same way you would `ExpressJs`:

``` javascript
  var flash = require('flash-express'),
      express = require('express'),
      app = express();
      
  app.use(flash());
```

Use `res.flash( msg [, type ] [, option ])` in your middleware

``` javascript
  app.get('/', function (req, res) {
    res.flash('Welcome', 'info');
    res.render('index', {
      title: 'Home'
    })
  });
  app.get('/addFlash', function (req, res) {
    res.flash()
    res.flash('Flash Message Added');
    res.redirect('/');
  });
```

Access the messages in your views by just importing the following script before the end of body tag.

In case of html/hbs
``` html
  ...
  <script type="text/javascript" src="flash/flash-client.js"></script>
  </body>
  ...
```
## Type

Type can be of four kinds 


`success`

``` html
<div style="opacity: 1;float:left;padding: .3em .4em;margin:0 auto .5em;display:inline-block;clear:both;position:relative;min-width:120px; /* 610/13 */ *max-width:45.750em; /* 610/13.3333 - for IE */color:green;background-color: rgba(9, 129, 0, 0.42);border-radius: 5px;border: 1px green solid;">success</div>
```

`info`

``` html
<div style="opacity: 1;float:left;padding: .3em .4em;margin:0 auto .5em;display:inline-block;clear:both;position:relative;min-width:120px; /* 610/13 */ *max-width:45.750em; /* 610/13.3333 - for IE */color:blue;background-color: rgba(26, 22, 242, 0.42);border-radius: 5px;border: 1px blue solid;">info</div>
```

`error`

``` html
<div style="opacity: 1;float:left;padding: .3em .4em;margin:0 auto .5em;display:inline-block;clear:both;position:relative;min-width:120px; /* 610/13 */ *max-width:45.750em; /* 610/13.3333 - for IE */color:red;background-color: rgba(255, 0, 0, 0.42);border-radius: 5px;border: 1px red solid;">error</div>
```

`warn`

``` html
<div style="opacity: 1;float:left;padding: .3em .4em;margin:0 auto .5em;display:inline-block;clear:both;position:relative;min-width:120px; /* 610/13 */ *max-width:45.750em; /* 610/13.3333 - for IE */color:coral;background-color: rgba(255, 250, 80, 0.87);border-radius: 5px;border: 1px coral solid;">warn</div>
```

## License 

(The MIT License)

Copyright (c) 2016 DEVESH GOYAL &lt;me@deveshgoyal.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
