# SOČ 2016 - Nadstavbová deska pro robota Pololu 3pi
**Autor:** Petr Bobčík

Vítejte v příloze mé práce Nadstavbová deska pro robota Pololu 3pi

#### V této příloze naleznete: 
1) Dokumenty
1) Eagle
1) Obhajoba
1) Použité obrázky
1) SolidWorks

#### Podrobnější obsah jednotlivých složek:
1) Přehled projektu s grafm pro IR senzor, obrázek s konceptem zapojení a tabulku potřebných součástek na pájení.
2) Finální verze desky a schéma k ní v programu Eagle + schéma s deskou k nárazovému senzoru.
3) Text samotné sočky a prezentaci k ní.
4) Veškeré obrázky použity jak v prezentaci, tak v textové práci.
5) Kompletní 3D model robota Pololu 3pi s přídavným shieldem.
									

## Cíl práce
<p>Cílem této práce byl návrh nadstavbové desky (shieldu) pro robota Pololu 3pi. Konstrukce robota je od výrobce optimalizována
na soutěžní disciplínu „sledování čáry“, kde robot dosahuje výborných výsledků a nemá mezi komerčně dostupnými produkty konkurenci. Ovšem při složitější variantě této disciplíny “najdi čáru“, konající se na Robotickém dni v Praze, kde dráha obsahuje rozpojky, odbočky, nebo překážky, není možné s ním závodit. Můj shield může posloužit, kromě možné účasti na soutěžích, také ve výuce. V ní si student může
robota sám naprogramovat. Přidáním funkcí a senzorů bude robot univerzálnější než doposud.</p>

![Robot Pololu 3pi](Pou%C5%BEit%C3%A9%20obr%C3%A1zky/C%C3%ADl%20pr%C3%A1ce.png)

<p>Práce řeší rozšíření možností využití robota Pololu 3pi návrhem nadstavby s doplňkovými funkcemi.
Přidané funkce umožňují robotovi snímat podněty ze svého okolí. Další navrženou částí je nárazník pro ochranu před mechanickým poškozením, ke kterému v praxi velmi často dochází. Tyto nárazy způsobovli nefunkčnost senzorů odrazivosti nebo dokonce i jejich odlomení od desky.</p>

Můj přídavný shield je také pinově kompatibilní s bastlířskými deskami, jako je **Arduino Uno**, **FRDM-KL25Z**, **FRDM-KL46Z** a **FRDM-K64F**. Je tedy možné a plánované, že pro přidání dalších funkcí, které můj shield neobsahuje, je možné připevnit jednu ze zmíněných desek, nebo desku, která má shodný pinout. Mikrokontroler, ATmega328P, který je na základním modelu robota se využívá jako MCU pro motory a hlavní řídící mikrokontroler je AVR XMEGu A1, který se nachází na mém shieldu. Ten mi poskytuje velký počet pinů s potřebnými periferiemi. 

## Jaké funkce jsou prostřednictvím shieldu přidány?
<p>Tato práce přidává robotovi Pololu 3pi schopnost detekovat překážku pomocí IR senzorů, kterých je na shieldu celkem 8 po 45° nebo pomocí nárazového senzoru, upevněného na mnou navržený nárazník. Dále také k orientaci v prostoru je přidáno IMU (inerciální pohybová jednotka), která obsahuje gyroskop, magnetometr a akcelerometr v jednom pouzdře. Posledním senzorem je enkodér, pomocí kterého můžeme měřit ujetou vzdálenost, zajišťuje přesnější otáčení okolo osi a umožňuje také měřit rychlost.</p><p>Na desce je přidán také chip pro nabíjení baterií, takže není zapotřebí vytahovat tužkové baterie, které se na základní verzi robota nacházejí. Pouzdra s tužkovými bateriemi je tedy možné vytáhnout a tím snížit váhu. Shield také obsahuje obvod pro měření baterie a to jak napětí, tak proudu. Tímto měřením je možné hlídat úroveň nabití baterie nebo dokonce detekovat, zda baterie není poškozená.</p>

## Co je vlastě Pololu 3pi? ![Robot Pololu 3pi](Pou%C5%BEit%C3%A9%20obr%C3%A1zky/Pololu%203pi.png)
<p>Je to velmi rychlý komerčně dostupný soutěžní robot, určený na disciplínu s názvem sledování čáry, která je v České republice velmi populární (tato disciplína je více popsaná níže). Jeho průměr je 95 mm (odtud dostal název 3pi) a hmotnost 83 g (bez baterií). Jeho rychlost se pohybuje okolo 1m/s. Hlavním mozkem celého robota je mikrokontrolér ATmega328P, který se nachází například u Arduino Nano. Tento robot je vhodný pro začínající programátory, kteří se chtějí od začátečních robotů, jako například legových ze stavebnice Mindstorm, posunout o kousek dále a chtějí se naučit programovací.</p>


## Sledování čáry
</p>Úkolem robota je, aby následoval černou čářu, která se pod ním nachází. Nejprve šlo jen o jízdu po čáře, ale v poslední době se zmíněná disciplína výrazně ztížila, přidáním rozdvojení, křižovatky, přerušení a překážky. Pololu 3pi nedokáže tyto nové prvky řešit, a proto jsem se rozhodl přidat potřebné funkce, které to zajistí.<p>

![Pololu 3pi s mým shieldem](https://github.com/RoboticsBrno/SO-2016-Nadstavbov-deska-pro-robota-Pololu-3pi/blob/master/Pou%C5%BEit%C3%A9%20obr%C3%A1zky/3D%20blokov%C3%A9%20sch%C3%A9ma%20s%20popisky.png)
#### [Více informací naleznete na stránkách Robotárny k mojí SOČ](https://www.robotikabrno.cz/robotarna/projekty-a-socky/soc-2017-petr-bobcik-nadstavbova-deska-pro-robota-pololu-3pi). 

Tato práce byla vypracována společně s [Robotárnou](www.robotarna.cz) a [SPŠ a VOŠ Sokolská Brno](www.spssbrno.cz).
