## Simple Example: Fibonacci in C++
<br />
### Code:
    int fib(int n) {
      if(n <= 0) {
        return 0;
      } else if (n == 1) {
        return 1;
      } else {
        return fib(n-2) +
          fib(n-1);
      }
    }
    void main() {
      cout << fib(5) << endl;
    }

<br />
### Test:
    void testFib() {
      // given
      int n = 6;
      // when
      int x = fib(n);
      // then
      assert(x, 8);
    }
