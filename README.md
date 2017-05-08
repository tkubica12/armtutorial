# ARM šablony - tutoriál

## demo01 - IP adresa
az group deployment create --template-file .\demo01.json -g arm

## demo02 - zmena nazvu, rozdil mezi increment a complete
az group deployment create --template-file .\demo02.json -g arm
az group deployment create --template-file .\demo02.json -g arm --mode Complete

## demo03 - variables
az group deployment create --template-file .\demo02.json -g arm

## demo04 - variables s location z resource group
az group deployment create --template-file .\demo02.json -g arm

## demo05 - parametry
az group deployment create --template-file .\demo05.json --parameters "@demo05.parameters.json" -g arm --mode Complete

## demo06 - smycka
az group deployment create --template-file .\demo06.json --parameters "@demo06.parameters.json" -g arm --mode Complete

## demo07 - smycka nad polem
az group deployment create --template-file .\demo07.json --parameters "@demo07.parameters.json" -g arm --mode Complete

## demo08 - smycka + dependencies
az group deployment create --template-file .\demo08.json --parameters "@demo08.parameters.json" -g arm --mode Complete

## demo09 - output
az group deployment create --template-file .\demo09.json --parameters "@demo09.parameters.json" -g arm --mode Complete


## troubleshooting
az group deployment operation list --name demo08  --resource-group arm