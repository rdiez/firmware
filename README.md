# Eulenfunk Firmware - Stand 08/01/2019
 
Serviervorschlag:
```
git clone https://github.com/eulenfunk/firmware
cd firmware
git clone https://github.com/freifunk-gluon/gluon
./build.sh sites.ffmet
```
Gluon-dependencies müssen ebenfalls auf dem System installiert sein.

Sites-Dateien enthalten eine Liste an Site-Konfigurationen die aus dem Template (aus `templates/`) erstellt werden.
Diese enthalten dann Zeilen wie `experimentall2tp v2018.2.x dusl2tp dusl2tp`.
Achtung, Zeile mit muss mit CR abgeschlossen sein, aber darf keine Leerzeilen enthalten.. ja, das ist ungünstig.

Das Buildscript wird mit der Sites-Datei als Parameter aufgerufen, zusätzlich können beliebig viele Architekturen angegeben werden, für die Images gebaut werden sollen. Wird keine Architektur angegeben, werden alle gebaut.
`./build.sh sites.ffmet ar71xx-generic ar71xx-nand`
