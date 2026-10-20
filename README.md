# Git & GitHub – Individuell examination

## Fråga 1: Versionshantering vs vanliga filer

Versionshantering är ett arbetssätt där vi kontinuerligt sparar ögonblicksbilder av vår utveckling i projektet, så att vi kan rulla tillbaka till en tidigare version. När vi sparar med Ctrl + S i kodeditorn skriver vi över filen, men skapar inte samma historik som Git gör, där vi kan gå tillbaka och se hur projektet såg ut för flera dagar eller veckor sedan.

Gits tidslinje av frysta ögonblicksbilder innebär att vi gör commits som sparar det vi har stageat vid just det tillfället, så att vi sedan kan återgå till de stunderna i projektets historia. Att alla tre TODO fortfarande syns i den första commiten på GitHub visar att tidigare commits inte påverkas av framtida arbete, utan ligger kvar som tidskapslar, frysta i tiden.

---

## Fråga 2: Arbetsytan, Staging och Commits

`git status` ger en rapport om arbetsytan och staging area, så vi kan se om det är något som ligger "i luften" och inte har blivit committat än.

Med `git add` väljer vi vilka filer vi vill lägga i staging area från arbetsytan, ungefär som att lägga dem i ett kuvert inför nästa commit.

`git commit` förseglar det vi har lagt i staging area med ett tydligt meddelande om vad vi har gjort, och sparar det som en punkt i projektets historik som vi kan gå tillbaka till.

Om vi bara har sparat filerna i editorn och försöker committa utan att ha lagt ändringarna i staging area får vi `no changes added to commit`, eftersom det inte finns några nya stageade ändringar att committa.

---

## Fråga 3: Lådan hemma vs Montern på GitHub

Mappen på din dator finns lokalt på den maskinen, medan repot på GitHub är online och går att nå från andra datorer. Vi använder `git push` för att pusha våra lokala commits till vårt GitHub-repo.

Git svarar `Everything up-to-date` eftersom det inte finns några nya lokala commits att skicka när commithistoriken redan är densamma på datorn och GitHub. Våra ändrade filer i arbetsytan räcker alltså inte för att pushas, utan ändringarna behöver först gå genom staging area och sparas i en commit.
