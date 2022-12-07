# BI-Slolution_Fusion_Zwei_Supermaerkte

Data Engineering  -Erstellen einer ETL-Pipeline mit SSIS
------------------------------------------------------
Dieses Projekt bietet einen Ausgangspunkt für die Erstellung einer ETL-Pipeline mit SQL Server Integration Services (SSIS) 
in Visual Studio 2019 zur Fusion die Daten zwei Supermärkte, die aus verschieden Quellen gesammelt sind und unterschiedlichen Datentypen wie
.json, .txt ,xlsx und .csv haben.  

Am Ende sollte ein Data Warehouse aufgebaut werden sein, damit Berichte und Dashboards basierend auf diese integrierte Daten erstellt werden können. 
die angewendete Architekture für Data Warehouse besteht auf vier Phasen: 
1. StageArea: in dieser Phase sind allte Daten auf den Quellen im System hochgeladen.
2. CleansingArea: in diser Phase wird die Daten bearbeitet. Die Fehler, doppelte Werte .... werden behandelt.

3. Core: hier ist das Kern das Data Warehouse, wo die Daten in einem integrierten Format gespreichert sind. In diesem Projekt ist Data Vault 2.0 als Datamodell verwendet.
In diesem Modell gibt es drei Komponenten: Hub, Linke und Satellite.
Hub:  repräsentiert Kerngeschäftskonzepte
Linke: represäntiert Beziehung zwischen Hubs
Satellite: in Satellite sind Informations über Hubs und Linkes gespeichert



![Unbenannt](https://user-images.githubusercontent.com/116841480/206168137-11f11bc8-262b-4a06-9bdb-c5ce2be56724.PNG)




Voraussetzung
         Visual Studio 2019               
         SQL Server
