# Trainieren eines Neuronalen Netzes zur Prädiktion der Bewegungsbahnen von Fußgängern
Modulprüfung zum Thema "Trajektorien-Prädiktion von Fußgängern" im Fach "Computational Intelligence" an der Universität Regensburg im Sommersemester 2021.
Hier geht's zur vollständigen [Projektdokumentation](Dokumentation/Projektdokumentation.pdf)
Hier geht's zum [Jupyter-Notebook des Projektes](PedestrianTrajectoryPrediction.ipynb)

## Aufgabe
Ziel der Projektarbeit ist die Vorhersage der zukünftigen Trajektorie/Bewegungsbahn eines Fußgängers, basierend auf bekannten, vergangenen Positionen. Ganz speziell sind in diesem Fall die ersten 8 Positionen eines Fußgängers gegeben und mit diesen Informationen sollen die nächsten 12 prädiziert werden. Die Aufgabenstellung wird auch nochmal in Abb. 1 verdeutlicht. <br>
![Beispieltrajektorie zur Verdeutlichung der Aufgabenstellung](Dokumentation/Grafiken/fc_best1.png)

## Lösungsansatz
- zuerst normalisieren und standardisieren
Zur Lösung des Problems wurde ein auf LSTM basierendes neuronales Netz mit folgender Architektur trainiert. <br>
![Verwendete Netzwerkarchitektur](Dokumentation/Grafiken/network_architecture.PNG | width=100)
<img src="Dokumentation/Grafiken/network_architecture.PNG" width="10">

Anmerkung: Code und 

## Evaluation
Der vorgestellte Ansatz wurde dann anhand zweier gängiger Metriken evaluiert.
	- Average displacement error (ADE): Durchschnittliche Fehler zwischen prädizierten Positionen und Ground-Trouth für alle (12) vorhergesagten Zeitschritte von allen Fußgängern des Testdatensatzes
	- Final displacement error (FDE): Der durchschnittliche Fehler zwischen prädizierter Position und Ground-Trouth zum finalen Zeitpunkt eines Fußgängers, für allen Fußgängern des Testdatensatzes

Das vorgestellte System erreicht dabei einen FDE von ... und einen ADE von ...

Zudem konnte durch eine qualitative Analyse einige Failure Cases festgestellt werden, bei denen der Ansatz zu versagen scheint
