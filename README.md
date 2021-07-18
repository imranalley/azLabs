# Azure Labs

## Creating a VM using Powershell and AzureCLI

1. `Get-AzResourceGroup`
	1. Copy the ResourceGroupName
2. `New-Azvm -ResourceGroupName '$ResourceGroupName' -Name 'TestVM' -VirtualNetworkName 'MyVNet' -SubnetName 'MySubnet' -SecurityGroupName 'MySecurityGroup' -PublicIpAddressName 'myPubIP' -OpenPorts 80,3389`
	1. Create username and password
3. `Get-AzPublicIpAddress`
	1. Connect via Public IP Address

## REST API Calls for Blobs
```
curl -X PUT -H "x-ms-blob-type:BlockBlob" \
  -H "x-ms-date:$request_date" \
  -H "x-ms-version:$storage_service_version" \
  -H "Authorization: $authorization_header" \
  -H "Content-Length:$file_length" \
  -H "Content-Type:$content_type" \
  --data-binary "@cars.csv" \
  "https://${storage_account}.blob.core.windows.net/records/cars"
```

```
curl -H "x-ms-date:$request_date" \
  -H "x-ms-version:$storage_service_version" \
  -H "Authorization: $authorization_header" \
  "https://${storage_account}.blob.core.windows.net/records/cars" > cars.csv
```
