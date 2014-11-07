European Turnout for Election to European Parliament
====================================================
- Source: European Parliament website: [“Turnout at the European elections (1979–2009)”][source]. View the PDF files the data is based on [here][source].
- View and inspect the data [here][view].
- Get the raw CSV [here][raw].

You may prefer to view the data at the linked source where the presentation is better; this is mainly preferable for crunching data.

### Table Excerpt ###
Year | BE | DK | DE | IE | FR | IT | LU | NL | UK | EL | ES | PT | SE | AT | FI | CZ | EE | CY | LT | LV | HU | MT | PL | SI | SK | BG | RO
-----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----|----
2004 | 90.81 | 47.89 | 43.00 | 58.58 | 42.76 | 71.72 | 91.35 | 39.26 | 38.52 | 63.22 | 45.14 | 38.60 | 37.85 | 42.43 | 39.43 | 28.30 | 26.83 | 72.50 | 48.38 | 41.34 | 38.50 | 82.39 | 20.87 | 28.35 | 16.97 |  |
2007 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | 29.22 | 29.47
2009 | 90.39 | 59.54 | 43.30 | 58.64 | 40.63 | 65.05 | 90.75 | 36.75 | 34.70 | 52.61 | 44.90 | 36.78 | 45.53 | 45.97 | 40.30 | 28.20 | 43.90 | 59.40 | 20.98 | 53.70 | 36.31 | 78.79 | 24.53 | 28.33 | 19.64 | 38.99 | 27.67

Validation
----------
All CSV files have been validated with `csvlint` to ensure proper CSV.

(For `csvlint` to work, however, you have to temporarily replace all the null values (`-`) with a number for the script to work.)


[source]: http://www.europarl.europa.eu/aboutparliament/en/000cdcd9d4/Turnout-(1979-2009).html
[view]: https://github.com/ndarville/data/blob/master/elections/_turnout/eu/european-parliament/data.csv
[raw]: https://github.com/ndarville/data/raw/master/elections/_turnout/eu/european-parliament/data.csv
