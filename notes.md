# Azure Labs

Creating a VM using Powershell and AzureCLI

1. `Get-AzResourceGroup`
	1. Copy the ResourceGroupName
2. `New-Azvm -ResourceGroupName '$ResourceGroupName' -Name 'TestVM' -VirtualNetworkName 'MyVNet' -SubnetName 'MySubnet' -SecurityGroupName 'MySecurityGroup' -PublicIpAddressName 'myPubIP' -OpenPorts 80,3389`
	1. Create username and password
3. `Get-AzPublicIpAddress`
	1. Connect via Public IP Address
