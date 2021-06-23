**COSMOSDB**

**PRIMARY CONNECTION STRING** 

```
AccountEndpoint=https://polycosmosdcmb.documents.azure.com:443/;AccountKey=nf5R3aOXzNQIdHd5O8mLGNEeL3LXiv9dwIbxrLjdc7MyJCLsR9oeHnSwivD2YoDqNKpIT1rTuf5mvzyF2pUFEA==;
```

**SQL Server**

Home\ **polysqlsrvrdcmb\AdventureWorks**

**ADO.NET (SQL authentication)**

```
Server=tcp:polysqlsrvrdcmb.database.windows.net,1433;Initial Catalog=AdventureWorks;Persist Security Info=False;User ID=testuser;Password={your_password};MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;
```

**Blob container images URL**

```
https://polystordcmb.blob.core.windows.net/images
```
**Migrate projects**

```
dotnet new console --name AdventureWorks.Migrate --framework netcoreapp3.1
```

User and password:

```
In the Login text box, enter testuser.

In the Password text box, enter TestPa55w.rd.
```

