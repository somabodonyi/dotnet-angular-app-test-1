# Frontend - Angular Application

## Setting up and running the Angular app

1. Install Node.js 22 from the [official website](https://nodejs.org/).
2. Install Angular CLI globally by running the following command:
   ```sh
   npm install -g @angular/cli
   ```
3. Navigate to the `frontend` directory of the project.
4. Install the project dependencies by running:
   ```sh
   npm install
   ```
5. Start the development server by running:
   ```sh
   ng serve
   ```
6. Open your browser and navigate to `http://localhost:4200` to see the running application.

## Building the Angular app for production

1. Navigate to the `frontend` directory of the project.
2. Build the Angular app for production by running:
   ```sh
   ng build --prod
   ```
3. The production-ready files will be generated in the `../backend/wwwroot` directory.
