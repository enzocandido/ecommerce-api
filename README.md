# E-Commerce API

A RESTful API for e-commerce applications built with Express.js, TypeScript, and PostgreSQL. This API provides endpoints for product management, user authentication, order processing, and Stripe payment integration.

## Features

- **Product Management**: Create, read, update, and delete products
- **User Authentication**: Register, login, and JWT-based authentication
- **Order Processing**: Create and manage orders
- **Payment Integration**: Process payments using Stripe
- **Database**: PostgreSQL with Drizzle ORM
- **API Documentation**: Detailed API endpoints
- **TypeScript**: Type-safe code

## Tech Stack

- **Backend**: Node.js, Express.js
- **Language**: TypeScript
- **Database**: PostgreSQL
- **ORM**: Drizzle ORM
- **Authentication**: JWT, bcrypt
- **Payment**: Stripe
- **Deployment**: Serverless ready

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- PostgreSQL database
- Stripe account (for payment processing)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/enzocandido/ecommerce-api.git
   cd ecommerce-api
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up environment variables:

   ```bash
   cp .env.example .env
   ```

   Then edit `.env` with your configuration details.

4. Generate database migrations:

   ```bash
   npm run db:generate
   ```

5. Run migrations:
   ```bash
   npm run db:migrate
   ```

### Development

Start the development server:

```bash
npm run dev
```

The API will be available at `http://localhost:3001`.

### Database Management

- Generate migrations: `npm run db:generate`
- Run migrations: `npm run db:migrate`
- Explore database with Drizzle Studio: `npm run db:studio`

## API Endpoints

### Authentication

- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login and receive an access token

### Products

- `GET /products` - Get all products
- `GET /products/:id` - Get a specific product
- `POST /products` - Create a new product
- `PUT /products/:id` - Update a product
- `DELETE /products/:id` - Delete a product

### Orders

- `GET /orders` - Get user's orders
- `GET /orders/:id` - Get a specific order
- `POST /orders` - Create a new order

### Payments

- `POST /stripe/create-payment-intent` - Create a payment intent
- `POST /stripe/webhook` - Handle Stripe webhook events

## Deployment

This project is configured for serverless deployment. The `handler` export in `index.ts` can be used with services like AWS Lambda, Vercel, or Netlify.
