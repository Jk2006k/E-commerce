# ShopHub - Full-Featured E-Commerce Platform

A modern and elegant e-commerce website built with React, TypeScript, and Tailwind CSS. ShopHub is basically a complete shopping platform designed to give users an intuitive and seamless online shopping experiance.

## Overview

ShopHub is a fully functional e-commerce platform that brings together best practices in modern web development with a user-centric design. Whether your building your first online store or looking for a solid foundation to expand upon, ShopHub has everything you need to get started.

Live Storefront Name: ShopHub
Platform Built With: React, TypeScript, Vite, Tailwind CSS
Data Management: Context API and Local Storage

## Features

Core E-Commerce Features

Product Catalog
- Browse products across multiple categories (Electronics, Fashion, Home and Kitchen, Books, Sports and Outdoors, Beauty and Personal Care)
- Detailed product pages with descriptions, specifications, prising, and images
- Product ratings and review counts
- Stock quantity tracking

Shopping Cart
- Add or remove items from cart
- Adjust quantities easily
- Real-time cart total calculation
- Cart persistence across browser sessions using Local Storage
- Slide-out cart sidebar for quick access when your shopping

Wishlist
- Save favorite products for later
- Add or remove from wishlist with one click
- Persistent wishlist storage
- Quick access via navigation menu

User Authentication
- User registration and login modal
- Session persistence
- User profile management
- Support for guest checkout if you dont want to register

Checkout and Orders
- Complete checkout flow
- Order history tracking
- Order status management (pending, processing, shipped, delivered, cancelled)
- Shipping and billing address management
- Order summary with itemized details

User Account
- User profile management
- Saved adresses for quick checkout
- Order history to track past purcases
- Purchase tracking and order updates

Product Search and Filtering
- Real-time search functionality
- Category-based filtering
- Product discovery features to help customers find what there looking for

## Project Structure

Here's how the project is organized:

E-commerce/project/
- public folder contains static assets
- src folder contains all the source code
  - components folder has reusable React components like Header.tsx (navigation with search), CartSidebar.tsx (shopping cart), and AuthModal.tsx (login/register)
  - pages folder contains the main page components like HomePage.tsx, ProductsPage.tsx, ProductDetailPage.tsx, CheckoutPage.tsx, WishlistPage.tsx, and AccountPage.tsx
  - context folder has AppContext.tsx for global state management
  - data folder contains mockData.ts with sample products and categories
  - types folder has index.ts with TypeScript definitions
  - App.tsx is the main app component
  - main.tsx is the React DOM entry point
  - index.css contains global styles
- package.json for dependencies and scripts
- vite.config.ts for Vite settings
- tailwind.config.js for Tailwind customization
- tsconfig.json for TypeScript config
- eslint.config.js for linting rules

---

##  Technical Architecture

### State Management

The app uses **React Context API** for global state management, handling:

```typescript
- User authentication state
- Shopping cart items and totals
- Wishlist items
- Order history
- UI state (modals, sidebars)
- Search queries
```

All data is automatically persisted to browser **Local Storage**, ensuring users don't lose their cart or wishlist when they close the browser.

### Type Safety

## Technical Architecture

State Management

The app uses React Context API for global state management. It handles user authentication, shopping cart items and totals, wishlist items, order history, UI state like modals and sidebars, and search queries.

All data is automaticly persisted to browser Local Storage, so users dont lose their cart or wishlist when they close the browser.

Type Safety

Full TypeScript support with comprehensive type definitions:
- User - User profile and authentication
- Product - Product details and metadata
- Order - Order information and status
- CartItem - Cart item with quantity
- WishlistItem - Wishlist entries
- Address - Shipping and billing addresses
- Review - Product reviews and ratings

Routing

Client-side navigation using React state management (no traditional router library). The App component handles page switching and passes navigation callbacks to child components.

## UI and Styling

Framework: Tailwind CSS 3.x with responsive design
Icons: Lucide React (modern, consistent icon library)
Design Philosophy: Mobile-first, accessible, and user-friendly
Responsive: Optimized for desktop, tablet, and mobile devices

##
### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-repo/E-Commerce-Website.git
   cd E-commerce/project
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```
Frontend
- React 18.3 - UI library
- TypeScript 5.5 - Type safety
- Vite 5.4 - Lightning-fast build tool
- Tailwind CSS 3.4 - Utility-first CSS framework
- Lucide React 0.344 - Beautiful icon library

Integrations
- Supabase 2.57 - Backend services (configured, ready to use)

Development Tools
- ESLint 9.9 - Code linting
- PostCSS 8.4 - CSS processing
- Autoprefixer - Vendor prefixes for CSS
- TypeScript ESLint - TypeScript linting

## Getting Started

Prerequisites
- Node.js version 16 or higher
- npm or yarn package manager

Installation Steps

1. Clone the repository

git clone https://github.com/your-repo/E-Commerce-Website.git
cd E-commerce/project

2. Install dependencies

npm install

3. Start development server

npm run dev

The site will be available at http://localhost:3000

4. Build for production

npm run build

5. Preview production build

npm run preview

##

## 🔌 Backend Integration (Supabase)

The project is set up with **Supabase** authentication and database support. Currently, mock data is used for development. To connect to a real Supabase instance:

1. Create a Supabase project at https://supabase.com
2. Add your credentials to a `.env` file:
   ```env
   VITE_SUPABASE_URL=your_supabase_url
