# PYLIBLO 

This is a fork of the original bindings for liblo

It implements some additional features, like removing registered methods.

Supports both Python >= 2.7 and Python >= 3.3

## Dependencies

* liblo >= 0.28
* cython >= 0.20

## Example


### Simple Server

```python

import liblo
server = liblo.Server(8080)

def test_handler(path, args, types, src):
    print(args)
    
server.add_method("/test", None, test_handler)

while True:
    server.recv(100)
```

-------

Original README:


	pyliblo - Python bindings for the liblo OSC library

	Copyright (C) 2007-2011  Dominic Sacré  <dominic.sacre@gmx.de>

	http://das.nasophon.de/pyliblo/


	To install, run "./setup.py build", followed by "./setup.py install". This
	will install both the python module and the send_osc/dump_osc scripts.

	See doc/API.html and doc/examples.html for API documentation and some
	example code.
