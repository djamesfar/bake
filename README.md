# Bake plugin for CakePHP

[![License](https://poser.pugx.org/cakephp/bake/license.svg)](https://packagist.org/packages/cakephp/bake)

This is a beta version of the "bake" system for CakePHP 3.0. It is currently under
development and should be considered experimental.

## Installation

You can install this plugin into your CakePHP application using [composer](http://getcomposer.org).

The recommended way to install composer packages is:

```
composer require --dev Stage32/bake-plugin
```

## Modifications

#### Date 
3/10/2015 

#### Author
djamesfar DJ Far

### Files

ModelTask.php

### Changes
##### Current Behavior
If a keyfield exists in a table that references no table, Bake will create a class using conventions: dropping the "\_id" extention and inflecting to a classname.  No attempt is made to verify a referenced table.
##### Proposed/Implemented behavior
The function getBelongsTo() has been changed to search the tables list, if a matching table is not found, the keyField is passed to findTableReferencedBy($keyField), which returns a matching table if any.

## License

Copyright (c) 2015 Cake Software Foundation, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
