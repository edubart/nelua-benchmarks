# Benchmarks

These are some benchmarks comparing Nelua with Lua, LuaJIT and C.
The code is made similar as possible between the language implementations.
The code uses the usual style of coding in Lua,
that is, using just tables and a garbage collector,
there are no fancy tricks to optimize further
in Nelua or LuaJIT implementations.

## Lasted Results

|    benchmark |  language |   min (ms) |   avg (ms) |   max (ms) |   std (ms) |
|--------------|-----------|------------|------------|------------|------------|
|    ackermann |       lua |   1108.149 |   1185.912 |   1393.872 |    120.194 |
|    ackermann |    luajit |    137.142 |    142.441 |    156.613 |      8.195 |
|    ackermann |     nelua |     43.084 |     48.714 |     50.844 |      3.255 |
|    ackermann |         c |     44.041 |     46.669 |     50.883 |      2.615 |
|    fibonacci |       lua |   2168.007 |   2170.071 |   2171.142 |      1.264 |
|    fibonacci |    luajit |    934.416 |    953.189 |    979.999 |     18.430 |
|    fibonacci |     nelua |    312.384 |    316.041 |    320.528 |      3.524 |
|    fibonacci |         c |    311.299 |    317.486 |    322.866 |      4.367 |
|       mandel |       lua |   1623.193 |   1666.009 |   1790.736 |     72.015 |
|       mandel |    luajit |    103.980 |    107.072 |    108.947 |      2.000 |
|       mandel |     nelua |     99.933 |    101.243 |    102.532 |      0.927 |
|       mandel |         c |     91.748 |     98.417 |    101.064 |      3.866 |
|        sieve |       lua |   1087.724 |   1100.847 |   1110.813 |      9.253 |
|        sieve |    luajit |    278.457 |    278.859 |    279.621 |      0.472 |
|        sieve |     nelua |     94.704 |     98.337 |    103.300 |      3.509 |
|        sieve |         c |     69.213 |     71.989 |     75.431 |      2.743 |
|     heapsort |       lua |   1592.553 |   1636.320 |   1742.035 |     61.304 |
|     heapsort |    luajit |    293.734 |    300.018 |    305.558 |      4.501 |
|     heapsort |     nelua |    177.532 |    179.762 |    182.379 |      1.949 |
|     heapsort |         c |    138.407 |    140.028 |    141.463 |      1.357 |

__NOTE__: Nelua can match C performance when using optimized structures and doing manual memory management. However, to do justice to Lua in the comparisons, the benchmarks were coded in the same style, i.e. using the garbage collector and table-like structures.

* Lua 5.4, LuaJIT 2.1, and GCC 10.2.0 were used in the benchmarks.
* CPU Intel Core i7-3770K (x86_64)
* 25/Jan/2021
