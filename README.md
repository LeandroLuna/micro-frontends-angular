# Micro Frontends with Angular 18 and Module Federation

This project demonstrates a simple implementation of Micro Frontends using Angular 18 and Module Federation. The project consists of two applications working together to showcase dynamic component loading capabilities.

## Project Structure

### Host Application (port 4200)
- Main container application
- Implements base layout and navigation
- Dynamically loads components from micro-frontend
- Demonstrates seamless integration with remote modules

### Micro Application (port 4201)
- Micro-frontend that exposes components to the host application
- Implements an example component (HelloWorld)
- Supports on-the-fly changes that are automatically reflected in the host application
- Demonstrates deployment and development independence

## Technologies Used

- Angular 18
- Module Federation
- Docker & Docker Compose
- Nginx

## How to Run

The project uses Docker Compose for easy execution. To start both applications, run:

```bash
docker-compose up --build
```

After execution, you can access:
- Host Application: http://localhost:4200
- Micro Frontend: http://localhost:4201

## Features

- Navigation between local and remote components
- Dynamic loading of micro-frontend components
- Support for on-the-fly component changes
- Module Federation integration demonstration

## Architecture

The project implements the Micro Frontends pattern using Webpack 5's Module Federation, enabling:
- Dynamic component loading
- Independent development
- Independent deployment
- Dependency sharing
- Seamless application integration

## Development

For local development without Docker:

1. Start the micro-frontend:
```bash
cd micro
npm install
npm start
```

2. Start the host application:
```bash
cd host
npm install
npm start
```