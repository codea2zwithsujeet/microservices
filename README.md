# Codea2zWithSujeet Backend Services

A collection of microservices built with .NET 8 and EF Core using a code-first approach, powering the backend for the Codea2zWithSujeet website. This repository includes separate projects for Identity, Blog, Portfolio, and Newsletter functionalities, each following a modular architecture for scalability and maintainability.

## Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Database Migrations](#database-migrations)
- [Running the Services](#running-the-services)
- [Development Guidelines](#development-guidelines)
- [CI/CD](#cicd)
- [Contributing](#contributing)
- [License](#license)

## Overview

**Codea2zWithSujeet** is designed to support a website featuring a portfolio, blog, and newsletter functionalities. Each microservice is a self-contained project with its own API, domain models, and EF Core data access layer, allowing independent development, testing, and deployment.

## Architecture

The backend is composed of the following microservices:

- **IdentityService:**  
  Manages user authentication, registration, and authorization.

- **BlogService:**  
  Handles blog post creation, editing, commenting, and SEO optimizations.

- **PortfolioService:**  
  Manages portfolio items, including project details and media uploads.

- **NewsletterService:**  
  Provides endpoints for newsletter subscriptions, campaign management, and email scheduling.

An API Gateway (e.g., Ocelot or YARP) can be used to route requests to the appropriate microservice while handling cross-cutting concerns like authentication and logging.

## Project Structure

The solution is organized as follows:


Each microservice follows a similar folder structure:

- **Controllers:** API controllers handling HTTP requests.
- **Data:** EF Core `DbContext` and migrations.
- **Domain:** Domain models (entities).
- **DTOs:** Data Transfer Objects for API communications.
- **Repositories:** Interfaces and classes for data access.
- **Services:** Business logic and service layer.

## Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [PostgreSQL](https://www.postgresql.org/) (or a Dockerized PostgreSQL instance)
- [Docker](https://www.docker.com/) (optional, for containerized deployments)
- EF Core CLI Tools:
  ```bash
  dotnet tool install --global dotnet-ef



**This project is licensed under the MIT License.**
