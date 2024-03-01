# LA-1303-SpielAPI

# Projekt-Dokumentation

Marek, Cyril, Dorian, Lorenzo

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
| 19.01.2024 | 0.0.1 | Heute haben wir mit dem Backend des Projektes angefangen und konnten schnell vorwärts kommen. Wir haben die Technologie Visual Studio Code benutzt. |
| 26.01.2024 | 0.0.2 | An diesem Tag haben wir uns mit Backend beschäftigt. Wir haben schon ein paar funkionalitäten hinzufügen können und haben auch mit Frontend angefangen. |
| 02.02.2024 | 0.0.3   |  Heute haben wir eine Datenbank mit hilf des NuGet Pakets "Microsoft.EntityFrameworkCore.SqlServer" erstellt. |
| 23.02.2024 | 0.1.0 | Wir konnten heute das Backend fertig programmieren und haben damit begonnen, das Frontend zu erstellen und zu containerisieren. |
| 01.03.2024 | 1.0.0 | Wir sind mit Backend und Frontend fertig, jedoch konnten wir unser projekt nicht containerisieren, obwohl wir noch Lehrpersonen um Hilfe gebetet haben. |

## 1 Informieren

### 1.1 Ihr Projekt

Wir werden auf Visual Studio Code eine Spieleapi mit Schere, Stein, Papier und Roulette programmieren. 

### 1.2 User Stories

| US-№ | Verbindlichkeit | Typ  | Beschreibung                       |
| ---- | --------------- | ---- | ---------------------------------- |
| 1 |  Muss  | Funktional | Als Benutzer möchte ich die Möglichkeit haben, Schere, Stein, Papier spielen zu können. |
| 2 |  Muss  | Funktional | Als Benutzer möchte ich die Möglichkeit haben, Roulette zu spielen. |
| 3 |  Muss  | Funktional | Als Benutzer möchte ich die Wahl haben, um entscheiden zu können, welchen Spiel ich zu erst spielen möchte. |
| 4 |  Muss  | Funktional | Als Benutzer möchte ich, dass der Spieler in Schere, Stein, Papier sich immer abwechselt, nachdem man eine Bewegung gemacht hat. |
| 5 |  Muss  | Funktional | Als Benutzer möchte ich die Möglichkeit haben, nachdem ich gewonnen oder verloren habe, weiterzuspielen. |
| 6 |  Muss  | Funktional | Als Benutzer möchte ich die Möglichkeit haben, bei Roulette eine bestimmte Menge von Geld zu verwetten. |
| 7 |  Muss  | Funktional | Als Benutzer möchte ich die Möglichkeit haben, auf alle drei Farben einzugehen und ein Zahl wählen. |
| 8 |  Kann  | Erweiterung | Als Benutzer möchte ich ein sauberes und funktionales Frontend sehen. | 

### 1.3 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  | Die Webseite ist einsatzbereit | "drückt ein Knopf" | Schere, Stein, Papier öffnet sich |
| 2.1  | Die Webseite ist einsatzbereit | "drückt ein Knopf" | Roulette öffnet sich |
| 3.1  | Die Webseite ist einsatzbereit |  -  |  "Zwei Knöpfe sind sichtbar"  |
| 4.1  | Schere, Stein, Papier ist geöffnet | "AI macht eine Bewegung" | Spieler hat gewonnen-/ verloren |
| 4.2  | Schere, Stein, Papier ist geöffnet | "Spieler macht eine Bewegung" | AI hat gewonnen-/ verloren |
| 5.1  | Schere, Stein, Papier oder Roulette ist geöffnet und Spieler hat verloren/ kein Geld mehr | "Weiterspielen Option wird gewählt" | Spieler kann weiterspielen |
| 5.2  | Schere, Stein, Papier oder Roulette ist geöffnet und Spieler hat verloren/ kein Geld mehr | "Spiel verlassen Option wird gewählt" | Spieler kommt zurück ins Menu |
| 6.1  | Roulette ist offen | "Spieler wählt die Wetten Option und entscheidet sich für eine Menge an Geld" | Spieler hat gewettet |
| 6.2  | Roulette ist offen | "Spieler wählt die Wetten Option und entscheidet sich für eine Menge an Geld, aber die Menge ist grösser als was man hat" | Spieler bekommt eine Warnung |
| 7.1  | Roulette ist offen | "Spieler wählt eine Farbe zwischen Schwarz, Rot und Grün" | Spieler kann jetzt wetten |
| 7.2  | Roulette ist offen | "Spieler wählt ein Zahl" | Spieler kann jetzt wetten |

### 1.4 Diagramme

