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

![alt tag](https://drive.google.com/uc?id=0B4fau-D6sg2rY2xhZ2piNmU4djA)

`info`

![alt tag](https://drive.google.com/uc?id=0B4fau-D6sg2rYkNVT1ExUkZwek0)

`error`

![alt tag](https://drive.google.com/uc?id=0B4fau-D6sg2reHlrU3Q2SG1LYmc)

`warn`

![alt tag](https://drive.google.com/uc?id=B4fau-D6sg2rY3FZUzRZUGdENGs)


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
