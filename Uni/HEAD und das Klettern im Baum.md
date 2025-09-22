# HEAD
ist der Alias für den Commit (auf dem Branch), der gerade ausgecheckt ist. 
Mit jedem Commit wandert HEAD mit.

## detach HEAD
```
git checkout <commitHash>
```
entkoppelt HEAD vom Branch -> *detached HEAD state*
HEAD zeigt dann auf diesen einen Commit, nicht auf den Branch.
Den Hash erfährt man über `git log`, es reicht aber, ausreichend viele Zeichen einzugeben, um eindeutig auf einen Commit zu verweisen.

## relative Referenzen
### mit ^ einen Commit zurück gehen
```
git checkout main^
```
geht zum vorherigen Commit auf main zurück.
```
git checkout HEAD^
```
folgt den Vorfahren von HEAD.
Mit mehreren ^ erhöht sich die Zahl der Schritte zurück entsprechend.
### mit ~n Schritte zurück gehen
```
git checkout main~5
```
geht die angegebene Anzahl Schritte zurück.

