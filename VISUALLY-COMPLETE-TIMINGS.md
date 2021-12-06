### WPT Visual Completeness
- Chrome: **2.150s**
  - https://webpagetest.org/result/211204_AiDcBZ_71516c114209225b0fe24e3cd94a0a37/?medianMetric=visuallyComplete#run2
- Firefox: **3.901s**
  - https://webpagetest.org/result/211204_BiDcFN_9e24929cc7bcee577dfeca8d31269cd4/?medianMetric=visuallyComplete#run2
- Firefox Nightly: **4.481s**
  - https://webpagetest.org/result/211206_AiDcKV_52d8d30f3df3e8376c82a924de859e25/?medianMetric=visuallyComplete#run2

### Manual Visual Completeness tests


**Methodology:**
1. Use builtin screen recorder to capture page loading
2. Visit [target page](https://richallanb.github.io/esm-with-http2/es6-modules.html) 3 times to warm up cache
3. Visit about:blank at the beginning of each run
4. Visit [target page](https://richallanb.github.io/esm-with-http2/es6-modules.html)
5. Repeat 3 times
6. Capture start of visit and last visual change using Avidemux (frame by frame analysis)

|                        | Run #1 VC | Run #2 VC | Run #3 VC | Median |
|------------------------|-----------|-----------|-----------|--------|
| FF w/o devtools 94.0.1 | 1.20s     | 0.55s     |  0.9s     | 0.9s   |
| FF w/devtools 94.0.1   | 3.27s     | 2.73s     | 2.82s     | 2.82s  |
|                        |           |           |           |        |

```
OSX Big Sur 11.6.1
MacBook Pro 16-inch, 2019
2.3Ghz 8-Core Intel Core i9
32GB 2667MHZ DDR4

Firefox 94.0.1
```