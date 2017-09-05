Services-Json
======

## Converts to and from JSON format

JSON (JavaScript Object Notation) is a lightweight data-interchange
format. It is easy for humans to read and write. It is easy for machines
to parse and generate. It is based on a subset of the JavaScript
Programming Language, Standard ECMA-262 3rd Edition - December 1999.
This feature can also be found in  Python. JSON is a text format that is
completely language independent but uses conventions that are familiar
to programmers of the C-family of languages, including C, C++, C#, Java,
JavaScript, Perl, TCL, and many others. These properties make JSON an
ideal data-interchange language.

This package provides a simple encoder and decoder for JSON notation. It
is intended for use with client-side Javascript applications that make
use of HTTPRequest to perform server communication functions - data can
be encoded into JSON notation for use in a client-side javascript, or
decoded from incoming Javascript requests. JSON format is native to
Javascript, and can be directly eval()'ed with no further parsing
overhead
 
All strings should be in ASCII or UTF-8 format!

Converts to and from JSON format.

Brief example of use:

```php
// create a new instance of Services_JSON
$json = new Services_JSON();

// convert a complexe value to JSON notation, and send it to the browser
$value = array('foo', 'bar', array(1, 2, 'baz'), array(3, array(4)));
$output = $json->encode($value);

print($output);
// prints: ["foo","bar",[1,2,"baz"],[3,[4]]]

// accept incoming POST data, assumed to be in JSON notation
$input = file_get_contents('php://input', 1000000);
$value = $json->decode($input);

// if you want to convert json to php arrays:
$json = new Services_JSON(SERVICES_JSON_LOOSE_TYPE);
```

