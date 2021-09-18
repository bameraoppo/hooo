#!/bin/bash
az group create --name hanpuy2 --location eastus2
az vm create --resource-group hanpuy2 --name switzerlandnorth --location switzerlandnorth --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name southeastasia --location southeastasia --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name eastus --location eastus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name brazilsouth --location brazilsouth --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name westus --location westus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name westus2 --location westus2 --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name southcentralus --location southcentralus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name northeurope --location northeurope --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name westeurope --location westeurope --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name japaneast --location japaneast --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name australiaeast --location australiaeast --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name centralus --location centralus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name eastasia --location eastasia --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name uksouth --location uksouth --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name koreacentral --location koreacentral --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name westcentralus --location westcentralus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name centralindia --location centralindia --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name canadacentral --location canadacentral --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name northcentralus --location northcentralus --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
az vm create --resource-group hanpuy2 --name francecentral --location francecentral --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
sleep 10m
x=1
while [ $x -le 500 ]
do
  echo "Start vps lan $x"
  az vm start --ids $(az vm list -g hanpuy2 --query "[?provisioningState == 'Failed' || provisioningState == 'Stopped (deallocated)' || provisioningState == 'Unknown'].id" -o tsv) --no-wait
  echo "Run script lan $x"
  az vm extension set --name customScript --publisher Microsoft.Azure.Extensions --ids $(az vm list -d --query "[?powerState=='VM running'].id" -o tsv) --settings '{"fileUris": ["https://raw.githubusercontent.com/0axz-tools/puyhan/main/named.sh"],"commandToExecute": "./named.sh"}'  --no-wait
  for vps in switzerlandnorth southeastasia eastus brazilsouth westus westus2 southcentralus northeurope westeurope japaneast australiaeast centralus eastasia uksouth koreacentral westcentralus centralindia canadacentral northcentralus koreacentral francecentral
  do
    if [ "$(az vm list -g hanpuy2 --query "[?name == '$vps'].id" -o tsv)" = "" ];
    then
      echo "$vps creating..."
	  az vm create --resource-group hanpuy2 --name $vps --location $vps --image Canonical:UbuntuServer:16.04-LTS:latest --size Standard_NC6s_v3 --admin-username azure --admin-password Sampoerna88Mild --priority Spot --max-price -1 --eviction-policy Deallocate --no-wait
    else
      echo "$vps was found."
    fi
  done
  sleep 7m
  x=$(( $x + 1 ))
done
az vm delete --ids $(az vm list -g hanpuy2 --query "[?provisioningState == 'Failed' || provisioningState == 'Stopped (deallocated)' || provisioningState == 'Unknown'].id" -o tsv) --yes --force-deletion --no-wait
