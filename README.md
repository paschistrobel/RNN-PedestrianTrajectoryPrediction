# Trainieren eines Neuronalen Netzes zur Prädiktion der Trajektorie von Fußgängern
Modulprüfung zum Thema "Trajektorien-Prädiktion von Fußgängern" im Fach "Computational Intelligence" an der Universität Regensburg im Sommersemester 2021.<br>
- [Projektdokumentation](Dokumentation/Projektdokumentation.pdf)<br>
- [Annotierter Code in Form eines Jupyter-Notebooks](PedestrianTrajectoryPrediction.ipynb)

## Aufgabe
Ziel der Projektarbeit ist die Vorhersage der zukünftigen Trajektorie/Bewegungsbahn eines Fußgängers, basierend auf bekannten, vergangenen Positionen. Ganz speziell sind in diesem Fall die ersten 8 Positionen eines Fußgängers gegeben und mit diesen Informationen sollen die nächsten 12 prädiziert werden. Die Aufgabenstellung wird auch nochmal in Abb. 1 verdeutlicht. <br>
<p align="center">
	<img src="Dokumentation/Grafiken/fc_best1.png" width="400"><br>
	<em>Abbildung 1: Beispiel-Trajektorie eines Fußgängers. Mithilfe der ersten acht beobachteten Positionen (blau) prädiziert das System die zukünftigen zwölf (rot). Die vorhergesagte Trajektorie sollte dabei möglichst nah an der Ground-Trouth (grün) liegen.</em>
</p>

## Lösungsansatz
- zuerst normalisieren und standardisieren
Zur Lösung des Problems wurde ein auf LSTM basierendes neuronales Netz mit folgender Architektur trainiert. <br>
<p align="center">
	<img src="Dokumentation/Grafiken/network_architecture.PNG" width="400">
</p>

Anmerkung: Code und 

## Evaluation
Der vorgestellte Ansatz wurde dann anhand zweier gängiger Metriken evaluiert.
	- Average displacement error (ADE): Durchschnittliche Fehler zwischen prädizierten Positionen und Ground-Trouth für alle (12) vorhergesagten Zeitschritte von allen Fußgängern des Testdatensatzes
	- Final displacement error (FDE): Der durchschnittliche Fehler zwischen prädizierter Position und Ground-Trouth zum finalen Zeitpunkt eines Fußgängers, für allen Fußgängern des Testdatensatzes

Das vorgestellte System erreicht dabei einen FDE von ... und einen ADE von ...

Zudem konnte durch eine qualitative Analyse einige Failure Cases festgestellt werden, bei denen der Ansatz zu versagen scheint
