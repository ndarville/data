Danish General-Election Data
============================
For a general overview of Danish election data, see the [overview README][overview].

Source: ft.dk: [“Folketingsvalg i Danmark siden 1913”][ge-source]. View the PDF files the data is based on [here][ge-original].

Data Files
----------
- [`1913-1953.csv`][ge-csv-1]
- [`1953-1971.csv`][ge-csv-2]
- [`1973-2011.csv`][ge-csv-3]

For now, the datasets are split into three due to the number of parties coming and going, as well as the [constitutional changes of 1953][1953]. You’ll want to focus on the latter dataset.

Understanding the Data
----------------------
The dataset is fairly basic in that it merely contains

- The election data (`MM/DD/YYYY`) in the first column.
- The parties’ share of votes (`100.0`).
- The election turnout of eligible voters (`100.0`) in the last column.

The number of mandates for each party are not included for the time being.

### Table Excerpt ###
Date       | S    | RV   | KF  | CD  | DR  | SF  | DKP | DF | FK | KD  | V    | VS  | FP   | EL | LA | Other | Turnout
-----------|------|------|-----|-----|-----|-----|-----|----|----|-----|------|-----|------|----|----|-------|--------
12/04/1973 | 25.6 | 11.2 | 9.2 | 7.8 | 2.9 | 6.0 | 3.6 |  - |  - | 4.0 | 12.3 | 1.5 | 15.9 |  - |  - |   0.0 | 88.7
01/09/1975 | 29.9 |  7.1 | 5.5 | 2.2 | 1.8 | 5.0 | 4.2 |  - |  - | 5.3 | 23.3 | 2.1 | 13.6 |  - |  - |   0.0 | 88.2
02/15/1977 | 37.0 |  3.6 | 8.5 | 6.4 | 3.3 | 3.9 | 3.7 |  - |  - | 3.4 | 12.0 | 2.7 | 14.6 |  - |  - |   0.9 | 88.7

Validation
----------
All CSV files have been validated with `csvlint` to ensure proper CSV.

(For `csvlint` to work, however, you have to temporarily replace all the null values (`-`) with a number for the script to work.)


[overview]: https://github.com/ndarville/data/blob/master/elections/dk/README.md
[ge-source]: http://www.ft.dk/Folketinget/Oplysningen/Valg/ValgresultaterDK.aspx
[ge-original]: https://github.com/ndarville/data/blob/master/elections/dk/general/_original
[ge-csv-1]: https://github.com/ndarville/data/blob/master/elections/dk/general/1913-1953.csv
[ge-csv-2]: https://github.com/ndarville/data/blob/master/elections/dk/general/1953-1971.csv
[ge-csv-3]: https://github.com/ndarville/data/blob/master/elections/dk/general/1973-2011.csv
[1953]: http://en.wikipedia.org/wiki/Danish_constitutional_and_electoral_age_referendum,_1953
