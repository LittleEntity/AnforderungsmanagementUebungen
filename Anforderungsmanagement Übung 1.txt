# Anforderungsmanagement Übung 1 #
## Aufgabe 1 ##
Ein Softwaremanager ist an einer Projektentwicklung für ein System beteiligt, das die übersetzung von Softwareanforderungen in eine formelle (beispielsweise UML-basierte) Softwarespezifikation unterstützt. Kommentieren Sie die Vor- und Nachteile folgender Entwicklungsstrategien:

a) Sie entwickeln einen Wegwerfprototypen, werten ihn aus und überprüfen die Systemanforderungen. Anschließend entwickeln Sie das endgültige System mit der Programmiersprache C.
#### Lösung:
#### pro:
+ Schnelle Entwicklung eines Prototypen führt zu schnellen dennoch aussagekräftigen proof of concept
+ Nach der Entwicklung des Prototypen kann entschieden werden, welches weitere Entwicklungs-Konzept sich am besten eignet
+ standardisierter Ablauf -> gute Einschätzbarkeit der Entwicklungslaufzeit

#### contra:
- Wenn Prototyp zu viel Zeit frisst -> kann der Versuch entstehen den Prototypen weiterzuentwickeln, was zu einer schlechten Implementierung führt
- Wenn Verfahren von vorn herein so festgelegt wird, wird die Entwicklung des Endproduktes schwierig, wenn sich nach Usability-Test des Prototypen gravierende Änderungswünsche ergeben
- Programmiersprache C: schwierig qualifiziertes und geschultes Personal zu finden

b) Sie verwenden die bestehenden Anforderungen, um das System in Java zu entwickeln, und modifizieren es anschließend, um es an eventuell geänderte Benutzeranforderungen anzupassen.
### Lösung:
#### pro:
+ Code welcher erhalten bleibt hat von Anfang an hohe Qualität -> keine Funktion wird zwei mal implementiert (vs Prototyp: Mehrfachimplementierung)
+ Wenn wenige und leicht zu implementierende Änderungswünsche folgen, führt dies eventuell zu einem schnelleren Projektabschluss als mit Prototypen Verfahren (unwahrscheinlich)

#### contra:
- schwierige Entwicklung, da stets auf Anpassbarkeit jedes Teilsystems geachtet werden muss, da sich prinzipiell jeder Funktionsbaustein geändert werden kann.
- schlechte Einschätzbarkeit der Entwicklungslaufzeit, da Umfang der Änderungen nicht festgelegt sind
- Code der Aufgrund von Änderungen wieder entfernt wird, hat hohe Qualität -> verschwendete Zeit

c) Sie entwickeln das System inkrementell, wobei der Benutzer in das Entwicklungsteam eingegliedert ist.
### Lösung:
#### pro:
+ wahrscheinlichkeit, dass qualitativ hochwertiger Code erhalten bleibt ist hoch, da jeder Funktionsbaustein direkt nach Entwicklung besprochen wird und eine neue Zielsetzung für die weiteren Entwicklungen festgelegt wird
+ kann zu höherer Benutzerzufriedenheit führen
+ in diesem Fall eignet sich dieses Entwicklungsmodell, da die Entwickler selbst wahrscheinlich mit einem solchen Tool arbeiten wollen. Hier trifft zu Entwickler = Benutzer

#### contra:
- Hohe Verwaltungskosten
- Zwischenmenschliche Konflikte zwischen Kunde und Entwickler
- erfordert viel Zeit vom Benutzer (hier vernachlässigbar da Entwickler = Benutzer)
- schwierig die Projektlaufzeit einzuschätzen, da von vorn herein der Umfang des Projektes nur wage bestimmt ist (wenn überhaupt)

## Aufgabe 2 ##
Finden Sie Mehrdeutigkeiten und Lücken in der folgenden Aufstellung von „Anforderungen“ für einen Teil eines Fahrscheinautomaten. Der Text ist sehr kurz und kann deshalb natürlich nicht alle möglichen Funktionen eines Fahrscheinautomaten beschreiben. Beachten Sei dies bei Ihrer Analyse.

