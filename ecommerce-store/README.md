
---
# E-commerce Store

This is a **Next.js** project bootstrapped with `create-next-app`. It is designed to be a fully functional e-commerce store that allows users to browse products, add them to a shopping cart, and proceed to checkout.
---

## Table of Contents

- [Getting Started](#getting-started)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [API Endpoints](#api-endpoints)
- [What I Learned](#what-i-learned)

---

## Getting Started

To get started with the project, follow these steps:

### Prerequisites

- Node.js (v14 or later)
- npm

### Install the dependencies:

```bash
cd ecommerce-store
npm install
```

### Set up environment variables
```env
NEXT_PUBLIC_API_URL=your_admin_store_url 
#NEXT_PUBLIC_API_URL=http://localhost:3000/api/userId

```


### Run the development server:

```bash
npm run dev
```

Open [http://localhost:3001](http://localhost:3001) in your browser to see the application.

---

## Features

- User-friendly interface for browsing products.
- Product filtering by category, size, and color.
- Shopping cart functionality with add/remove items.
- Modal previews for product details.
- Responsive design for mobile and desktop views.

---

## Technologies Used

- **Next.js**: A React framework for server-side rendering and static site generation.
- **TypeScript**: For type safety and better development experience.
- **Tailwind CSS**: For styling and responsive design.
- **Zustand**: For state management.
- **Axios**: For making HTTP requests.
- **React Hot Toast**: For notifications.

---

## API Endpoints

### Auth Endpoints

| Method | Endpoint       | Description          |
| ------ | -------------- | -------------------- |
| POST   | `/auth/signin` | Log in a user.       |
| POST   | `/auth/signup` | Register a new user. |

### Product Endpoints

| Method | Endpoint            | Description                     |
| ------ | ------------------- | ------------------------------- |
| GET    | `/api/products`     | Fetch all products.             |
| GET    | `/api/products/:id` | Fetch a specific product by ID. |
| POST   | `/api/products`     | Create a new product.           |
| PATCH  | `/api/products/:id` | Update a product.               |
| DELETE | `/api/products/:id` | Delete a product.               |

### Category Endpoints

| Method | Endpoint              | Description                      |
| ------ | --------------------- | -------------------------------- |
| GET    | `/api/categories`     | Fetch all categories.            |
| GET    | `/api/categories/:id` | Fetch a specific category by ID. |
| POST   | `/api/categories`     | Create a new category.           |
| PATCH  | `/api/categories/:id` | Update a category.               |
| DELETE | `/api/categories/:id` | Delete a category.               |

### Size Endpoints

| Method | Endpoint         | Description                  |
| ------ | ---------------- | ---------------------------- |
| GET    | `/api/sizes`     | Fetch all available sizes.   |
| GET    | `/api/sizes/:id` | Fetch a specific size by ID. |
| POST   | `/api/sizes`     | Create a new size.           |
| PATCH  | `/api/sizes/:id` | Update a size.               |
| DELETE | `/api/sizes/:id` | Delete a size.               |

### Color Endpoints

| Method | Endpoint          | Description                   |
| ------ | ----------------- | ----------------------------- |
| GET    | `/api/colors`     | Fetch all available colors.   |
| GET    | `/api/colors/:id` | Fetch a specific color by ID. |
| POST   | `/api/colors`     | Create a new color.           |
| PATCH  | `/api/colors/:id` | Update a color.               |
| DELETE | `/api/colors/:id` | Delete a color.               |

### Billboards Endpoints

| Method | Endpoint          | Description           |
| ------ | ----------------- | --------------------- |
| GET    | `/api/billboards` | Fetch all billboards. |

## What I Learned

During the development of this e-commerce store, I gained hands-on experience with the following technologies and concepts:

- **Next.js & TypeScript**: Learned to create full-stack applications with **Next.js** and **TypeScript**, leveraging its features like static site generation (SSG) and server-side rendering (SSR).
- **Tailwind CSS**: Mastered styling with **Tailwind CSS**, applying a utility-first approach to create responsive layouts that adapt to various screen sizes.

- **State Management with Zustand**: Used **Zustand** for managing global state, learning how to implement a centralized store and manage complex state logic across components.

- **API Design with RESTful Principles**: Designed and implemented a RESTful API structure for managing products, categories, sizes, colors, and billboards, following standard HTTP methods and response codes.

- **Authentication**: Integrated a simple **authentication system** using custom APIs for user sign-in and sign-up.

- **Responsive Design**: Applied **responsive web design** principles to ensure the store works seamlessly on both mobile and desktop devices.

- **API Integration with Axios**: Used **Axios** for making API calls, handling HTTP requests, and managing responses with proper error handling.

---
