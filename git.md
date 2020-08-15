# Hoe gebruik je **Git** en **GitHub/GitLab**?

## Wat is **Git**?

Git is een versiebeheersysteem.

Git houd de wijzigingen van bestanden bij. Git zorgt ervoor dat alle code goed wordt opgeslagen en je nooit een stukje code kwijt kan raken. Je kan precies terugvinden welke code je op welke tijd hebt toegevoegd. Als de code fouten bevat kan je de wijzigingen ongegaan maken.

## Wat zijn **GitLab** en **GitHub**?

GitLab en GitHub zijn websites waarop je een Git repositoroy op wordt gehost. Een repository (vaak afgekort tot "repo") is een locatie waar alle bestanden voor een bepaald project worden opgeslagen. Naast het opslaan van de repository kan je op GitLab en GitHub ook allerlei extra dingen doen zoals issues en projectborden maken om goed als team te kunnen samenwerken!

**Opmerking:** Omdat je GitHub pas mag gebruiken vanaf je 13e,  gebruiken de kinderen t/m 12 jaar GitLab.

**Handige Links:**

- [Prive GitLab van de DJOG](http://51.15.53.32/)

- [GitHub](https://github.com)

- [GitHub - DJOG Organisatie](https://github.com/djog)

## **Clonen:** De repository voor de eerste keer van GitHub/GitLab downloaden

Als je voor de eerste keer aan een Git-project wilt werken moet je eerst de repository downloaden. Dat noemen we **clonen** (klonen).
Daarvoor heb je de link van de GitHub/GitLab nodig.

### **Stap 1:** Vind de website van het project/repository

Om de download-link te kopieeren moet je eerst de website van het Git-project zien te vinden. Vraag aan de teamleden waar die staat of zoek hem zelf op:

- Zoek op de GitLab: [Ga naar de GitLab](http://66e5dd16-d4e9-4183-bb30-cffe48d1d880.pub.cloud.scaleway.com/)

- Zoek op de GitHub: [Ga naar de GitHub](https://github.com/djog)

We zoeken naar de homepagina van een project/repository.

De homepagina van een GitLab project ziet er zo uit:

![GitHub Homepagina](pics\homepage-gitlab.png)

De homepagina van een GitHub repository ziet er zo uit:

![GitHub Homepagina](pics\homepage-github.png)

### **Stap 2:** Kopieer de link van de repository

Als het goed is zie je nu de blauwe of groene 'Clone' knop.
Als je daar op drukt kan je 2 soorten links kopieeren.
Wij gebruiken de HTTPS link.

Druk op het kopieerknopje om de link te kopieeren:
![Link](pics\clone-link-gitlab.png)

(op GitHub ziet het er vergelijkbaar uit)

### **Stap 3:** Voor het clone commando uit

Open eerst de terminal/command promt op die je gebruikt op jouw besteuringssysteem.

Type `git clone` en gebruik dan een van de volgende sneltoetsen om de link te plakken:

- Windows CMD: `CTRL + V`
- Windows Git Bash: `CTRL + SHIFT + INSERT`
- Linux Terminal: `CTRL + SHIFT + V`

`git clone [de link die je gekopieerd hebt hier]`

(Druk daarna op enter om het commando uit te voeren.)

Als het goed is gaat die nu het project downloaden. De output ziet er ongeveer zo uit:
![Clone Output](pics\clone-output.png)

Gefeliciteerd! Je hebt nu het project gecloned!

## **Pullen en Mergen:** Nieuwe veranderingen binnenhalen

Als andere mensen van je team veranderingen hebben gedaan en je die zelf ook wilt krijgen moet je **pullen**. In het Nederlands: trekken. Je trekt de veranderingen naar je toe 😉.

### Pullen

Om te pullen gebruik je het volgende commando:

`git pull`

Als je geen bestanden hebt aangepast werkt het prima en krijg je de nieuwe veranderingen binnen! Heb je wel bestanden aangepast dan krijg je de volgende error:

![Pull error](pics\pull-error.png)

Git zorgt ervoor dat je niet kan pullen omdat je verandereingen dan weg gaan (wat Git natuurlijk ten alle tijde probeerd te voorkomen).

### Mergen

Als je je eigen veranderingen wilt behouden en ze wilt mengen (mergen) met de veranderingen van de anderen maak je eerst een commit: Zie stap 1 en 2 van pushen.
Dus je doet:

1. `git add -A`

2. `git commit -m "[Mijn berichtje hier]"`

**Let op:** Daarna kan je nog NIET pushen (dat geeft een error) maar opnieuw pullen:

`git pull`

Als het goed is gaat Git dan de bestanden mergen. Als je niet dezelfde bestanden op dezelfde plekken hebt aangepast gaat dit goed. Git is zo slim om alle bestanden goed samen te voegen.
Gaat het proces helemaal goed dan hoef je alleen nog maar te pushen:

`git push`

Lukt Git het toch niet dan krijg je een merge-conflict. Zie dan: [merge conflicts](merge-conflicts.md) om die op te lossen.

## **Pushen:** Mijn wijzigingen met de andere delen

Als je iets hebt aangepast wil je natuurlijk je veranderingen met de andere mensen delen.

Dit doe je door een commit te maken.

### Wat is een **commit**?

Nadat je wijzigingen in je code hebt aangebracht, doe je een "commit".

Een commit is een bericht over de wijzigingen die je hebt aangebracht. Een commit bevat een berichtje en de naam van de gebruiker.

Je kan alle commits bekijken op GitLab/GitHub:
![Commit Voorbeeld](pics\commit-example.png)

### **Stap 1:** Voeg bestanden toe aan je commit

Als je aanpassingen/wijzigingen/veranderingen aan het project hebt gemaakt zie je als het goed is in het rood 'modified' (aangepast) staan als je het commando `git status` uitvoerd. Je kan dit commando altijd uitvoeren om de 'status' van de bestanden van je repository te zien.

![](pics\git-status-modified.png)

Om alle gewijzigde bestanden aan je commit toe te voegen gebruik voer je het volgende commando uit:

`git add -a` (Voegt alle bestanden toe aan je commit)

### **Stap 2:**  Een commit berichtje schrijven

Voordat je de commit kan versturen moet je eerst een soort berichtje schrijven dat de andere mensen kunnen lezen om duidelijk te maken wat je nou precies commit. Meestal beschrijf je in een paar woorden wat je precies hebt aangepast of toegevoegd.

Om een commit te doen met een berichtje gebruik je het volgende commando. Belangrijk is dat je het berrichtje tussen aanhalingstekens "" typt:

`git commit -m "[je brerichtje hier]"` (Maakt een commit met een berrichtje)

Voolbeeld: `git commit -m "Ik heb een bug opgelost!"`

### **Stap 3:** **Pushen:** De commit naar de website versturen

Tot en met de vorige stap stond de commit alleen nog maar op je eigen computer. Dat is heel leuk maar je team heeft er niks aan als alleen jij de commits hebt. Om je werk te delen moet je **'pushen'** (letterlijk: duwen) je duwt de bestanden van jezelf af naar de server. Die is in dit geval GitLab of GitHub.

Om te pushen gebruik je het volgende commando:

`git push`

Soms moet je eerst nog inloggen met GitLab of GitHub. Bekijk daarvoor de insturcties hieronder.

## Inloggen met GitLab

Als je voor de eerste keer iets cloned, pushet of pulled van de Jonge Onderzoekers GitLab moet je inloggen met je GitLab gebruikersnaam en wachtwoord. Deze zijn dezelfde als degene die je gebruikt om op de GitLab website in te loggen.

Je krijgt dan een login-venster. Dat ziet er zo uit op Windows:

![GitLab lokale login](pics\gitlab-login.png)

## Inloggen met GitHub

Als je voor de eerste keer iets pushet naar de Jonge Onderzoekers, of een prive repository cloned of pulled moet je inloggen met je GitHub account (zorg ook dat je in de DJOG organisatie zit).

Je krijgt dan een login-venster. Dat ziet er zo uit op Windows:

![](pics\github-login.png)

Log in met je GitHub gebruikersnaam en wachtwoord. Deze zijn hetzelfde als die je gebruikt om op de GitHub website in te loggen.

## **Commit error:** Git weet je gegevens niet

Git heeft een username en emailadres nodig om toe te voegen aan commits. Meestal gaat dit al automatisch als je met GitLab of GitHub bent ingelogd. Maar soms krijg je toch een error. Maak dan gebruik van de volgende commando's om het op te lossen:

`git config --global user.name "[jou username]"`

Je username is je GitLab of GitLab username. (bijv: richelbilderbeek, zonder de @!)

`git config --global user.email [jou email]`

Je email is het emailadres dat je gebruikt voor je GitHub of GitLab account. Je kan die vinden bij de instellingen.

*Geschreven door Rijk van Putten (@Rijk-van-Putten)*

*Bevat de tekst nog fouten of wil je dingen toevoegen? Maak dan een commit naar deze repository!*
