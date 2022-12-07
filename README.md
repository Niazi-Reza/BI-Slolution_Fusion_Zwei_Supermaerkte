# BI-Slolution_Fusion_Zwei_Supermaerkte

Data Engineering  -Erstellen einer ETL-Pipeline mit SSIS
------------------------------------------------------
Dieses Projekt bietet einen Ausgangspunkt für die Erstellung einer ETL-Pipeline mit SQL Server Integration Services (SSIS) 
in Visual Studio 2019 zur Fusion die Daten zwei Supermärkte, die aus verschieden Quellen gesammelt sind und unterschiedlichen Datentypen wie
.json, .txt ,xlsx und .csv haben.  

Am Ende sollte ein Data Warehouse aufgebaut werden sein, damit Berichte und Dashboards basierend auf die integrierte Daten erstellt werden. 
Die angewendete Architekture für Data Warehouse besteht auf vier Phasen: 

1. StageArea: in dieser Phase sind alle Daten aus den Quellen im System hochgeladen.
2. CleansingArea: in diser Phase wird die Daten bearbeitet. Die Fehler, doppelte Werte .... werden bearbeitet.
3. Core: hier ist der Kern das Data Warehouse, wo die Daten in einem integrierten Format gespeichert sind. In diesem Projekt ist Data Vault 2.0 als Datamodell verwendet. Data Vault besteht aus drei Komponenten: Hubs, Links und Satellites.

Hub:  repräsentiert Kerngeschäftskonzepte
Linke: represäntiert Beziehung zwischen Hubs
Satellite: in Satellite sind Informationen über Hubs und Links gespeichert

4. Data Marts: hier wird ein Star Schema aufgebaut. Diese Star Schema wird zur Erstellung von Berichtn und Dashboards für den Endnutzer verwendet.



 Architekture von Data Warehouse
----------------------------------------------------
 
![Unbenannt](https://user-images.githubusercontent.com/116841480/206168137-11f11bc8-262b-4a06-9bdb-c5ce2be56724.PNG)



CleansingArea 
----------------------------------------------------------

![Screenshot (134)](https://user-images.githubusercontent.com/116841480/206174638-4aff04ab-f6ec-4c94-ae2e-a0df015aaebc.png)


Data Vault Modell
-----------------------------------------------------------------
![Screenshot (135)](https://user-images.githubusercontent.com/116841480/206174762-a57cb74d-2178-4eb4-b2de-2fc8f695982b.png)


Voraussetzung
---------------------------------------------------------------------
         Visual Studio 2019               
         SQL Server
        
Vorgehensweise
----------------------------------------------------------------------
Dieses Projekt wurde in SSIS und SSMS erledigt. Zunächst werden die Daten(.json, .txt) mit Hilfe von Python in .csv Format umgewandelt und in StageArea hochgeladen. Danach wurden die Struktur und Fehler der Daten bearbeiet. In dieser Phase wurden die doppelte Informationen und andere mögliche Fehler bei den Daten bearbeitet, damit alles sauber zum Laden in Core als Data Vault Modell vorbereitet sind. 
In Core ist Dat Vault aufgebaut und alle Geschäftsrelevante Daten sind da gespreichert. Anschließend sind Data Marts zur Nutzung von Endnutzer mit Hilfe von  durch Reporting-Tools oder Dashboards verwendet. 


Beispiel für Dashboard
-------------------------------------------------------------------------
![Screenshot (136)](https://user-images.githubusercontent.com/116841480/206181131-750c384c-3a8f-4983-bb07-29d2466c08c5.png)







