## BOJ Payment and Settlement Statistics

This repo contains the Bank of Japan (BOJ) [Payment and Settlement Statistics](https://www.boj.or.jp/en/statistics/set/kess/index.htm/) report from February 2000. While the BOJ doesn't link directly to data from [3 years ago](https://www.boj.or.jp/en/statistics/outline/notice_2018/not181031b.htm/), they used to have the files up. It looks like they have removed the links to older reports now. The BOJ sets up the links to the reports nicely in the form of

    https://www.boj.or.jp/en/statistics/set/kess/release/<4 digit year>/kess<2 digit year><2 digit month>.pdf

For example, the link for the August 2018 publication is:

    https://www.boj.or.jp/en/statistics/set/kess/release/2018/kess1808.pdf

For earlier data, please contact them at post.pr@boj.or.jp.

You can also go to the [BOJ Time-Series Data Search](http://www.stat-search.boj.or.jp/index_en.html) to get some of the data available in the reports. The data is under the "Other Payment and Settlement Systems" category. Below is the mapping of the available time series to their locations in the PDF:

| Time series dataset | Location in the PDF |
|---|---|
| `PS01'PMRA2` Settlement via BOJ Accounts (a)/Value/Daily Average | Table 1-1 "Value" column |
| `PS01'PMRA3` Settlement via BOJ Accounts (a)/Number of Transactions | Table 1-1 "Volume" × [n](#notes "numbers of open days in the month") |
| `PS01'PMRA4` Settlement via BOJ Accounts (a)/Value | Table 1-1 "Value" column × [n](#notes "numbers of open days in the month") |
| `PS01'PMRA@01` JGB Book-entry System (b)(c)/Number of Transactions | Table 3-1 (1) "Volume" column × [n](#notes "numbers of open days in the month") |
| `PS01'PMRA@02` JGB Book-entry System (b)(c)/Value | Table 3-1 (2) "Value" column × [n](#notes "numbers of open days in the month") |
| `PS01'PMRA@03` JGB Book-entry System (b)(c)/Value/Daily Average | Table 3-1 (2) "Value" column |

#### Notes

n = numbers of business days in the month ([Holiday schedule of BOJ](https://www.boj.or.jp/en/about/outline/holi.htm/))
