PROJEKTMANAGEMENT

# Anforderungen
## Tasks
- Tasks können erstellt werden
- Tasks befinden, wenn sie den Status TODO besitzen, in einem Pool
- Tasks können einem Mitarbeiter zugeordnet werden
- Tasks wechseln in den Status Doing, wenn sie einem Mitarbeiter zugeordnet werden.
   Paradigma: Tasks koennen nicht von einem Mitarbeiter uebernommen sein und sich dabei noch im Status TODO befinden. Dies verhindert, dass 
- Tasks besitzen Status: TODO, Doing, Review (QM), Done
- Tasks sind immer einem Projekt zugeordnet
- Tasks sind immer einem Milestone zugeordnet
- Tasks besitzen Estimates fuer den Aufwand
- Tasks besitzen geleisteten Aufwand
- Tasks koennen Labels besitzen.
- Tasks koennen nur fuer einen bestimmten Mitarbeitertyp zuordbar sein (Ingenieur, Entwickler....)
- Tasks koennnen Kommentare besitzen
- Tasks koennen von anderen Tasks abhaengig sein. Sie koennen dann erst in einen Status wechseln, wenn sich der Task, von dem sie abhaengig sind, auch mindestens in diesem Status befindet.
- **TODO**: Nicht nur die Zeit beim Doing, sondern auch im Review zaehlt! Sollte man die StoryPoints als Estimate fuer den Gesamtaufwand (Doing + Review) zahelen, und dann beim Tracking die aufgewendete Zeit differenzieren? ACHTUNG: Die aufgewendete Zeit in Doing unterscheidet sich von der im Review dadurch, dass das Review von einem anderen Mitarbeiter durchgefuehrt wird.
   Wahrscheinlich sollte das Estimate dann erstmal nur das Doing miteinbeziehen. Die Reviews werden dann nicht innerhalb des Sprints, sondern danach in einer review-phase gemacht.
   Im Zuge des Monitorings muss dann irgendwie abgeschaetzt werden, wie lange die Review-Phase dauert. Hier koennte man eine art "review-velocity" bilden, indem aus den vorherigen Sprints abgeschaetzt wird, wieviel review-zeit fuer einen StoryPoint im Doing aufgewendet werden muss. Dabei ist aber noch zu evaluieren, ob zwischen Arbeitsaufwand im Doing und Review-Time eine relation besteht.
- Auch waehrend eines Sprints koennen "Issue-Tasks" angelegt werden, die ungeplante Probleme reflektieren. Die Differenzierung zwischen Normalen und Issue-Tasks soll es ermoeglichen, bei der Auswertung des Sprints festzustellen, wieviel Zeitaufwand nicht geplant gewesen ist. Dies soll dann einen Indikator dafuer geben, wieviel Zeitaufwand bei einem Sprint fuer nicht geplante Tasks einzurechnen ist. Dieser geschaetzte Issue-Zeitaufwand wird dann in der Planung von der verfuegbaren Entwicklungszeit subtrahiert.
   
   
#### TODO: Wie wird mit tasks umgegangen, die bei einem Sprint nicht fertiggestellt wurden, und dann im naechsten Sprint nicht weiter gemacht werden, da sich die Prioritaeten veraendert haben? Das Estimate und der geleistete Aufwand sollten gespeichert bleiben. Wird der Task dann wieder in TODO gesetzt und die Zuordnung zum Mitarbeiter aufgehoben?

## Monitoring
TODO: Man kann nicht Estimates als StoryPoints und geleistete Arbeitsstunden angeben.
Wir wollen aber sowohl eine Velocity in Form von Storypoints als auch eine abschaetzung der Arbeitsstunden.
Vorschlag: Es werden anstelle von Estimates in Zeitstunden "Storypoints" vergeben. 
Nach einem Sprint wird aus den tatsaechlich aufgewendeten Arbeitsstunden abgeschaetzt, wievielen Arbeitsstunden ein Storypoint entspricht. 
Vorgehensweise:
- Die aufgewendete Zeit aller Tasks, die nach dem Review Done sind, wird in Relation zu den vergebenen Storypoints gesetzt. 
   Daraus folgt dann ein gemessener Arbeitsaufwand je Storypoint.
   Die Mitarbeiter geben fuer jeden Sprint an, wieviel Zeit sie haben. Dann kann abgeleitet werden, wieviele StoryPoints das Team im Sprint schafft.
- Man koennte das StoryPoint/Zeit-Verhaeltnis auch je mitarbeiter berechnen, oder sogar statistische abschaetzungen machen.
- **Alternative zu Storypoints**: Es werden keine Storypoints, sondern direkt geschaetzte Arbeitsstunden an jeden Task vergeben. Am Ende jedes Sprints wird das verhaeltnis der tatsaechlich fuer abgeschlossene Tasks aufgewendeten Arbeitsstunden zu den fuer diese Tasks abgeschaetzten Arbeitsstunden in Relation gesetzt. Der daraus folgende Konversionsfaktor wird dann als indikator fuer die Qualitaet der Abschaetzung genutzt, sodass die Schaetzungen in zukuenftigen Sprints angepasst werden koennen. Fuer die Review-Velocity wird dann auch nicht die Review-Zeit mit den storypoints, sondern mit den abgeschaetzten Arbeitsstunden in Relation gesetzt.
- Fuer jeden Mitarbeiter wird am Ende des Sprints die tatsaechlich geleistete Arbeitszeit mit der vorher als verfuegbar eingeschaetzten abgeglichen. Damit soll abgeschaetzt werden koennen, vieviel zeit ein Mitarbeiter tatsaechlich effektiv aufbringen kann.

## Task-Pool
- Nicht angefangene Tasks befinden sich in einem Pool
- Im Pool koennen Tasks nach gewissen Aspekten (bspw. Estimate oder Projekt) gefiltert werden.
- WICHTIG: Das Monitoring der Tasks muss Einfach sein, damit es auch angewendet wird. Vorschlag: Im persoenlichen Board jedes Mitarbeites hat jeder Task einen Button, der aktiviert werden kann.
   Waehrend der Button aktiviert ist, arbeitet der Mitarbeiter an dem Task. Nur ein Task kann zu einem Zeitpunkt aktiviert sein. Waehrend der Task aktiviert ist, wird die Zeit gezaehlt. 
- Waehrend der Review-Phase existiert ein Review-Pool. Hier koennen mehrere Mitarbeiter denselben Task gleichzeitig reviewen. 

## Projekte
- Projekte besitzen Task
- Projekte besitzen Milestones
- Projekte besitzen Deadlines

## Milestones
- Milestones besitzen Deadlines

## Resourcen- und Zeitplanung
- Fuer jeden Sprint kann die Anzahl der verfuegbaren Stunden je Mitarbeiter angegeben werden.
- Auf Basis der Abhaengigkeiten von Tasks, der geschaetzten Zeiten, der Zuordbarkeit zu Mitarbeitertypen und der durchschnittlichen verfuegbaren Arbeitszeit wird abgeschaetzt, ob die Deadlines eingehalten werden koennen.

## Mitarbeiter
- Mitarbeiter besitzen einen Typ (Ingenieur, Entwickler)
- Mitarbeiter besitzen ein Zeitkontingent

# Umsetzung
