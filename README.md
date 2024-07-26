# KNOW YOUR HTTP * WELL

HTTP encodings, headers, media types, methods, relations and status codes, all summarized and linking to their specification.

This project is used by [HyperREST bin](https://github.com/andreineculau/hyperrest-bin) at [bin.hyperrest.com](http://bin.hyperrest.com) .


## Table of Contents

- [SPECS](specs.md)
- [ENCODINGS](encodings.md)
- [HEADERS](headers.md)
- MEDIA TYPES
- [METHODS](methods.md)
- [RELATIONS](relations.md)
- [STATUS CODES](status-codes.md)


## How to convert to other formats

* [pandoc](http://johnmacfarlane.net/pandoc/)
* [Marked](http://markedapp.com/)
* ...


## Packages

### Emacs

```emacs
(require 'know-your-http-well)
;; M-x http-header ;; content-type
;; M-x http-method ;; post | POST
;; M-x http-relation ;; describedby
;; M-x http-status-code ;; 500
;; M-x http-status-code ;; not_found | NOT_FOUND
```

### JavaScript

```javascript
var httpWell = require('know-your-http-well'),
    statusWell = httpWell.statusPhrasesToCodes,
    phraseWell = httpWell.statusCodesToPhrases;

// on the server side
res.statusCode = statusWell.NOT_FOUND

// on the client side
if (res.statusCode !== statusWell.OK) {
    // Log "Request returned 404 Not Found"
    log('Request returned ' + res.statusCode + ' ' + phraseWell[res.statusCode]);
}
```

### JSON

Just take a look at [./json/*.json](json).

## References

* https://github.com/dret/webconcepts
* [DanaDanger on twitter.com](https://twitter.com/DanaDanger/status/183316183494311936): `HTTP response codes for dummies. 50x: we fucked up. 40x: you fucked up. 30x: ask that dude over there. 20x: cool.`
* [Steve Losh on twitter.com](https://x.com/stevelosh/status/372740571749572610?lang=en) : `HTTP status ranges in a nutshell: 1xx: hold on. 2xx: here you go. 3xx: go away. 4xx: you fucked up. 5xx: I fucked up`

## License

[Unlicense](LICENSE).

## Stargazers over time

[![Stargazers over time](https://starchart.cc/for-GET/know-your-http-well.svg)](https://starchart.cc/for-GET/know-your-http-well)
