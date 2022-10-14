
# Audiogame Protoype





## Inhalt

1. [Struktur](#Struktur)
2. [Example2](#example2)
3. [Third Example](#third-example)
4. [Fourth Example](#fourth-examplehttpwwwfourthexamplecom)
## Struktur

### Game und Gamestates
Die **Game** Klasse beinhaltet alle Globalen spielrelevanten Daten. Unter anderem: 
- *alle Räume*
- *der aktuelle Raum in dem sich der Spieler befindet* 
- *alle Charaktere* 
- *der altuell gespielte Charakter* 
- *und auch der aktuelle **Gamestate***.


Ein ***Gamestate*** ist ein Zustand in welchem sich das Spiel befinden kann.

Die verschiedenen Gamestates sind:

- [PLAYING](####PLAYING)
- [INVENTORY](####INVENTORY)
- [CONTAINER](####CONTAINER)
- [SEARCHING](####SEARCHING)
- [MENU](####MENU)

#### PLAYING 
---
Dieser Gamestate ist der default zustand des Spiels. In diesem Gamstate ist es möglich sich durch Räume zu bewegen, Items aufzuheben, *CONTAINER* zu öffnen usw. Es ist der Ausgangszustand um in andere Gamestates hineinzugelangen.

#### INVENTORY 
---
Wenn man im Gamestate [PLAYING](####PLAYING) nach unten Swiped, oder den jeweiligen Sprachbefehl ausführt, gelangt man in diesen Gamestate.In ihm ist es möglich durch seine Items zu iterieren, ein Item auszuwählen Items mithilfe des **Kombinationsmoduses** zu Kombinieren

#### CONTAINER
---
In diesen Gamestate gelangt man, indem man einen **CONTAINER** betritt.
Hier ist es möglich, durch die Items, die dieser **CONTAINER** enthält zu cyclen und sie aufzuheben.
Verlässt diesen wieder (z.B. durch Runterswipen) kommt man wieder in den [PLAYING](####PLAYING) Gamestate. 

#### SEARCHING
---
Dies ist der Gamestate einer Spezial-Interaktion. In ihm ist es das Ziel nach **HINTS** zu suchen in dem  man sein finger über den Bildschirm fährt.
Beendet man die Spezialinteraktion, verlässt man diesen Gamestate automatisch.

#### MENU
---
Bisher ist dies Nur der Start-Zustand des Spiels. Nach hochswipen gelangt man in das eigentliche Spiel.
Dies ist aufgrund einer Browser-Beschränkung, die es vorschreibt, das Sound nur nach einer Erst-Interaktion des Users abgespielt werden darf.