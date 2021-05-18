
# Minesweeper - generátor herného plánu (časť 2)

[difficulty:5]

*Vytvorte jednoduchú reprezentáciu hry míny, ktorú poznáte zo starých Windows-ov.*

![Minesweeper](https://github.com/jan-kandrac-ssnd/zbierka_uloh/blob/main/img/minesweeper.png?raw=true)

Každé políčko (samostatný objekt) má 2 vlastnosti:
1.  **Stav** - skryté, odkryté alebo označené ($$covered$$, $$uncovered$$, $$marked$$ - odporúčam použiť `Enum`)
2.  **Hodnotu** - teda čísla $$0-8$$, alebo mínu

Všetky tieto políčka sa nachádzajú uložené v ďalšej triede. Táto trieda reprezentuje herný plán a umožňuje jeho interakciu s používateľom. V tejto úlohe interakcia s používateľom nie je nutná.

### Úloha

Vašou úlohou je vygenerovať základ herného plánu. Teda na plochu danej výšky (@@h@@) a šírky(@@w@@) umiestniť určené množstvo mín (@@count@@) a čísel, ktoré určujú, koľko mín sa v ich okolí nachádza. Vykreslite takto vygenerovaný hrací plán na štandardný výstup podľa nasledujúceho príkladu:

```
112X101X101X1000
2X32201110111000
X33X100000000000
3X21111100011100
X21001X21001X100
1100012X10012210
0000012210013X20
000012X21002XX20
01111X3X1013X421
01X22222222X33X1
0112X212X2X23X31
111223X212112X20
2X32X22221101110
3XX2122X2X332100
X32212X222XXX100
1101X211013X3100
```

### Vstupy

Riadok 1: 3 čísla oddelené medzerou

@@w@@ - šírka hracej plochy

@@h@@ - výška hracej plochy

@@count@@ - počet náhodne umiestnených mín, ktoré sa na hracej ploche majú nachádzať

### Výstupy

@@h@@ riadkov obsahujúcich @@w@@ znakov. Na mieste míny vypíšte znak $$X$$ na ostatných miestach vypíšte znak $$.$$

