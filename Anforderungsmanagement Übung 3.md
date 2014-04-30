# Anforderungsmanagement Übung 3 #
## Aufgabe 1 (Aufgaben 2 und 3 aus Übungsblatt 2)##

## Aufgabe 2 ##
Aus Übung 1 Aufgabe 2 kennen Sie folgende grobe Beschreibung eines Fahrscheinautomaten:
"Ein Fahrscheinautomat verkauft Zugfahrscheine. Benutzer wählen ihr Ziel aus und geben eine Kreditkarte und eine persönliche Geheimnummer ein. Der Fahrschein wird ausgegeben, und vom Konto der Kreditkarte werden die Kosten abgebucht. Drückt der Benutzer den Startknopf, dann wird neben einem Menü mit möglichen Zielorten eine Nachricht angezeigt, dass der Benutzer den Zielort auswählen soll. Wurde erst einmal ein Ziel ausgewählt, werden die Benutzer dazu aufgefordert, ihre Kreditkarte einzugeben. Deren Gültigkeit wird überprüft, und die Benutzer werden aufgefordert, die persönliche PIN einzugeben. Wenn die Transaktion überprüft ist, wird der Fahrschein ausgegeben."

a. Identifizieren Sie alle im System „Fahrscheinautomat“ beteiligten (Teil-)Systeme.

Hardware:
- Möglichkeit 1:
	- Startknopf
	- PIN-Eingabepad
	- Zielauswahlknöpfe
	- Ausgabebildschirm
- Möglichkeit 2:
	- Touchscreen zur Ein- und Ausgabe
- Kreditkarteneingabeslot

Software:
- Konfigurationsschnittstelle zur Eingabe des Standorts und der möglichen Zielorte mit entsprechenden Ticketpreisen
- Begrüßung und Anleitung
- Zielauswahlmenü
- Kreditkartenannahme und PIN-Prüfung
- Kreditkarten-Finanztransaktion

b. Erstellen Sie ein Kontextdiagramm (beschreibt das eigentliche System im Zentrum und alle über Schnittstellen beteiligten weiteren Systeme bzw. Teilsysteme im Umfeld, siehe auch http://de.wikipedia.org/wiki/Kontextdiagramm für eine Kurzerläuterung) des Fahrscheinautomaten.
Hinweis: Bei dieser Aufgabe müssen Sie festlegen, welche Systeme (Teilsysteme) aus Ihrer Sicht zum Fahrscheinautomaten gehören und welche nicht. Dazu müssen Sie zunächst das System in passende Teilsysteme unterteilen. Bei Verwendung eines UML Use Case Diagramms können sie den Kontext mit einfachen Rechtecken kennzeichnen ( siehe auch http://de.wikipedia.org/wiki/Anwendungsfalldiagramm)

c. Spezifizieren Sie ein Sequenzdiagramm der Aktionen, die bei dem Fahrscheinautomaten beim Kaufvorgang ausgeführt werden. Sie können jede sinnvolle Voraussetzung für das System annehmen. Benutzen Sie u.a. ihre durchgeführte Analyse aus Übung 1 Aufgabe 2 für die Spezifikation des Sequenzdiagramms, um gefundene Mehrdeutigkeiten und Lücken zu beseitigen.


