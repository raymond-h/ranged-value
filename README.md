# ranged-value
Simple class for values with a min and max (like HP in videogames)

## Installing
`npm install ranged-value`

## Example usage
```js
var RangedValue = require('ranged-value');

// The main parameter object can have 3 properties:
// `min`, `current`, and `max`.
// `min` defaults to `0`, `current` defaults to `max`.

val hp = new RangedValue({max: 20});

// The parameter values are available under the same name
// on the instance itself.

// ogre attack!
hp.current -= 10;

// priest heal!
hp.current += 20;

if(hp.full) console.log('I feel really good!');

// wow, this guy punches really hard!!
hp.current -= 500;

if(hp.empty) console.log('Oh no, I am dead!');

hp.percent = 0.7;

if(!hp.empty) console.log('I have been resurrected, with ' + hp.percent * 100 + '% HP!');

JSON.stringify(hp); // {"min": 0, "current": 14, "max": 20}
```
    
## License
The MIT License (MIT)

Copyright (c) 2015 Raymond Hammarling

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.