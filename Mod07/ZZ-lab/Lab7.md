**Storage connection string**

**Access Keys\Connection string**

```
DefaultEndpointsProtocol=https;AccountName=securestordcmb;AccountKey=dFbO2jjL0Fb4IyZteXE/J5AmDYftdfrkA2jQl3IXs1hO/oT193WBXT0iJCa7kY2nE3nURGIwa5vHahKTFiWSBg==;EndpointSuffix=core.windows.net
```

**securevaultdcmacias\secrets\storagecredentials\Current version**

**Secret identifier**

```
https://securevaultdcmacias.vault.azure.net/secrets/storagecredentials/f42c182656c940bdba434d511426856c
```



**securefuncdcmb\Settings\Configuration**

**New application setting**

**StorageConnectionString**

```
@Microsoft.KeyVault(SecretUri=Secret Identifier)
```

```

```



Editing the FileParser file:

```csharp
using Azure.Storage.Blobs;
using Microsoft.AspNetCore.Mvc;
using Microsoft.Azure.WebJobs;
using Microsoft.AspNetCore.Http;
using System;
using System.Threading.Tasks;

public static class FileParser
{
    [FunctionName("FileParser")]
    public static async Task<IActionResult> Run(
        [HttpTrigger("GET")] HttpRequest request)
    {
        string connectionString = Environment.GetEnvironmentVariable("StorageConnectionString");
        BlobClient blob = new BlobClient(connectionString, "drop", "records.json");
        var response = await blob.DownloadAsync();
        return new FileStreamResult(response?.Value?.Content, response?.Value?.ContentType);
    }
}
```