# luvit-favicon

Luvit.io middleware for serving favicon (typically used with [Utopia](https://github.com/luvitrocks/luvit-utopia)).

## Install

```bash
npm install luvit-favicon
```

If you're not familiar with [npm](https://www.npmjs.org/) check this out:
- https://github.com/voronianski/luvit-npm-example#how-to
- https://github.com/luvitrocks/luvit-utopia#install

## Example

This middleware will come very early in your stack (maybe even first) to avoid processing any other middleware if we already know the request is for /favicon.ico.

### Utopia

```lua
local utopia = require('luvit-utopia')
local favicon = require('luvit-favicon')
local http = require('http')

local app = utopia:new()

app:use(favicon(__dirname .. '/public/favicon.ico'))

http.createServer(app):listen(8080)
```

## License

MIT Licensed

Copyright (c) 2014 Dmitri Voronianski [dmitri.voronianski@gmail.com](mailto:dmitri.voronianski@gmail.com)

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
