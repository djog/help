# **Merge Confilcts**

Als je tegelijkertijd met iemand anders commit en dezelfde bestanden zijn gewijzigd weet Git niet precies hoe die de bestanden moet samenvoegen (mergen). Dan geeft hij een error en vraagt hij aan jou of jij het wilt oplossen. Je gaat dan alle bestanden bij langs en voegd de veranderingen handmatig samen. 

## **Stap 1:** Kijk welke bestanden een confilct hebben

Gebruik `git status` om te zien welke bestaden merge conflicts hebben.

## **Stap 2:** Los de merge conflicts op

Open de bestanden die een conlict hebben met een editor:

Tussen de `<<<<<<< HEAD` en `=======` zitten de veranderingen die jezelf hebt gedaan.

Tussen de `=======` en `>>>>>>> [commit id]` zitten de veranderingen van de anderen.

Voeg de verschillende stukjes samen en zorg dat alle aanduidingen weg zijn. Als je het bestand daarna weer opslaat dan is de merge-conflict opgelost!

## **Stap 3:** Push de veranderingen

Ook voor het mergen moet je een commit maken en pushen gebruik daarvoor alle stappen die je gebruikt bij het pushen:

1. `git add -A`

2. `git commit -m "Merge conflict opgelost!"`

3. `git push`

*Geschreven door Rijk van Putten (@Rijk-van-Putten)*

*Bevat de tekst nog fouten of wil je dingen toevoegen? Maak dan een commit naar deze repository!*
