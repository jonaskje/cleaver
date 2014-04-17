title: API Design
author:
	name: Jonas Kjellström
	email : jonas.kjellstrom@dice.se
output: apidesign.html
controls: false
progress: false

--

# A New Webservice
## Better and improved

--

### Agenda

- Blah
- Tjoj

--

### First slide

- apapap
- asdfjaskdfj
- [To Google](http://www.google.com)
--

### Diagram

%%%% ditaaborder

    +--------+   +-------+    +-------+
    |        | --+ ditaa +--> |       |
    |  Text  |   +-------+    |Diagram|
    |Document|   |!magic!|    |       |
    |     {d}|   |       |    |       |
    +---+----+   +-------+    +-------+
        :                         ^
        |       Lots of work      |
        +-------------------------+

%%%%

--

### Code

``` javascript
Renderer.prototype.image = function(href, title, text, clazz) {
  var out = '<img src="' + href + '"';
  if (text) { 
    out += ' alt="' + text + '"';
  }
  if (title) {
    out += ' title="' + title + '"';
  }
  if (clazz) {
    out += ' class="' + clazz + '"';
  }
  out += this.options.xhtml ? '/>' : '>';
  return out;
};
```

--

### Memory layout

%%%% ditaaborder

	+-----------------+
	| Header          |
	+-----------------+
	| Body            |
	|                 |
	|                 |
	+-----------------+
	| CRC             |
	+-----------------+

%%%%

--

### Memory layout

%%%% ditaaborder

	+-----------------+
	| Header          |
	+-----------------+
	| Body            |
	|                 |
	|    cF00         |
	+-----------------+
	| CRC             |
	+-----------------+

%%%%

--

### Memory layout #2

%%%% ditaaborder

	+-----------------+         +-----------------+
	| Header          +-------->| Header          |
	+-----------------+         +-----------------+
	| Body            |         | Body            |
	|                 |         |                 |
	|                 |         |                 |
	+-----------------+         +-----------------+
	| CRC             |         | CRC             |
	+-----------------+         +-----------------+

%%%%

