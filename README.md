# @tracker1/deep-merge

Deep merges javascript objects.

## Import/Require

```
// CJS
const deepMerge = require('@tracker1/deep-merge');

// ESM
import deepMerge from '@tracker1/deep-merge';
```

## Use

```
const a = { a: 'foo', b: { c:'bar', d:'baz' }, e: { f: 'to be replaced' } };
const b = { x: 'biff', b: { d: 'bazzer' }, e: { __REPLACE__: 'deep replaces e', g: 'new value' } };

console.log(deepMerge(a, b));
// {
//   a: 'foo',
//   b: { c: 'bar', d: 'bazzer' },
//   e: { g: 'new value' },
//   x: 'biff'
// }
```

### Replace

Objects with a truthy `__REPLACE__` property will replace the original entirely (without the `__REPLACE__` property);

## License

MIT License

Copyright (c) 2019 Michael J. Ryan

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.