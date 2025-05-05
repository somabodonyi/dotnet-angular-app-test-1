# Backend Setup and Deployment

## Setting up and running the .NET app

1. Install .NET 9 SDK from the official .NET website.
2. Clone the repository to your local machine.
3. Navigate to the `backend` directory.
4. Restore the project dependencies by running the following command:
   ```
   dotnet restore
   ```
5. Build the project by running the following command:
   ```
   dotnet build
   ```
6. Run the project by executing the following command:
   ```
   dotnet run
   ```

## Building and deploying the .NET app

1. Build the project for production by running the following command:
   ```
   dotnet publish -c Release -o out
   ```
2. Create a Docker image for the .NET app:
   ```
   docker build -t <your-docker-image-name> .
   ```
3. Push the Docker image to Azure Container Registry:
   ```
   docker tag <your-docker-image-name> <your-azure-container-registry>/<your-docker-image-name>
   docker push <your-azure-container-registry>/<your-docker-image-name>
   ```
4. Deploy the Docker image to Azure Container Apps using the Azure CLI:
   ```
   az containerapp create --name <your-container-app-name> --resource-group <your-resource-group> --image <your-azure-container-registry>/<your-docker-image-name> --environment <your-environment-name>
   ```
