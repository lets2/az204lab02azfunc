# AZ-204 LAB 02 AZURE FUNCTION

[AZ-204 - Todos os labs](https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/)
[AZ-204 - LAB 2 - az function](https://microsoftlearning.github.io/AZ-204-DevelopingSolutionsforMicrosoftAzure/Instructions/Labs/AZ-204_lab_02.html)

func init --worker-runtime dotnet-isolated --target-framework net8.0 --force

dotnet build

"AzureWebJobsStorage": "UseDevelopmentStorage=true",

func new --template "HTTP trigger" --name "Echo"

func start --build
func start --build --port 7071, a 7071 é a padrão

curl -X POST -i http://localhost:7071/api/echo -d 3
curl -X POST -i http://localhost:7071/api/echo -d "{"msg":"okay"}"
