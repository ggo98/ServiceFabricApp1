* Install SDK
https://learn.microsoft.com/en-us/azure/service-fabric/service-fabric-get-started#install-the-sdk-and-tools

* GUI:
http://localhost:19080/Explorer/index.html#/

* Note: le service Stateful1 va là:
C:\SfDevCluster\Data\_App\_Node_0\ServiceFabricApp1Type_App1\Stateful1Pkg.Code.1.0.0

* installer les cmdlets de ServiceFabric (MARCHE PAS):
(once)
Install-Module -Name ServiceFabric -Force
#Install-Module -Name ServiceFabric -AllowPrerelease -Force

* Arrêter/Démarrer le "truc":

Import-Module -Name ServiceFabric

#cls

Write-Host("Connect-ServiceFabricCluster 1")
Connect-ServiceFabricCluster -ConnectionEndpoint localhost:19000
Write-Host("Connect-ServiceFabricCluster 2")
# n'existe pas ou plus.
#Stop-ServiceFabricService -ApplicationName fabric:/ServiceFabricApp1 -ServiceName fabric:/ServiceFabricApp1/Stateful1
# n'existe pas ou plus.
#Invoke-ServiceFabricPartitionRestart -ServiceName fabric:/ServiceFabricApp1/Stateful1 -RestartPartitionMode AllReplicasOrInstances

<#
Write-Host("Stop-ServiceFabricNode 1")
Stop-ServiceFabricNode -NodeName "_Node_0" -TimeoutSec 30
Write-Host("Stop-ServiceFabricNode 2")
#>

Write-Host("Start-ServiceFabricNode 1")
Start-ServiceFabricNode -NodeName "_Node_0" -TimeoutSec 30
Write-Host("Start-ServiceFabricNode 2")

You can remove your cluster services via 'Cluster Manager' or via 'POwershell'.
- Via Cluster Manager:
In the task bar tray (clock) right-click on SF (Service Fabric etc...) icon
Select the option 'Remove Cluster' (ou 'STOP Cluster' plutôt ?)
- Via Powershell (PAS testé):
Executing the following powershell script(as administrator) instead:
C:\Program Files\Microsoft SDKs\Service Fabric\ClusterSetup\CleanCluster.ps1'


