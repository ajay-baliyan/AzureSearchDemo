# Configuring Azure Search:

This user manual will guide you through to create an Azure Search Instance with sample data on associated Blob Storage account.

1) The Azure Resource Manager(ARM) template will be used to deploy the Search and Blob Storage. This will be the one click deployment solution.  
Note - It is reccomended to keep the search and blob names short as there is a maximum length of 24 characters and the ARM template will add a guid to the end of the value you provide. [![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/).

From the [Azure Portal](https://portal.azure.com), note following four key information to configure search:
Search Service Name
Admin Key of Search Instance
BLOB name
BLOB Account access key1\ key2.

2) Create a container in the blob storage account called "allblobs" (you can call it something different, but you'll have to change the REST calls to reflect it), and upload a sample file to it. I used a publicly available [food hygeine dataset](https://data.gov.uk/dataset/uk-food-hygiene-rating-data-yorkshire-and-humberside-food-standards-agency/resource/b290ee03-1405-4b90-ae63-2ae09d8c7791) from DATA.GOV.UK.  The data is available in XML format so I used a simple XML to JSON transformation - the converted file is available [here](https://github.com/ajay-baliyan/AzureSearchDemo/blob/master/sampledata.json) if you want to use this.  I recommend using [Azure Storage Explorer](http://storageexplorer.com/) for uploading the file.

3) Next, you need to create a search index.

4) Then, add a data source to point to your blob storage account.
5) Once the data source has been added, then you need to add an indexer, which maps the data source to the index.
6) Test! You can use the Azure Portal to test.  The Search instance has a Search Explorer that you can use to type in a search and run the query - or you can query the REST endpoint directly. 



