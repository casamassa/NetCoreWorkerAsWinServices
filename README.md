# NetCoreWorkerAsWinServices
.Net Core Worker as Windows Services

Create the Windows Services using sc.exe tool

Step 1: Publish the Worker service
cd "Path to the Worker service project"

dotnet restore

dotnet publish -o PathToThePublishFolder


Step 2: Deploy and start with sc utility
sc.exe create DemoWorker binpath= PathToThePublishFolder\YourWorkerClassName.exe

sc.exe start YourWorkerClassName


Step 3: Stop and delete with sc utility
sc.exe stop YourWorkerClassName 

sc.exe delete YourWorkerClassName 
