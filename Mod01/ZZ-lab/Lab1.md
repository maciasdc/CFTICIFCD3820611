**Connection String:**

```
DefaultEndpointsProtocol=https;AccountName=imgstordcmb;AccountKey=HiYw8OVQjCD7G4EcVn2aVwEBE7xzJLOb54IzhqBFdpL78SFLVw5enj+IZuBT5TndijH4l3csuUSIWqUeC9SgiA==;EndpointSuffix=core.windows.net
```

**URL WEB API:**

```
http://imgapidcmb.azurewebsites.net/
```

```
az webapp deployment source config-zip --resource-group ManagedPlatform --src api.zip --name imgapidcmb
```

```
az webapp deployment source config-zip --resource-group ManagedPlatform --src web.zip --name imgwebdcmb
```