"Ein Fahrscheinautomat verkauft Zugfahrscheine. Benutzer wählen ihr Ziel aus und geben eine Kreditkarte und eine persönliche Geheimnummer ein. Der Fahrschein wird ausgegeben, und vom Konto der Kreditkarte werden die Kosten abgebucht.
Drückt der Benutzer den Startknopf, dann wird neben einem Menü mit möglichen Zielorten eine Nachricht angezeigt, dass der Benutzer den Zielort auswählen soll. Wurde erst einmal ein Ziel ausgewählt, werden die Benutzer dazu aufgefordert, ihre Kreditkarte einzugeben. Deren Gültigkeit wird überprüft, und die Benutzer werden aufgefordert, die persönliche PIN einzugeben. Wenn die Transaktion überprüft ist, wird der Fahrschein ausgegeben."

###Lösung:###
#### Analyse:
- erster Teil
	- Ein Fahrscheinautomat verkauft Zugfahrscheine.
		(zu allgemein; Beschreibt Gesamtfunktionalität in einem Satz und lässt viel zu viele Details was der Automat tun soll ungeklärt)
- zweiter Teil
	- Benutzer wählen ihr Ziel aus
	- geben eine Kreditkarte [...] ein
	- geben [...] eine persönliche Geheimnummer ein
	- Fahrschein wird ausgegeben
	- vom Konto der Kreditkarte werden die Kosten abgebucht
- dritter Teil
	- Startknopf für Benutzer
	- Menü mit möglichen Zielorten 
		(Spezifikation zur Zielauswahl)
	- eine Nachricht [wird] angezeigt, dass der Benutzer den Zielort auswählen soll 
		(Spezifikation zur Zielauswahl)
	- die Benutzer [werden] dazu aufgefordert, ihre Kreditkarte einzugeben 
		(Duplikat/Spezifikation)
	- [Kreditkarten-] Gültigkeit wird überprüft
	- die Benutzer werden aufgefordert, die persönliche PIN einzugeben. 
		(Duplikat)
	- Transaktion überprüf[en]
	- Fahrschein [ausgeben] 
		(Duplikat)

#### Atome:
- Eingabemöglichkeit für Kreditkarten PIN
- Eingabemöglichkeit für Kreditkarten
- Startknopf für Benutzer
- Menü mit möglichen Zielorten
- eine Nachricht [wird neben dem Menü mit Zielorten] angezeigt, dass der Benutzer den Zielort auswählen soll
- die Benutzer [werden] dazu aufgefordert, ihre Kreditkarte einzugeben
- [Kreditkarten-] Gültigkeit wird überprüft
- die Benutzer werden aufgefordert, die persönliche PIN einzugeben.
- vom Konto der Kreditkarte werden die Kosten abgebucht
- Transaktion überprüf[en]
	- (fehlende Spezifikation: Was passiert, wenn Transaktion fehlschlägt?)
- Fahrschein wird ausgegeben

## Aufgabe 3 ##
Sie sollen die Anforderungen an ein neues Bibliothekssystems (das alte System wird durch das neue System abgelöst) an einem Institut erfassen und beschreiben. Das Bibliothekssystem ist eine zentrale Schnittselle zu mehreren Artikeldatenbanken. Es ermöglicht den Benutzern, Kopien von Artikeln herunterzuladen, die in Magazinen, Zeitungen und wissenschaftlichen Zeitschriften veröffentlicht worden sind. Treffen Sie alle weiteren notwendigen Annahmen selbstständig und benennen Sie diese gegebenenfalls.

a) Beschreiben Sie Ihr Vorgehen zur Definition von Anforderungen.
### Lösung:
1. Ist-Zustand erfassen: Altes System analysieren und Benutzer zu folgenden Fragen interviewen:
	- Was hat ihnen am alten System nicht gefallen?
	- Gibt es Verbesserungsvorschläge?
	- Was war im alten System besonders gelungen? Warum? (Merkmale: Zeit, Erklärung, Spaß, Information)
2. Antworten der Benutzer vergleichen und analysieren
	- Unterschiede feststellen und insbesondere auf Widersprüche achten (Widersprüche müssen mit besonderer Vorsicht behandelt werden)
	- Gemeinsamkeiten feststellen und gut dokumentieren (Kern des Systems)
	- Verständnis prüfen, ggf. weitere Interviews bei Verständnisschwierigkeiten durchführen
