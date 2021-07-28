```
az eventgrid topic create --name $topicname -l $location -g $resourceGroup

$topicId = az eventgrid topic list --query ‘[0].id’ --output json

az eventgrid event-subscription create --name $ehSubName --source-resource-id $topicId --endpoint $hubId --endpoint-type eventhub

$endpoint = az eventgrid topic list --resource-group $resourceGroup --query '[0].endpoint' --output tsv
```
