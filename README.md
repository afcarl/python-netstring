Python-Netstring
================

Python-Netstring is a Python implementation of a netstring parser. 
cf. http://cr.yp.to/proto/netstrings.txt

Usage
-----

Python-Netstring comes with one function and one class.

netstring function

    Encodes a Python object as a netstring.
    
    >>> netstring(456)
    '3:456,'
    >>> netstring(['abc', 'defg'])
    '3:abc,4:defg,'

NetstringParser

    Decodes a netstring to a list of Python strings.

    >>> parser = NetstringParser()
    >>> parser.feed('3:456,')
    >>> parser.results
    ['456']
    >>> NetstringParser.parse('3:abc,4:defg,')
    ['abc', 'defg']


Terms and Conditions
--------------------

(This is so-called MIT/X License)

Copyright (c) 2014 Yusuke Shinyama <yusuke at cs dot nyu dot edu>

Permission is hereby granted, free of charge, to any person
obtaining a copy of this software and associated documentation
files (the "Software"), to deal in the Software without
restriction, including without limitation the rights to use,
copy, modify, merge, publish, distribute, sublicense, and/or
sell copies of the Software, and to permit persons to whom the
Software is furnished to do so, subject to the following
conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY
KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