3. "Papierprototyp" entwickeln und den Benutzern vorstellen
	- auf geeignete Präsentationsform achten
	- auf Änderungswünsche eingehen und ggf. Papierprototyp abändern und erneut vorstellen
		- dabei darauf achten nur die Änderungen vorzustellen
	- Sobald Konsens erreicht wurde muss dieser sehr gut dokumentiert werden
4. Anforderungen festlegen

b) Beschreiben sie in natürlicher Sprache (mindestens 5) Anforderungen, die das neu zu entwickelnde System erfüllen soll.
c) Geben Sie für jede ihrer Anforderungen an, wie diese überprüft werden kann.
### Lösung:
- Die Artikeldatenbank muss über die Oberfläche mittels Filter mit den Kategorien Autor, Mediumtitel, Artikel-Titel und Inhalt/Freitext durchsuchbar sein
	- test der Benutzeroberfläche
- Das System muss eine Vorschaufunktion zur Darstellung der herunterladbaren Dokumente enthalten
	- test der Benutzeroberfläche
- Dem Benutzer soll es möglich sein den Speicherort der heruntergeladenen Kopie zu wählen
	- test der Benutzeroberfläche und Prüfung der Funktion indem Speicher nach Herunterladen geprüft wird
[- Nach einer Suche sollen die Trefferergebnisse links neben der Vorschau des zuerst angewählten Treffer-Ergebnisses angezeigt werden]
Verbesserung:
- Liste der Suchergebnisse mit einer simultanen Detailvorschau versehen
	- test der Benutzeroberfläche
- Rechts oben soll ein Hilfeknopf zur Anleitung des Systems führen
	- test der Benutzeroberfläche
- Bei Systemstart befindet sich ein Menü links in dem Filter zur Suche gesetzt werden können.
	- test der Benutzeroberfläche
- Das Vorschaufenster zeigt zu Systembeginn eine zusammenfassende Bedienungsanleitung des Systems. Die Anleitung sollte mit Schriftgröße 12 der Schrift Times New Roman maximal eine DinA5 Seite umfassen. Die Anleitung darf weniger Text umfassen.
	- Text in Textverarbeitungsprogramm eingeben, das DinA5 unterstützt. Schriftgröße und Schrift auswählen, entsprechend formatieren und gegen die Anforderung prüfen.

d) Legen Sie ein Vorgehensmodell für die Implementierung fest und begründen Sie Ihre Wahl. Erläutern Sie insbesondere, wie Ihre Wahl die Verwaltung von Anforderungen im Prozess beeinflusst. (optional)
### Lösung:
- Für dieses Projekt würde ich ein statisches Entwicklungsmodell bevorzugen (V-Modell oder Wasserfallmodell), da nach Abschluss der Interviews und Vorstellung des Papierprototypen keine weiteren Änderungen zu erwarten sind
- Bibliothekssystem/Suchsystem mit Downloadfunktion wurde bereits mehrfach implementiert und ist in sofern wenig innovativ -> gute Voraussetzungen für statisches Entwicklungsmodell

## Aufgabe 4 ##
In der Vorlesung haben Sie gesehen, dass „Die wirtschaftliche Wirkung von Requirements Engineering ist immer indirekt! Das RE kostet zunächst nur!“

a) Begründen Sie mit Hilfe eines Projektbeispiels, warum diese Aussage korrekt ist.

b) Sie sind Projektleiter in der IT –Abteilung eines Softwarehauses. Stellen Sie sich eine Projektsituation vor, in der Sie die Leitung der IT überzeugen möchten, dass zukünftig mindestens 10% des Gesamtprojektaufwandes für Anforderungsmanagement eingeplant werden muss.
Beschreiben Sie Ihr Vorgehen.

c) Erstellen Sie passend zu Ihrem Vorgehen eine Kurzpräsentation (5 Minuten), mit der Sie die Leitung der IT von Ihrem Vorgehen überzeugen möchten. Das Format, Aussehen, Art, ... der Präsentation ist Ihnen überlassen.