# Module: NoOps Accelerator - Management Services

## Overview

NoOps Accelerator management services overlays are module templates that can be deployed to extend an existing Platform Landing Zones or Enclave. 

## Management Services Explanations

Service | Description |  Link|
------- | ----------- | -----|
Azure App Service Plan | This overlay module deploys an App Service Plan (AKA: Web Server Cluster) to support simple web accessible linux docker containers.  It also optionally supports the use of dynamic (up and down) scale settings based on CPU percentage up to a max of 10 compute instances. | [Azure App Service Plan](../management-services/app-service-plan/deploy.bicep)
Azure Application Gateway | This overlay module adds an web traffic load balancer that enables you to manage traffic to your web applications. This application gateway is meant to be in the Hub Network. | [Azure Application Gateway](../management-services/applicationGateway/deploy.bicep)
Azure Automation Account | This overlay module deploys an Platform Landing Zone compatible Azure Automation account, with diagnostic logs pointed to the Platform Landing Zone Log Analytics Workspace (LAWS) instance. | [Azure Automation Account](../management-services/automation/deploy.bicep)
Bastion Host | This overlay module adds a linux and windows virtual machines to the Hub resource group to serve as a jumpbox into the network using Azure Bastion Host as the remote desktop solution without exposing the virtual machine via a Public IP address. | [Bastion Host](../management-services/bastion/deploy.bicep)
Azure Container Registry | This overlay module deploys a premium Azure Container Registry suitable for hosting docker containers. The registry will be deployed to the Hub/Spoke shared services resource group using default naming unless alternative values are provided at run time. | [Azure Container Registry](../management-services/bastion/deploy.bicep)
Microsoft Defender for Cloud | This overlay module adds a standard/defender sku which enables a greater depth of awareness including more recomendations and threat analytics. | [Microsoft Defender for Cloud](../management-services/defender/deploy.bicep)
Microsoft Front Door Service | Module to deploy the Microsoft Front Door Service to the Hub Network
Network Security Groups | Module to deploy the Microsoft Front Door Service to the Hub Network

