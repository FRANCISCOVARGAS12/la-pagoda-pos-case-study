# La Pagoda POS

Restaurant POS system built for a real Asian restaurant in Mexico.

Status: delivered and deployed on a VPS with Docker and Nginx.

This project is my strongest proof of work because it solves a real business workflow: tables, orders, menu, sales, payments, tips, reports, and daily closing.

## Why This Project Matters

Most student portfolios show tutorial apps.

La Pagoda POS is different:

- Built for a real restaurant client
- Designed around a real restaurant operation
- Deployed to a real VPS
- Connected to a PostgreSQL database
- Split into backend, admin panel, and waiter app

## Architecture

```txt
                    Restaurant Staff
                         |
        -------------------------------------
        |                                   |
  Flutter Waiter App                 Angular Admin Panel
  tables, orders, flow               menu, users, reports
        |                                   |
        --------------- HTTPS/API ----------
                         |
                  Spring Boot API
       auth, sales, products, payments, reports
                         |
                    PostgreSQL
       catalogos, operacion, ventas, reportes
                         |
                    VPS + Docker
                         |
                       Nginx
```

## Main Modules

### Backend API

Built with Java 21 and Spring Boot.

Responsibilities:

- Authentication flow
- Menu and product management
- Table management
- Waiter/order workflow
- Sales and payment handling
- Tips and daily summaries
- Daily closing flow
- Error handling through a global exception layer
- REST endpoints for the admin panel and waiter app
- WebSocket support for real-time updates

Technical details found in the project:

- 24 REST controllers
- 18 JPA entities
- PostgreSQL schemas:
  - `catalogos`
  - `operacion`
  - `ventas`
  - `reportes`
- Spring Data JPA
- Spring Security
- Bean Validation
- WebSocket/STOMP support
- Dockerfile for deployment

### Admin Panel

Built with Angular.

Responsibilities:

- Admin login
- Product/menu management
- User management
- Sales view
- Tips view
- Top products view
- Restaurant configuration
- Toast notifications and API error handling
- PDF/report support
- WebSocket client support

### Waiter App

Built with Flutter.

Responsibilities:

- Waiter login
- Table map
- Menu screen
- Order summary
- Order grouping
- Family dish billing logic
- Sale lookup
- PDF/printing support

## Deployment

The system was deployed on a VPS using:

- Docker for backend packaging
- Nginx as web server/reverse proxy
- PostgreSQL as the production database
- Linux server environment

This is important because the project was not only coded. It was shipped.

## What I Learned

- Turning restaurant requirements into database entities and API endpoints
- Building a multi-part system with backend, web admin, and mobile/tablet app
- Deploying software to a real VPS
- Handling real data instead of demo data
- Thinking about reliability, errors, users, payments, and business flow

## Tech Stack

- Java 21
- Spring Boot
- PostgreSQL
- Angular
- Flutter
- Docker
- Nginx
- Linux VPS

## Screenshots

Add screenshots here:

- Admin dashboard
- Product/menu management
- Sales/report screen
- Waiter table map
- Order summary screen
- VPS/Nginx deployment proof without exposing secrets


## Result

La Pagoda POS proves that I can build more than visual demos. I can build and deploy practical software for a real business.