![image](https://github.com/Loreytox/LA-1303-SpielAPI/assets/110893594/e95ba9a0-2259-4e58-a01a-7901c35d7fe5)

![image](https://github.com/Loreytox/LA-1303-SpielAPI/assets/110893594/cef6c4f6-8bbd-44ec-9cd3-6edd6189e52e)

## 2 Planen

| AP-№ | Frist | Zuständig | Beschreibung | geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 1.A | 19.01.2024 | Lorenzo | Informieren wie man mit Backend ein Schere, Stein, Papier Spiel machen könnte. | 10' |
| 1.B | 19.01.-02.02.2024 | Marek, Cyril | Erstellen eines S., S., P. Spiel | 325' |
| 2.A | 26.01.2024 | Lorenzo | Informieren wie man mit Backend ein Roulette machen könnte. | 10' |
| 2.B | 26.01.-02.02.2024 | Marek, Dorian | Erstellen eines auf Backend basierendes Roulette | 325' |
| 3.A | 26.01.2024 | Cyril | Erstellen einer Auswahl welche Spiele man spielen will. | 30' |
| 4.A | 26.01.2024 | Dorian | Erstellen eines Mechanismus, welcher die Spieler abwechselt. | 20' |
| 5.A | 26,01.2024 | Lorenzo, Marek | Implementation des "Weiter spielen" Funktion. | 30' |
| 6.A | 23.02.2024 | Marek | Spieler kann Geld wetten, verlieren oder gewinnen. | 45' |
| 7.A | 23.02.2024 | Marek, Cyril | Spieler kann auf bestimmte Zahlen, Farben oder Sektoren wetten. | 45' |
| 8.A | 23.02.2024 | Cyril | Informieren über Roulette, recherchieren von Methoden. | 40' |
| 8.B | 23.02.2024 - 01.03.2024 | Cyril, Dorian | Implementierung eines funktionfähigen Frontends. | 240' |

## 3 Entscheiden

Wir haben uns für diese User Stories entschieden, weil wir ein Spiel erstellen wollten. Wir haben zwei verschiedene Spiele kreiert: Schere, Stein, Papier und Roulette. Wir haben die wichtigsten Funktionen für jedes Spiel definiert, wie zum Beispiel die Möglichkeit, eine Bewegung oder eine Wette zu wählen, das Ergebnis zu sehen und weiterzuspielen. Wir haben auch darauf geachtet, dass die User die Freiheit haben, zu entscheiden, welches Spiel sie zuerst spielen möchten. Wir haben die User Stories nach ihrer Priorität geordnet, wobei die Muss-Stories die grundlegenden Anforderungen sind, die wir erfüllen müssen, und die Kann-Stories die zusätzlichen Features sind, die wir implementieren können, wenn wir genug Zeit haben

## 4 Realisieren

| AP-№ | Datum | Zuständig | geplante Zeit | tatsächliche Zeit |
| ---- | ----- | --------- | ------------- | ----------------- |
| 1.A | 19.01.2024 | Lorenzo | 10' | 25' |
| 1.B | 19.01.-02.02.2024 | Marek, Cyril | 325' | 325' |
| 2.A | 26.01.2024 | Lorenzo | 10' | 30' |
| 2.B | 26.01.-02.02.2024 | Marek, Dorian | 325' | 325' |
| 3.A | 26.01.2024 | Cyril | 30' | 40' |
| 4.A | 26.01.2024 | Dorian | 20' | 15' |
| 5.A | 26,01.2024 | Lorenzo, Marek | 30' | 30' |
| 6.A | 23.02.2024 | Marek | 45' | 45' |
| 7.A | 23.02.2024 | Marek, Cyril | 45' | 60' |
| 8.A | 23.02.2024 | Cyril | 40' |60' |
| 8.B | 23.02.2024 - 01.03.2024 | Cyril, Dorian | 240' | 300' |

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  | 02.02.2024 | NOK | Dorian, Cyril |
| 2.1  | 02.02.2024 | NOK | Dorian, Cyril |
| 3.1  | 02.02.2024 | NOK | Dorian, Cyril |
| 4.1  | 02.02.2024 | OK | Dorian |
| 4.2  | 02.02.2024 | OK | Dorian |
| 5.1  | 23.02.2024 | NOK | Lorenzo, Cyril |
| 5.2  | 23.02.2024 | NOK | Lorenzo, Cyril | 
| 6.1  | 23.02.2024 | OK | Lorenzo |
| 6.2  | 23.02.2024 | OK | Lorenzo |
| 7.1  | 23.02.2024 | OK | Lorenzo |
| 7.2  | 23.02.2024 | OK | Lorenzo |

Wir haben es nicht geschafft, das Programm zu containerisieren, und konnten daher kein Frontend implementieren. Daher kann Roulette derzeit nur über Swagger verwendet werden, und Schere, Stein, Papier funktioniert nur lokal.

// Wir haben Herrn Thut um Hilfe gebeten, da wir zuvor Docker mit ihm verwendet haben, aber auch er konnte unser Problem nicht lösen.

## 6 Auswerten

Was wir gut gemacht haben:
- Teamarbeit
- Programmierung nach IPERKA
- Erstellung von Diagrammen und Internetrecherche
- Jeder hat zumindest ein wenig programmiert
  
Was wir nicht gut gemacht haben:
- Das Frontend hat viel Zeit in Anspruch genommen
- Die Implementierung eines Frontends wurde unterschätzt
- Wir konnten nicht erfolgreich mit Docker arbeiten, obwohl wir wussten, wie es ging.
