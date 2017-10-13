# deegree 

## Artefakte Entwicklungsversion LDBV

Die Entwicklungsversion besteht aus folgenden Komponenten:
* deegree-webservices (war)
* deegree-cli-utility (jar) 
* deegree-webservices-handbook (pdf)
* deegree-webservices-handbook (zip)

Die bereitgestellten Artefakte basieren auf [deegree 3.4 RC3](http://github.com/deegree/deegree3) und dem [deegree-cli-utility](https://github.com/lat-lon/deegree-cli-utility/tree/deegree-3.4-bayldbvdeegree) und enthalten u. a. folgende, für die INSPIRE-Umsetzung notwendigen Bugfixes/Features:
* https://github.com/deegree/deegree3/issues/573 Filter auf xlink:href (Bug)
* https://github.com/deegree/deegree3/issues/781 GetFeatureInfo-XSLT bei INSPIRE-Datenmodellen (Bug)
* https://github.com/deegree/deegree3/issues/782 Möglichkeit SOAP zu deaktivieren.

Die Bugfixes/Feature stehen als Pull-Request dem [OpenSource-Projekt](https://github.com/deegree/deegree3/pulls) zur Verfügung. 

## deegree-cli-utility Konfiguration für INSPIRE

Für die spätere Filterung von xlink:href-Attributen (z. B. bei SLDs) ist es notwendig, während der Erstellung der Dienstekonfiguration (FeatureStore, DDL) alle Attribute zu benennen, die nicht als GML-Referenz sondern als primitiver String interpretiert werden sollen (z. B. xlink:href bei Codelisten). 

Dies geschieht über eine deegree-cli-utility Konfigurationsdatei mit folgendem Aufbau:
```
{http://inspire.ec.europa.eu/schemas/gn/4.0}nativeness
{http://inspire.ec.europa.eu/schemas/ps/4.0}designation
```

Folgende Konfigurationsdatei enthält erste für INSPIRE relevante Ausnahmen: 
https://github.com/gdi-by/deegree-sandbox/blob/master/inspire-properties-with-primitive-href.properties 
