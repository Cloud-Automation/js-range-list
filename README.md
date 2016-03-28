# Range List

Simple and easy tool to merge intervals.

## Installation

A simple `npm install --save js-range-list` will do the trick.

## Example

    var RangeList = require('js-range-list')();

    // add a new interval from [0:2] to the list
    RangeList.merge(0, 2);

    // [ { start: 0, end: 2 }]

    RangeList.merge(4, 10};
    
    // [ { start: 0, end: 2 }, { start : 4, end: 10 }]

    RangeList.merge(2, 6);

    // [ { start: 0, end: 10 }]

    RangeList.getList();

## API

### RangeList([max])

Returns a new RangeList with an optional parameter `max` for the maxmial size of a single interval.

### .merge(start, end)

Adds a new interval to the list. The new interval gets autmatically merged into the existing intervals.

### .getList()

Returns the list of intervals.

## Testing

You can test the module with `jasmine` or `npm test`.

## LICENSE

The MIT License (MIT)
Copyright (c) 2016 stefan.poeter@cloud-automation.de

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

