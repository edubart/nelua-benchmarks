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
|    ackermann |       lua |    863.671 |    864.351 |    865.787 |      0.839 |
|    ackermann |    luajit |    118.921 |    128.813 |    139.048 |      9.559 |
|    ackermann |     nelua |     26.204 |     26.404 |     26.758 |      0.215 |
|    ackermann |         c |     27.703 |     27.757 |     27.852 |      0.060 |
|    fibonacci |       lua |   1688.828 |   1695.720 |   1700.948 |      4.417 |
|    fibonacci |    luajit |    844.899 |    851.083 |    854.129 |      3.624 |
|    fibonacci |     nelua |    261.552 |    262.193 |    262.813 |      0.604 |
|    fibonacci |         c |    261.615 |    262.072 |    262.356 |      0.300 |
|       mandel |       lua |    843.166 |    844.378 |    845.589 |      0.870 |
|       mandel |    luajit |     87.209 |     87.395 |     87.611 |      0.152 |
|       mandel |     nelua |     63.313 |     63.556 |     64.100 |      0.322 |
|       mandel |         c |     63.459 |     63.969 |     64.657 |      0.450 |
|        sieve |       lua |    865.231 |    867.390 |    870.252 |      1.843 |
|        sieve |    luajit |    214.959 |    217.534 |    219.353 |      1.600 |
|        sieve |     nelua |     84.039 |     84.388 |     84.666 |      0.268 |
|        sieve |         c |     54.188 |     55.224 |     56.574 |      1.034 |
|     heapsort |       lua |    979.402 |    990.841 |   1016.197 |     14.764 |
|     heapsort |    luajit |    263.044 |    264.802 |    265.794 |      1.053 |
|     heapsort |     nelua |    180.609 |    182.224 |    184.772 |      1.606 |
|     heapsort |         c |    136.662 |    138.027 |    140.033 |      1.273 |

__NOTE__: Nelua can match C performance when using optimized structures and doing manual memory management. However, to do justice to Lua in the comparisons, the benchmarks were coded in the same style, i.e. using the garbage collector and table-like structures.

* Lua 5.4, LuaJIT 2.1, and GCC 10.2.0 were used in the benchmarks.
* CPU Intel Core i7-3770K (x86_64)
* 06/Feb/2021
