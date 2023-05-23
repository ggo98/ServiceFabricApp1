* Install SDK
https://learn.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started#install-the-sdk-and-tools

* GUI:
http://localhost:19080/Explorer/index.html#/

* installer les cmdlets de ServiceFabric (MARCHE PAS):
(once)
Install-Module -Name ServiceFabric -Force
#Install-Module -Name ServiceFabric -AllowPrerelease -Force

* Arrêter le "truc":
You can remove your cluster services via 'Cluster Manager' or via 'POwershell'.
- Via Cluster Manager:
In the task bar tray (clock) right-click on SF (Service Fabric etc...) icon
Select the option 'Remove Cluster' (ou 'STOP Cluster' plutôt ?)
- Via Powershell (PAS testé):
Executing the following powershell script(as administrator) instead:
C:\Program Files\Microsoft SDKs\Service Fabric\ClusterSetup\CleanCluster.ps1'


