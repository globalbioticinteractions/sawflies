[![Build Status](https://travis-ci.com/globalbioticinteractions/sawflies.svg)](https://travis-ci.com/globalbioticinteractions/sawflies) [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:globalbioticinteractions/sawflies)](http://globalbioticinteractions.org/?accordingTo=globi:globalbioticinteractions/sawflies)

Configuration to help Global Biotic Interactions (GloBI, https://globalbioticinteractions.org) index: 

Andrew J Green. 2020. Larval Foodplants of British and Irish Sawflies. Accessed via https://www.sawflies.org.uk/wp-content/uploads/2019/04/Symphyta-larval-foodplants-latest-version.xlsx on 2020-12-28.

The following steps were taken to help index the data:

1. download https://www.sawflies.org.uk/wp-content/uploads/2019/04/Symphyta-larval-foodplants-latest-version.xlsx
2. convert to UTF-8 encoded CSV using OpenOffice Calc and store results in Symphyta-larval-foodplants-latest-version.csv
3. use [Elton](https://github.com/globalbioticinteractions/elton) to generate schema mapping with ```elton init --data-url file://$PWD/Symphyta-larval-foodplants-latest-version.csv --data-citation "Andrew J Green. 2020. Larval Foodplants of British and Irish Sawflies. Accessed via https://www.sawflies.org.uk/wp-content/uploads/2019/04/Symphyta-larval-foodplants-latest-version.xlsx on 2020-12-28." globalbioticinteractions/sawflies```
4. edit schema mapping in globi.json and apply defaults (e.g., sourceLifeStageName -> larva, interactionTypeName -> eats)
5. run ```elton review``` to inspect the mapping results

