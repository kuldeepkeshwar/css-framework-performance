# A performance comparison of css approaches

<img src="https://raw.githubusercontent.com/jakejarvis/lighthouse-action/master/screenshots/logo.png" width="300">  

[![Deploy Task](https://github.com/jantimon/css-framework-performance/workflows/github%20pages/badge.svg)](https://jantimon.github.io/css-framework-performance/)

The following table shows [different speed measurments](https://developers.google.com/web/updates/2018/05/lighthouse3#scoring) for the same demo implemented with different js and css technologies. The results are sorted by the amount of time it takes for the page to become fully interactive.

<a href="https://jantimon.github.io/css-framework-performance/" id="report-table">See the results</a>

##### How do you generate these values?

Every commit to the [css-framework-performance master branch](https://github.com/jantimon/css-framework-performance/) generates five lighthouse reports for each project in the [css-frameworks folder](https://github.com/jantimon/css-framework-performance/tree/master/css-frameworks).

The teste is executed with the following parameters:

```bash
  lighthouse
    http://127.0.0.1/
    --throttling.cpuSlowdownMultiplier=4
    --chrome-flags="--headless"
    --throttling-method=devtools
```

The network throtteling is using the [lighthouse devtools defaults](https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md).  
These defaults simulate `3G` as seen in the footer of every lighthouse report:

- Latency: 150ms
- Throughput: 1.4Mbps down / 675 Kbps up.
- Packet loss: none.

##### Feel free to contribute

To add a new technology create a new demo implementation inside the [css-frameworks folder](https://github.com/jantimon/css-framework-performance/tree/master/css-frameworks).