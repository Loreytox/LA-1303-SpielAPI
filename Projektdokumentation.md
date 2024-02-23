# LA-1303-SpielAPI

# Projekt-Dokumentation

Marek, Cyril, Dorian, Lorenzo

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
| 19.01.2024  | 0.0.1 | Heute haben wir mit dem Backend des Projektes angefangen und konnten schnell vorwärts kommen. Wir haben die Technologie Visual Studio Code benutzt. |
| 26.01.2024  | 0.0.2 | An diesem Tag haben wir uns mit Backend beschäftigt. Wir haben schon ein paar funkionalitäten hinzufügen können und haben auch mit Frontend angefangen. |
| 02.02.2024  | 0.0.3   |  Heute haben wir eine Datenbank mit hilf des NuGet Pakets "Microsoft.EntityFrameworkCore.SqlServer" erstellt. |
|  |  |  |
|  |  |  |

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

### 1.3 Testfälle

| TC-№ | Ausgangslage | Eingabe | Erwartete Ausgabe |
| ---- | ------------ | ------- | ----------------- |
| 1.1  | Die Webseite ist einsatzbereit | "drückt ein Knopf" | Schere, Stein, Papier öffnet sich |
| 2.1  | Die Webseite ist einsatzbereit | "drückt ein Knopf" | Roulette öffnet sich |
| 3.1  | Die Webseite ist einsatzbereit |  -  |  "Zwei Knöpfe sind sichtbar"  |
| 4.1  | Schere, Stein, Papier ist geöffnet | "AI macht eine Bewegung" | Spieler ist daran |
| 4.2  | Schere, Stein, Papier ist geöffnet | "Spieler macht eine Bewegung" | AI ist daran |
| 5.1  | Schere, Stein, Papier oder Roulette ist geöffnet und Spieler hat verloren/ kein Geld mehr | "Weiterspielen Option wird gewählt" | Spieler kann weiterspielen |
| 5.2  | Schere, Stein, Papier oder Roulette ist geöffnet und Spieler hat verloren/ kein Geld mehr | "Spiel verlassen Option wird gewählt" | Spieler kommt zurück ins Menu |
| 6.1  | Roulette ist offen | "Spieler wählt die Wetten Option und entscheidet sich für eine Menge an Geld" | Spieler hat gewettet |
| 6.2  | Roulette ist offen | "Spieler wählt die Wetten Option und entscheidet sich für eine Menge an Geld, aber die Menge ist grösser als was man hat" | Spieler bekommt eine Warnung |
| 7.1  | Roulette ist offen | "Spieler wählt eine Farbe zwischen Schwarz, Rot und Grün" | Spieler kann jetzt wetten |
| 7.2  | Roulette ist offen | "Spieler wählt ein Zahl" | Spieler kann jetzt wetten |

✍️ Die Nummer hat das Format `N.m`, wobei `N` die Nummer der User Story ist, die der Testfall abdeckt, und `m` von `1` an nach oben gezählt. Beispiel: Der dritte Testfall, der die zweite User Story abdeckt, hat also die Nummer `2.3`.

### 1.4 Diagramme

✍️ Hier können Sie PAPs, Use Case- und Gantt-Diagramme oder Ähnliches einfügen.

## 2 Planen

| AP-№ | Frist | Zuständig | Beschreibung | geplante Zeit |
| ---- | ----- | --------- | ------------ | ------------- |
| 1.A | 19.01.2024 | Lorenzo | Informieren wie man mit Backend ein Schere, Stein, Papier Spiel machen könnte. | 10' |
| 1.B | 19.01.-02.02.2024 | Marek, Cyril | Erstellen eines S., S., P. Spiel | 325' |
| 2.A | 19.01.2024 | Lorenzo | Informieren wie man mit Backend ein Roulet machen könnte. | 10' |
| 2.B | 19.01.-02.02.2024 | Marek, Dorian | Erstellen eines auf Backend basierendes Roulette | 325' |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

Total: 

✍️ Die Nummer hat das Format `N.m`, wobei `N` die Nummer der User Story ist, auf die sich das Arbeitspaket bezieht, und `m` von `A` an nach oben buchstabiert. Beispiel: Das dritte Arbeitspaket, das die zweite User Story betrifft, hat also die Nummer `2.C`.

✍️ Ein Arbeitspaket sollte etwa 45' für eine Person in Anspruch nehmen. Die totale Anzahl Arbeitspakete sollte etwa Folgendem entsprechen: `Anzahl R-Sitzungen` ╳ `Anzahl Gruppenmitglieder` ╳ `4`. Wenn Sie also zu dritt an einem Projekt arbeiten, für welches zwei R-Sitzungen geplant sind, sollten Sie auf `2` ╳ `3` ╳`4` = `24` Arbeitspakete kommen. Sollten Sie merken, dass Sie hier nicht genügend Arbeitspakte haben, denken Sie sich weitere "Kann"-User Stories für Kapitel 1.2 aus.

## 3 Entscheiden

✍️ Dokumentieren Sie hier Ihre Entscheidungen und Annahmen, die Sie im Bezug auf Ihre User Stories und die Implementierung getroffen haben.

## 4 Realisieren

| AP-№ | Datum | Zuständig | geplante Zeit | tatsächliche Zeit |
| ---- | ----- | --------- | ------------- | ----------------- |
| 1.A  |       |           |               |                   |
| ...  |       |           |               |                   |

✍️ Tragen Sie jedes Mal, wenn Sie ein Arbeitspaket abschließen, hier ein, wie lang Sie effektiv dafür hatten.

## 5 Kontrollieren

### 5.1 Testprotokoll

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

### 5.2 Exploratives Testen

| BR-№ | Ausgangslage | Eingabe | Erwartete Ausgabe | Tatsächliche Ausgabe |
| ---- | ------------ | ------- | ----------------- | -------------------- |
| I    |              |         |                   |                      |
| ...  |              |         |                   |                      |

✍️ Verwenden Sie römische Ziffern für Ihre Bug Reports, also I, II, III, IV etc.

## 6 Auswerten

✍️ Fügen Sie hier eine Verknüpfung zu Ihrem Lern-Bericht ein.
