# 🌍 Sustainable Tourism Project

## Overview

This project focuses on **sustainable tourism** in Barcelona, visualizing tourist density, noise levels, and points of interest. The application consists of three main components: **backend**, **frontend**, and **data processing**.

## ⚙️ Backend Setup
This project uses Java 21

1. **Navigate to folder**:
    ```bash
    cd ../backend
    ```
2. **Install dependencies** (Maven is required):
    ```bash
    mvn install
    ```
3. **Run the backend**:
    ```bash
    mvn spring-boot:run
    ```
    The backend will be available at `http://localhost:8080`.

### Database Setup

1. **Install MySQL** if not already installed:
    ```bash
    sudo apt install mysql-server
    ```
2. **Create the database**:
    ```bash
    CREATE DATABASE touristdb;
    ```
3. **Configure backend**: Update the database configuration in `application.properties` to point to your local MySQL instance:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/touristdb
    spring.datasource.username=root
    spring.datasource.password=yourpassword
    ```

### Implemented Endpoints

- `GET /api/culturalPlace/all`: Retrieves all cultural places.
- `GET /api/turistConcentration/all`: Retrieves all tourist concentration points.
- `GET /api/noise/all`: Retrieves all tourist concentration points.

## 🎨 Frontend Setup (TurismeSostenible)

This project uses [Angular CLI](https://github.com/angular/angular-cli) version 17.1.2.

### Development Server

Run `npm install` to install dependencies.

### Development Server

Run `ng serve` to start a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload when source files change.

### Code Scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

### Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

### Development Server

Run `npm run start` to run the app. The application will be available at http://localhost4200

### Running Unit Tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

### Running End-to-End Tests

Run `ng e2e` to execute end-to-end tests. To use this command, add a package that implements end-to-end testing capabilities.

### Further Help

For more information on Angular CLI, use `ng help` or check the [Angular CLI Overview and Command Reference](https://angular.io/cli).

## 📊 Data Sources

The project uses data from **Open Data Barcelona** to analyze tourism patterns:

- **Tourist Density Areas**  
  Source: [Intensitat d'Activitat Turística](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/intensitat-activitat-turistica)  
  Description: Areas with high tourist concentrations.

- **Cultural Points of Interest**  
  Source: [Punts d'Interès Turístic](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/punts-informacio-turistica)  
  Description: Key cultural sites in Barcelona.

- **Environmental Noise Monitoring Data**  
  Source: [Xarxa Soroll](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/xarxasoroll-equipsmonitor-dades)  
  Description: Daily noise levels in the city.

- **Geographic Data for Noise Sensors**  
  Source: [Geographic Data for Noise Sensors](https://opendata-ajuntament.barcelona.cat/data/ca/dataset/xarxasoroll-equipsmonitor-instal)  
  Description: Geographic information for noise sensors.

## 🛠️ Data Processing & Modelling

Data processing includes **cleaning** and **feature extraction** to prepare datasets for use:

- **Tourist Concentration**: Simulated **daily tourist density** for 2019.
- **Cultural Sites**: Cleaned and categorized tourist sites by relevance.
- **Noise Levels**: Averaged **daily noise levels** and combined with the geographic location of sensors.

The final datasets display **tourist activity** and **environmental conditions** on an interactive map.

## 🚀 Implementation

### Steps to Run the Project

1. Download the raw data from the indicated sources and place it in the `data/` folder.
2. Create the environment using the provided `environment.yml` file:
    ```bash
    conda env create -f environment.yml
    ```
3. Activate the environment:
    ```bash
    conda activate tourism-env
    ```
4. Run the main script:
    ```bash
    python main.py
    ```
