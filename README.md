# AKS Well Architected

Using [AKS Construction](https://github.com/Azure/AKS-Construction) and [PSRule](https://azure.github.io/PSRule.Rules.Azure/) to create a Well Architected configuration for your AKS environment.

## Repo purpose

To serve as a demonstratable Well Architected review of a live environment.

Using GitHub actions to orchestrate the environment deploy and assessment. Failures are reported in the GitHub step summary, GitHub artifacts and by raising an issue in the repository.

The sample workflow runs on demand, and on a schedule. By running on a schedule we can be alerted to both;
1. Degredations in our environment configuration 
2. New rules in the Well Architected assesment

## AKS Configurations

Description | AKSC | Rules passed | Rules failed | PSRule Config | Rules exempt
----------- | ----- | ------------ | ----------- | ------------- | ------------
The "cool" config, Cillium, Azure CNI Overlay and Prometheus monitoring through Azure monitor | [AKSC](https://azure.github.io/AKS-Construction/?feature=defender&cluster.DefenderForContainers=true&addons.enableACRTrustPolicy=true&preset=defaultOps&deploy.deployItemKey=deployArmCli&deploy.githubrepo=https%3A%2F%2Fgithub.com%2FGordonby%2Faks-well-architected-assesment-brownfield&deploy.clusterName=brownfield&deploy.rg=AksBicepAcc-Ci-Brownfield&ops=none&secure=low&addons.monitor=aci&cluster.AksPaidSkuForSLA=true&cluster.autoscale=true) | 20 | 19
