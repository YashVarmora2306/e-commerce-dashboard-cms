
---

# E-Commerce Admin Dashboard

This is an E-Commerce Admin Dashboard built with Next.js, TypeScript, and Tailwind CSS. The application allows users to manage their e-commerce stores, including products, categories, sizes, colors, and orders.
---

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
   - [Auth Endpoints](#auth-endpoints)
   - [Product Endpoints](#product-endpoints)
   - [Category Endpoints](#category-endpoints)
   - [Size Endpoints](#size-endpoints)
   - [Color Endpoints](#color-endpoints)
- [What I Learned](#what-i-learned)

---

## Features

- **User Authentication**: Secure user authentication using Clerk.
- **Store Management**: Create and manage multiple stores.
- **Product Management**: Add, edit, and delete products with images, categories, sizes, and colors.
- **Order Management**: View and manage orders placed in the store.
- **Category Management**: Create and manage product categories.
- **Size and Color Management**: Manage product sizes and colors.
- **Billboard Management**: Manage promotional billboards for the store.
- **Responsive Design**: Fully responsive UI built with Tailwind CSS.

---

## Technologies Used

- **Next.js**: A React framework for server-side rendering and static site generation.
- **TypeScript**: A superset of JavaScript that adds static types.
- **Tailwind CSS**: A utility-first CSS framework for styling.
- **Prisma**: An ORM for database management.
- **Clerk**: User authentication and management.
- **React Hook Form**: For managing form state and validation.
- **Axios**: For making HTTP requests.

---

## Getting Started

### Prerequisites

- Node.js (v14 or later)
- npm

### Installation

1. **Install dependencies**:

  ```bash
  cd ecommerce-admin
  npm install
  ```

2. **Set up environment variables**:
   Create a `.env` file in the root of the project and add the following variables:

   ```env
   #Clerk Configuration
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key

   # Clerk Redirect URLs
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up

   # Prisma Configuration (Automatically used by Prisma)
   DATABASE_URL=your_database_connection_string

   # Cloudinary Configuration
   NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name

   # Stripe Configuration
   STRIPE_API_KEY=your_stripe_api_key
   STRIPE_WEBHOOK_SECRET=your_stripe_webhook_secret

   # Frontend Store URL
   FRONTEND_STORE_URL=http://localhost:3001

   ```

3. **Run the development server**:

     ```bash
     npm run dev
     ```

4. **Open the app**:  
   Navigate to [http://localhost:3000](http://localhost:3000) in your browser.

---

## Usage

- **Sign up** or **sign in** using Clerk.
- **Create a new store** or select an existing one.
- **Manage products**, categories, sizes, colors, and orders from the dashboard.

---

## API Endpoints

### Auth Endpoints

| Method | Endpoint     | Description          |
| ------ | ------------ | -------------------- |
| POST   | /user/signin | Log in a user.       |
| POST   | /user/signup | Register a new user. |

### Product Endpoints

| Method | Endpoint                    | Description                              |
| ------ | --------------------------- | ---------------------------------------- |
| GET    | /api/[storeId]/products     | Fetch all products for a specific store. |
| GET    | /api/[storeId]/products/:id | Fetch a specific product by ID.          |
| POST   | /api/[storeId]/products     | Create a new product.                    |
| PATCH  | /api/[storeId]/products/:id | Update a product.                        |
| DELETE | /api/[storeId]/products/:id | Delete a product.                        |

### Category Endpoints

| Method | Endpoint                      | Description                                |
| ------ | ----------------------------- | ------------------------------------------ |
| GET    | /api/[storeId]/categories     | Fetch all categories for a specific store. |
| GET    | /api/[storeId]/categories/:id | Fetch a specific category by ID.           |
| POST   | /api/[storeId]/categories     | Create a new category.                     |
| PATCH  | /api/[storeId]/categories/:id | Update a category.                         |
| DELETE | /api/[storeId]/categories/:id | Delete a category.                         |

### Size Endpoints

| Method | Endpoint                 | Description                           |
| ------ | ------------------------ | ------------------------------------- |
| GET    | /api/[storeId]/sizes     | Fetch all sizes for a specific store. |
| GET    | /api/[storeId]/sizes/:id | Fetch a specific size by ID.          |
| POST   | /api/[storeId]/sizes     | Create a new size.                    |
| PATCH  | /api/[storeId]/sizes/:id | Update a size.                        |
| DELETE | /api/[storeId]/sizes/:id | Delete a size.                        |

### Color Endpoints

| Method | Endpoint                  | Description                            |
| ------ | ------------------------- | -------------------------------------- |
| GET    | /api/[storeId]/colors     | Fetch all colors for a specific store. |
| GET    | /api/[storeId]/colors/:id | Fetch a specific color by ID.          |

---

## What I Learned

Throughout the development of this E-Commerce Admin Dashboard, I have gained valuable knowledge and hands-on experience in various technologies and concepts. Below are the key takeaways:

- **Next.js & TypeScript**:

  - Learned how to leverage the power of **Next.js** for server-side rendering and static site generation, ensuring better SEO and faster page loads.
  - Gained expertise in using **TypeScript** to add type safety to JavaScript, making the code more robust and maintainable.

- **Tailwind CSS**:

  - Deepened my understanding of **Tailwind CSS**, a utility-first CSS framework, to create responsive and customizable UIs quickly.
  - Mastered responsive design techniques using Tailwind, ensuring the dashboard looks great across all screen sizes.

- **Clerk for Authentication**:

  - Implemented **Clerk** for secure and easy user authentication, learning about its capabilities such as sign-up, sign-in, and managing user sessions.
  - Understood the importance of securing routes and pages based on user authentication and the role-based access control mechanisms in Clerk.

- **Prisma ORM**:

  - Used **Prisma** to manage database interactions, learning how to define models and perform CRUD operations efficiently.
  - Gained experience with database migrations and schema design for scalable applications.

- **Stripe Integration**:

  - Integrated **Stripe** for handling payments, understanding how to securely store API keys and process payments in a production environment.
  - Learned how to manage Stripe webhook events for processing different payment statuses.

- **API Design & RESTful Principles**:

  - Created and documented RESTful API endpoints for managing products, categories, sizes, colors, and orders.
  - Gained practical knowledge of API design principles, such as route conventions, HTTP methods, and response structures.

- **Form Handling with React Hook Form**:

  - Implemented **React Hook Form** for efficient form handling and validation, ensuring a smooth user experience with minimal re-renders.

- **State Management with React**:

  - Developed complex state management solutions using React's `useState` and `useEffect` hooks, improving the app’s performance and scalability.

- **Middleware & Security**:

  - Implemented middleware in Next.js for route protection and ensuring only authenticated users can access certain parts of the application.
  - Understood the importance of handling sensitive data securely, including using environment variables for keys and secrets.

- **Project Structure & Clean Code**:
  - Applied a modular folder structure to separate concerns between components, API routes, and actions, ensuring scalability and maintainability.
  - Followed best practices for writing clean, reusable, and testable code, making future enhancements easier.

---
