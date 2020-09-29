# Kertlámpa vezérlő 
## A rendszer felépítése
A kertlámpa rendszer nyomógombokból, lámpákból és egy 5 eres kábelből álló rendszer, amelyre csatlakozik egy vezérlő is.
Ez a rendszer a kert különböző pontjain nyomógombok és lámpák elhelyezését teszi lehetővé, amelyek mind erre a "busz"-ra vannak felfűzve. A vezérlő a működési logikához használ 1 db digitális inputot (nyomógomb kontakt) és 1 db digitális outputot (relével kapcsolt 220V).
![Image1](https://github.com/ahinsen/kertlampa/IMG1.jpg)
## A vezérlő működése 
Bármelyik nyomógomb egyszeri megnyomása (és elengedése) hatására a lámpák fel/le kapcsolódnak (vagyis a kimenet állapotot vált). A bekapcsolt állapotból az időzítés (pl. 3 perc) elteltével automatikusan kikapcsol. Bekapcsoláskor a vezérlő érzékeli ha egymás után többször nyomják meg a gombot egymás után. Az időzítés annyiszor 3 perc lesz ahányszor egymás után (pl. 500 ms-on belül) megnyomták a gombot.
## A kontaktok függetlenítése
A nyomógombok párhuzamosan kapcsolt kapcsolók. Ha bármelyik kapcsoló beragad, akkor a rendszer egyik kapcsolóról se működtethető. Ennek elkerülése érdekében a kapcsolók egy passzív RC tagon keresztül kapcsolódnak a kontakt vonalakra, ami a kontaktus létrehozásakor egy tüskét generál (garantálja, hogy a kontaktust a vezérlő csak néhány 10 ms-ig érzékelje, függetlenül attól, hogy a gomb meddig van lenyomva.

