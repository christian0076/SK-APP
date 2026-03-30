Stockkarten Anforderung

Header:
1. Betriebsjahr
2. Volk: text 30
3. Standmaß: Zander / Miniplus / Zadant / Dadant / Apidea (die Liste muss erweiterbar sein und auch die Reihnefolge muss der Imker bestimmen können damit er das schnell aussuchen kann.)
4. Königin:
4.1. Jahr: int 2020 ... 3000
4.2. optional Ziffer: int 0 ... 1000
4.3. Mutter Zuchtbuch Nr.: text 30
4.4. Vatervölker Zuchtbuch Nr.: text 30
4.5. Rasse: Buckfast / Carnica / unbekannt (die Liste muss erweiterbar sein)
5. Honigleistung in kg vorjahr: (automatisches Feld und zeigt wert vom letzten Jahr an default 0)
6. Honigleistung in kg heuer: (automatisches Feld berechnet aus der Summe der entnommen kg aus dem wiederholteil)

Wiederholteil:
0. Datum: Datum vom Tag (kann aber ggf. angepasst werden)
1. Allgemeiner Befund
1.1. Belegte Waben: integer 1 ... 1000
1.2. Brut
1.2.1. Weiselzellen: 0 ... 500
1.2.2. Ei: 1 , 2 ,3 ,4
1.2.3. offene: 1, 2, 3, 4
1.2.4. verdeckelte: 1, 2, 3, 4
1.3. Futter: 1, 2, 3, 4
1.4. Wabensitz: 1, 2, 3, 4
1.5. Sanftmut: 1, 2, 3, 4
2. hinzugefüg + / entnommen -
2.1. Räume: int -100...100
2.2. Mittelwände: int -1000 ... 1000
2.3. Drohnenrahmen: int -10 ... 10
2.4. Brut: int -100 ... 100
2.5. Bienen in kg: festkommawert -10 ... 10 mit 2 Komastellen (2,55 kg)
2.6. Honig: festkommawert -200 ... 200 mit 2 Kommastellen (naja man wird wenig hinzugeben) nur wenn man die Honigräume zurückbringt
2.7. Zucker / Sirup: festkommawert -50 ... 50 mit 2 Kommastellen
3. Kommentarfeld: text feld mit 5000 zeichen (tbc für dei 5000 Zeichen)



Erklärung zu:
1 = gering bis fehlend
2 = mäßig
3 = viel (befriedigend)
4 = sehr viel (gut)