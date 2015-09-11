
# describe.h

  Simple BDD describe test thingy

## Installation

  Install with [clib(1)](https://github.com/clibs/clib):

    $ clib install stephenmathieson/describe.h

## Example

```c
#include "describe.h"

int main(void) {
  describe("my program") {
    it("should do stuff") {
      assert(12 == 12);
    }

    it("should fail sometimes") {
      assert(0 == 12);
    }

    it("should be ok after failures") {
      assert(1 == 1);
    }

    it("should bundle assertion macros") {
      assert_equal(1, 1);
      assert_not_equal(1, 2);
      assert_str_equal("hello", "hello");
      assert_str_not_equal("hello", "world");
      assert_null(NULL);
      assert_not_null("not null");
    }
  }
  return assert_failures();
}
```

## License

(The MIT License)

Copyright (c) 2013 Stephen Mathieson &lt;me@stephenmathieson.com&gt;
Copyright (c) 2015 Michael Phan-Ba &lt;michael@mikepb.com&gt;

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
