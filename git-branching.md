# **Git Branching** - Concept

Om beter samen te werken met Git gebruiken we het Git Branching systeem. Dat systeem zorgt ervoor dat we allemaal onze eigen versie van het project hebben, onze eigen branch. Die we vervolgens kunnen mengen (mergen) met de andere branches.

**Opmerking:** Dit document is nog niet helemaal af! Er zijn nog extra onderwerpen en dingen die ontbreken die hier aan moeten worden toegevoegd. Dit is nog een conceptversie met een snelle notitie hoe je een develop branch gebruikt.

## Merge develop in jouw branch

Merge het werk van de andere met jouw werk. Doe dit altijd eerst voordat je jouw werk weer met de andere deelt.

Update develop eerst:

`git checkout develop`

`git pull`

Merge het dan met jouw branch:

`git checkout rijk`

`git merge develop`

`git push`

Je kan merge conflicts krijgen! Zie daarvoor [merge conflicts](merge-conflicts.md).

## Merge jouw branch in develop

**Let op:** :warning: Dit mogen alleen de ervaren programmeurs doen!

Zorg eerst dat jouw branch up-to-date met develop is. Zie daarvoor het kopje hierboven.

Ga dan naar develop:

`git checkout develop`

`git pull` (Dit zou niks moeten doen!)

Merge dan jouw branch in develop:

`git merge rijk`

`git push`


*Geschreven door Rijk van Putten (@Rijk-van-Putten)*

*Bevat de tekst nog fouten of wil je dingen toevoegen? Maak dan een commit naar deze repository!*
