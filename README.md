# deegree 

## deegree-cli-utility Konfiguration für INSPIRE

Für die spätere Filterung von xlink:href-Attributen (z. B. bei SLDs) ist es notwendig, während der Erstellung der Dienstekonfiguration (FeatureStore, DDL) alle Attribute zu benennen, die nicht als GML-Referenz sondern als primitiver String interpretiert werden sollen (z. B. xlink:href bei Codelisten). 

Dies geschieht über eine deegree-cli-utility Konfigurationsdatei mit folgendem Aufbau:
```
{http://inspire.ec.europa.eu/schemas/gn/4.0}nativeness
{http://inspire.ec.europa.eu/schemas/ps/4.0}designation
```

Folgende Konfigurationsdatei enthält erste für INSPIRE relevante Ausnahmen: 
https://github.com/gdi-by/deegree-sandbox/blob/master/inspire-properties-with-primitive-href.properties 
Diese Datei wurde als Grundlage für unsere aktuelle Datei verwendet und ergänzt