npm run dev - Start development server with hot reload
npm run build - Create optimized production build
npm run lint - Check code quality with ESLint
npm run preview - Preview production build locally
npm run typecheck - Verify TypeScript types

## Product Categories

The platform comes with 6 featured categories that you can browse through:

1. Electronics - Latest gadgets and electronic devices
2. Fashion - Trendy clothing and accessories
3. Home and Kitchen - Everything for your home
4. Books - Bestsellers and classics
5. Sports and Outdoors - Gear for active lifestyles
6. Beauty and Personal Care - Cosmetics and personal care products

## Data Persistence

All user data is stored in the browser's Local Storage, so information is saved between sessions:

Cart - Automaticly saved when items are added or removed
Wishlist - Persists favorite items across sessions
Orders - Historical order data stored locally
User Profile - User authentication state is maintained

Note: Local Storage persists data on a per-device basis. To implement cloud synchronization, you'll need to integrate Supabase or another backend service.

## Backend Integration with Supabase

The project is set up with Supabase authentication and database support. Right now, mock data is used for development. To connect to a real Supabase instance, follow these steps:

1. Create a Supabase project at https://supabase.com
2. Add your credentials to a .env file
3. Update the AppContext to use Supabase authentication
4. Connect to Supabase database for products and orders

## Mock Data

The project includes comprehensive mock data for development:

Over 20 Products with detailed descriptions, prising, and images
Multiple Categories to showcase filtering and navigation
Product Specifications showing extensible data structure
Review Data with ratings and verified purchases

Mock data is loaded from src/data/mockData.ts and can be easily replaced with API calls.

## Key Components Breakdown

Header Component
This component handles the main navigation with product categories, search functionality, user profile menu, cart icon with item count, wishlist access, and a mobile hamburger menu for responsive design.

CartSidebar Component
The shopping cart appears in a sliding drawer on the side and shows all the items in the cart. It lets you adjust item quantities, remove items, calculates the cart total, and has a button to proceed to checkout.

AuthModal Component
This is where users can login or register. It has a user login interface, registration form, and handles session management.

Pages

HomePage - This is the landing page with a hero banner and promotions, featured products showcase, category highlights, and call-to-action sections.

ProductsPage - Shows a product grid display with category filtering, product cards with pricing, and buttons to add items to cart or wishlist.

ProductDetailPage - The full product information page with an image gallery, detailed specifications, customer reviews section, quantity selector, and options to add to cart or wishlist.

CheckoutPage - This is where customers review their cart, enter shipping address, manage billing address, review the order summary, enter payment information, and get order confirmation.

WishlistPage - Display saved items, move items to cart, and remove from wishlist.

AccountPage - User profile information, address management, order history, and account settings.

## Customization

Change Store Name
Update the store name from "ShopHub" in these places:
- src/App.tsx for header branding
- index.html for the page title

Modify Categories
Edit src/data/mockData.ts to add or remove product categories.

Update Colors
Customize colors in tailwind.config.js to match your brand.

Add Products
Add new products to the mock data array in src/data/mockData.ts, or connect to a backend API.

## Security Considerations

Authentication - Implement secure token-based authentication with Supabase
Payment Processing - Use a PCI-compliant payment gateway like Stripe or PayPal
HTTPS - Always deploy over HTTPS in production
Input Validation - Implement server-side validation for all user inputs
CORS - Configure proper CORS headers for API requests
Environment Variables - Never commit sensitive keys to version control

## Performance Optimizations

Vite - Fast bundling and hot module replacement
Image Optimization - External image URLs (consider using a CDN)
Code Splitting - Each page component can be code-split for faster loading
Tree Shaking - Unused code is automaticly removed during build
Lazy Loading - Components only load when needed

## Troubleshooting

Port 3000 already in use?
Edit vite.config.ts and change the port number to something like 3001 or 3002.

Local Storage not working?
Clear browser cache and LocalStorage, then reload the app.

Styles not loading?
Make sure Tailwind CSS is properly configured. Run npm run build and check for errors.

## Deployment

Build Optimization

npm run build

This creates an optimized build in the dist folder.

Deploy to Popular Platforms

Vercel (Recommended for React and Vite projects)
npm i -g vercel
vercel

Netlify
- Connect your Git repository
- Build command: npm run build
- Publish directory: dist

Docker (Optional)
Create a Dockerfile for containerized deployments.

## Resources and Documentation

- React Documentation - https://react.dev
- TypeScript Handbook - https://www.typescriptlang.org/docs
- Tailwind CSS Docs - https://tailwindcss.com/docs
- Vite Guide - https://vitejs.dev/guide
- Supabase Docs - https://supabase.com/docs
- Lucide Icons - https://lucide.dev

## Contributing

We welcome contributions! Heres how to get involved:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

Code Style Guidelines
- Use TypeScript for type safety
- Follow existing code conventions
- Run npm run lint before committing
- Add comments for complex logic

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Future Enhancements

Here are some ideas for future features we could add:

- User reviews and ratings system
- Product recommendations engine
- Advanced search and filtering
- Multiple payment gateway integration
- Email notifications
- Coupon and discount codes
- Product variants like size and color
- Inventory management dashboard
- Admin panel for store management
- Analytics and reporting
- Push notifications
- Social media integration
- Live chat support
- Multi-language support
- Dark mode theme
