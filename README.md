# Pruefungsaufgabe-2
Prüfungsaufgabe 2
# Logistic-Regression
Prüfungsaufgabe 2 - Zweiter Teil

Um dieses Projekt zu starten, folgen Sie dem Binder Badge:      [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/FelixWuensch/Pruefungsaufgabe-2/HEAD)

# Ausführung der Übungsaufgabe

!!! Alle Befehle werden ausgeführt in dem die Zeile ausgewählt wird und anschließend mit Shift (Großschreibtaste) und Enter gestartet wird !!!

1. Im ersten Schritt müssen alle benötigten Libraries installiert und importiert werden, so dass im Folgenden alle Befehle erfolgreich ausgeführt werden können.
2. Danach werden die Funktionen my_logger und my_timer implementiert.
3. Danach werden unsere Daten im CSV Format eingelesen.
4. Daraufhin werden die Daten erst einmal begutachtet. Zunächst die ersten fünf Zeilen des Datensatzes (.head()), dann die Datentypen des Datensatzes (.info()) und zu guter Letzt noch einmal die ersten Statistiken der Daten (.describe()).
5. Dann gehen wir über und untersuchen die Daten. Dazu erstellen wir zunächst ein Histogramm, welches die Altersverteilung in diesem Datensatz zeigt.
6. Im fünften Schritt wird ein Jointplot erstellt, welches das Alter (X-Ache) und das Area Income (Y-Achse) gegenüberstellt. Daraus lässt sich ablesen, wie viel jeder Kunde abhängig von seinem Alter verdient.
7. Beim nächsten Jointplot wird über das Alter (X-Achse) und die Daily Time Spent on Site (Y-Achse) aufgezeigt, welche Personengruppen abhängig vom Alter, wie viel Zeit auf der Seite verbringen. Dies ist diesmal nicht in Punkten sondern in Regionen aufgezeigt. Die innersten Kreise zeigen die intensivste Nutzung.
8. Als Nächstes wird dann wieder in einem Jointplot die Daily Time on Site (X-Achse) und die Daily Internet Usage (Y-Achse) betrachtet. Daraus lässt sich dann ablesen, wie viel Zeit die Personen auf der Internetseite verbringen in Relation zu ihrer gesamten Internetnutzungszeit.
9. Zu guter Letzt wird noch mit einem Pairplot, anhand aller Kriterien in Relation zueinander gesetzt gezeigt, wer auf die Werbung geklickt hat und wer nicht. Damit endet dann auch die explorative Datenanalyse.
10. Dann geht es über zur logistischen Regression. Hierbei wird zunächst die SKLearn Library importiert. Danach werden die Daten in X-Daten und Y-Daten aufgeteilt. Im Folgenden werden dann die X-Daten wiederum aufgeteilt in Test- und Trainingsdaten, ebenso passiert das gleiche mit den Y-Daten.
11. Damit werden noch die Wichtigen Klassen für die Logistische Regression, den Classification Report und die Confusion Matrix importiert. Ebenso wird gleich eine Instanz einer Logistischen Regression erstellt. 
12. Daraufhin folgen die Funktionen für das Trainieren der Logistischen Regression und für das Treffen der Vorhersage. Diese beiden Funktionen sind mit einem Decorator versehen, welche von my_logger und my_timer kommen. Diese Decorator sorgen dafür, dass die Funktionen geloggt und getimt werden.
13. Dann werden die beiden Funktionen aufgerufen und ausgeführt. Im Anschluss werden auch wichtige Prints ausgeführt, welche gerade für die späteren Unittest wichtig sind. Bei dem Trainieren sind es einmal die Dauer, wie lang das Trainieren dauert, sowie die Genauigkeit und die Confusion Matrix des Trainings. Bei der Vorhersage dagegen wird die Genauigkeit, die Confusion Matrix und der Classification Report ausgegeben.
14. Dann wird die Klasse TestInput erstellt, welche die Unittest Klasse darstellt. Dafür werden Unittest interne Funktionen verwendet, um diesen aufzubauen. Der Hauptteil ist dabei die Funktion setUp(self). Hier werden alle wichtigen Daten dem Unittest übergeben, dies beinhaltet: Die Aufteilung der Daten, der TrainTestSplit, die Trainingsgenauigkeit, die Trainings Confusion Matrix und Laufzeit, ebenso de Testgenauigkeit und Confussion Matrix. Diese Werte werden alle aus dem zuvor ausgeführten Model übernommen und dienen als Grundlage für den Unittest, dass dieser erfolgreich durchläuft.
15. Nun folgt die Funktion test_fit() welche den Testfall 2 beschreibt. Hier wird das Modell als erstes trainiert. Dann wird überprüft, ob die Testgenauigkeit der Unittest-Genauigkeit übereinstimmen, sowie die Confuison Matrizen beider Fälle. Dieser Abgleich ist im Testfall 2 nicht gefordert und somit ein kleiner Bonus, da dies aufgrund der parallelen Entwicklung der Testfälle entstand. Dann kommt die eigentliche Aufgabe die Überprüfung der Laufzeit. Hierfür wird die Laufzeit des Tests genommen und mit 1,2 multipliziert, um einen Toleranzwert von 120% zu erreichen. Dann wird mit assertLessEqual überprüft, ob die Unittest Laufzeit unter oder gleich der Testlaufzeit ist, wenn ja ist dieser Test erfolgreich abgeschlossen. Danach werden alle drei Laufzeiten, Test-, Modifizierte- und Unittest Laufzeit ausgegeben, sowie in einem extra File gespeichert, dem „Testdatenfile_Fit.txt“.
15. Nun folgt die Funktion test_predict() welche den Testfall 1 beschreibt. Hier wird das Modell als erstes trainiert und dann vorhergesagt. Dann wird überprüft, ob die Testgenauigkeit der Unittest-Genauigkeit übereinstimmen, sowie die Confuison Matrizen beider Fälle. Wenn diese beiden abgleiche mit der assertEqual Funktion erfolgreich waren, ist der Test positiv. Danach werden beide Test- und Unittest Genauigkeiten und Confusion Matrizen ausgegeben, sowie in einem extra File gespeichert, dem „Testdatenfile_Predict.txt“.

Damit ist auch die zweite Prüfungsaufgabe abgeschlossen.
