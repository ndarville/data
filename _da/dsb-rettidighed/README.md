DSB-Rettidighed
===============
Data fra [DSB][source].

Datafiler
----------
 Filnavn                    | View rendered | View raw
:---------------------------|:-------------:|:--------------:
 `rettidighed.csv`          | [View][rt]    | [View][rt-raw]
 `operatoerregularitet.csv` | [View][or]    | [View][or-raw]

Format
------
* UTF-8
* Unix line endings

Databeskrivelse
---------------
### `rettidighed.csv` ###

#### Visning ####
DSB gengiver deres data på følgende måde:

**september 2014**

Målestrækning | Mål for rettidighed | Resultat | Kompensation
--------------|---------------------|----------|-------------
København - Helsingør    | 92.0% | 94,2% | 0,0%
København - CPH Lufthavn | 92.0% | 89,2% | 3,0%
København - Malmø        | 92.0% | 87,2% | 5.0%

I dette projekt er data gengivet på denne facon med henblik på at fjerne redundans og fyld:

Måned | Helsingør | CPH Lufthavn | Malmø
------|-----------|--------------|------
10/14 | 94.2      | 89.2         | 87.2

#### Forklaring ####

DSBs side oplyser tre månedlige værdier for følgende tre strækninger:

* København - Helsingør
* København - CPH Lufthavn
* København - Malmø

Da København går igen i alle tre, er følgende forkortelser anvendt i CSV-filen:

* Helsingør
* CPH Lufthavn
* Malmø

Ud fra hver af de tre strækninger er tre værdier:

* Mål for rettidighed
* Resultat
* Kompensation

**Mål for rettidighed** er en fast værdi på `92%`; formår DSB at komme til tiden 92% af gangene, har de opnået deres mål for rettidighed.

**Resultat** er den faktiske rettidighed for den givne måned. Er den 92% eller over, er togene rettidige; er det lavere, skal pendlere have en kompensation.

**Kompsensation** findes ved differensen mellem rettidighedsmålet og det månedlige resultat. For at tage et eksempel:

* Mål for rettidighed: `92%`
* Septemberresultat på Malmø-strækningen: `87.2%`

`Mål - Resultat = 92% - 87.2% = 4.8%`

Da den beregnede kompensation afrundes til et helt tal, får vi `5%`—værdien, der fremgår af tabellen.

Rettidighedsmålet er et fast tal på 92%, så det undlades i tabellen, og da kompensationen kan beregnes ud fra resultatet (og rettidighedsmålet), udelades kompsensationen også.

Tilbage er det månedlige resultat for hver af de tre strækninger i et [mindre, simplere datasæt][rt].

#### Tabeluddrag ####
Måned | Helsingør | CPH Lufthavn | Malmø
------|-----------|--------------|------
10/14 | 94.2      | 89.2         | 87.2
09/14 | 90.0      | 84.9         | 82.0
08/14 | 90.4      | 81.9         | 77.9
07/14 | 95.8      | 89.8         | 84.9

### `operatoerregularitet.csv` ###
>Følgende tal viser den regularitet DSB Øresund har leveret. Tallene er altså renset for den del, der kan tilskrives udefrakommende faktorer.

Værdien for juli 2013 har en asterisk, forklaret således:

>* DSBØresund tager forbehold for force majeure i juli måned - DSBØresund forventer at tallet korrigeres for dette og tallet er derfor ikke endeligt.

#### Tabeluddrag ####
Måned | Operatørregularitet
------|--------------------
09/14 | 98.5
08/14 | 97.6
07/14 | 97.9

Validering
----------
Begge datafiler er valideret med `csvlint` for at sikre at der er tale om CSV.


[source]: http://dsboresund.dk/rettidighed.asp