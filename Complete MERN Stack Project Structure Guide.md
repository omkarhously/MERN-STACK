# **Complete MERN Stack Project Structure Guide**

## **📚 Table of Contents**

1. [Overview](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#overview)  
2. [Prerequisites](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#prerequisites)  
3. [Complete Folder Structure](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#complete-folder-structure)  
4. [Backend Structure Explained](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#backend-structure-explained)  
5. [Frontend Structure Explained](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#frontend-structure-explained)  
6. [Step-by-Step Setup Guide](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#step-by-step-setup-guide)  
7. [Development Environment](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#development-environment)  
8. [Testing Setup](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#testing-setup)  
9. [Production Deployment](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#production-deployment)  
10. [Environment Variables](https://lmarena.ai/c/019b26fe-8e02-77a1-8ea1-d21080a30933#environment-variables)

---

## **📋 Overview**

text

MERN Stack Components:  
├── M \- MongoDB    → Database (NoSQL)  
├── E \- Express.js → Backend Framework  
├── R \- React.js   → Frontend Library  
└── N \- Node.js    → Runtime Environment

---

## **🔧 Prerequisites**

Bash

\# Required Software  
\- Node.js (v18+ recommended)  
\- npm or yarn  
\- MongoDB (local or Atlas)  
\- Git  
\- VS Code (recommended)

\# Verify Installation  
node \--version  
npm \--version  
mongod \--version  
git \--version

---

## **📁 Complete Folder Structure**

text

mern-project/  
│  
├── 📁 backend/                          \# Backend Application  
│   │  
│   ├── 📁 src/                          \# Source Code  
│   │   │  
│   │   ├── 📁 config/                   \# Configuration Files  
│   │   │   ├── db.js                    \# Database connection  
│   │   │   ├── cloudinary.js            \# Cloudinary setup  
│   │   │   ├── email.js                 \# Email configuration  
│   │   │   ├── redis.js                 \# Redis configuration  
│   │   │   ├── passport.js              \# Passport.js strategies  
│   │   │   └── index.js                 \# Config exports  
│   │   │  
│   │   ├── 📁 controllers/              \# Request Handlers  
│   │   │   ├── authController.js        \# Authentication logic  
│   │   │   ├── userController.js        \# User CRUD operations  
│   │   │   ├── productController.js     \# Product operations  
│   │   │   ├── orderController.js       \# Order management  
│   │   │   ├── paymentController.js     \# Payment processing  
│   │   │   └── index.js                 \# Controllers export  
│   │   │  
│   │   ├── 📁 models/                   \# Database Models  
│   │   │   ├── User.js                  \# User schema  
│   │   │   ├── Product.js               \# Product schema  
│   │   │   ├── Order.js                 \# Order schema  
│   │   │   ├── Category.js              \# Category schema  
│   │   │   ├── Review.js                \# Review schema  
│   │   │   └── index.js                 \# Models export  
│   │   │  
│   │   ├── 📁 routes/                   \# API Routes  
│   │   │   ├── authRoutes.js            \# /api/auth/\*  
│   │   │   ├── userRoutes.js            \# /api/users/\*  
│   │   │   ├── productRoutes.js         \# /api/products/\*  
│   │   │   ├── orderRoutes.js           \# /api/orders/\*  
│   │   │   ├── paymentRoutes.js         \# /api/payments/\*  
│   │   │   ├── uploadRoutes.js          \# /api/upload/\*  
│   │   │   └── index.js                 \# Routes combiner  
│   │   │  
│   │   ├── 📁 middleware/               \# Custom Middleware  
│   │   │   ├── authMiddleware.js        \# JWT verification  
│   │   │   ├── errorMiddleware.js       \# Error handling  
│   │   │   ├── validationMiddleware.js  \# Input validation  
│   │   │   ├── uploadMiddleware.js      \# File upload (multer)  
│   │   │   ├── rateLimitMiddleware.js   \# Rate limiting  
│   │   │   ├── corsMiddleware.js        \# CORS configuration  
│   │   │   ├── loggerMiddleware.js      \# Request logging  
│   │   │   └── index.js                 \# Middleware export  
│   │   │  
│   │   ├── 📁 services/                 \# Business Logic  
│   │   │   ├── authService.js           \# Auth business logic  
│   │   │   ├── emailService.js          \# Email sending  
│   │   │   ├── paymentService.js        \# Payment processing  
│   │   │   ├── uploadService.js         \# File upload logic  
│   │   │   ├── notificationService.js   \# Push notifications  
│   │   │   └── index.js                 \# Services export  
│   │   │  
│   │   ├── 📁 utils/                    \# Utility Functions  
│   │   │   ├── apiResponse.js           \# Standardized responses  
│   │   │   ├── apiError.js              \# Custom error class  
│   │   │   ├── asyncHandler.js          \# Async error wrapper  
│   │   │   ├── generateToken.js         \# JWT generation  
│   │   │   ├── validators.js            \# Validation helpers  
│   │   │   ├── helpers.js               \# General helpers  
│   │   │   ├── constants.js             \# App constants  
│   │   │   ├── logger.js                \# Winston logger  
│   │   │   └── index.js                 \# Utils export  
│   │   │  
│   │   ├── 📁 validators/               \# Request Validators  
│   │   │   ├── authValidator.js         \# Auth validation rules  
│   │   │   ├── userValidator.js         \# User validation  
│   │   │   ├── productValidator.js      \# Product validation  
│   │   │   └── index.js                 \# Validators export  
│   │   │  
│   │   ├── 📁 jobs/                     \# Background Jobs  
│   │   │   ├── emailQueue.js            \# Email queue  
│   │   │   ├── cleanupJob.js            \# Database cleanup  
│   │   │   └── index.js                 \# Jobs export  
│   │   │  
│   │   ├── 📁 sockets/                  \# WebSocket Handlers  
│   │   │   ├── chatSocket.js            \# Chat functionality  
│   │   │   ├── notificationSocket.js    \# Real-time notifications  
│   │   │   └── index.js                 \# Socket setup  
│   │   │  
│   │   ├── 📁 docs/                     \# API Documentation  
│   │   │   ├── swagger.js               \# Swagger configuration  
│   │   │   └── api.yaml                 \# API specifications  
│   │   │  
│   │   └── app.js                       \# Express app setup  
│   │  
│   ├── 📁 tests/                        \# Test Files  
│   │   ├── 📁 unit/                     \# Unit Tests  
│   │   │   ├── controllers/  
│   │   │   ├── services/  
│   │   │   └── utils/  
│   │   ├── 📁 integration/              \# Integration Tests  
│   │   │   ├── auth.test.js  
│   │   │   ├── user.test.js  
│   │   │   └── product.test.js  
│   │   ├── 📁 e2e/                      \# End-to-End Tests  
│   │   ├── 📁 fixtures/                 \# Test Data  
│   │   │   └── testData.js  
│   │   └── setup.js                     \# Test configuration  
│   │  
│   ├── 📁 uploads/                      \# Uploaded Files (temp)  
│   │   └── .gitkeep  
│   │  
│   ├── 📁 logs/                         \# Application Logs  
│   │   ├── error.log  
│   │   ├── combined.log  
│   │   └── .gitkeep  
│   │  
│   ├── 📁 scripts/                      \# Utility Scripts  
│   │   ├── seedDatabase.js              \# Database seeding  
│   │   ├── createAdmin.js               \# Create admin user  
│   │   └── cleanDatabase.js             \# Clean database  
│   │  
│   ├── .env                             \# Environment variables  
│   ├── .env.example                     \# Example env file  
│   ├── .env.development                 \# Development env  
│   ├── .env.production                  \# Production env  
│   ├── .env.test                        \# Testing env  
│   ├── .gitignore                       \# Git ignore rules  
│   ├── .eslintrc.js                     \# ESLint config  
│   ├── .prettierrc                      \# Prettier config  
│   ├── jest.config.js                   \# Jest configuration  
│   ├── nodemon.json                     \# Nodemon config  
│   ├── Dockerfile                       \# Docker configuration  
│   ├── docker-compose.yml               \# Docker compose  
│   ├── package.json                     \# Dependencies  
│   ├── package-lock.json                \# Lock file  
│   ├── server.js                        \# Entry point  
│   └── README.md                        \# Documentation  
│  
│  
├── 📁 frontend/                         \# Frontend Application  
│   │  
│   ├── 📁 public/                       \# Static Assets  
│   │   ├── favicon.ico                  \# Site favicon  
│   │   ├── logo192.png                  \# PWA icons  
│   │   ├── logo512.png  
│   │   ├── manifest.json                \# PWA manifest  
│   │   ├── robots.txt                   \# SEO robots  
│   │   └── index.html                   \# HTML template  
│   │  
│   ├── 📁 src/                          \# Source Code  
│   │   │  
│   │   ├── 📁 api/                      \# API Layer  
│   │   │   ├── axiosConfig.js           \# Axios instance  
│   │   │   ├── authApi.js               \# Auth API calls  
│   │   │   ├── userApi.js               \# User API calls  
│   │   │   ├── productApi.js            \# Product API calls  
│   │   │   ├── orderApi.js              \# Order API calls  
│   │   │   └── index.js                 \# API exports  
│   │   │  
│   │   ├── 📁 assets/                   \# Static Assets  
│   │   │   ├── 📁 images/               \# Image files  
│   │   │   │   ├── logo.png  
│   │   │   │   ├── hero-bg.jpg  
│   │   │   │   └── placeholder.png  
│   │   │   ├── 📁 icons/                \# Icon files  
│   │   │   │   └── sprite.svg  
│   │   │   ├── 📁 fonts/                \# Custom fonts  
│   │   │   │   └── custom-font.woff2  
│   │   │   └── 📁 styles/               \# Global styles  
│   │   │       ├── global.css  
│   │   │       ├── variables.css  
│   │   │       └── animations.css  
│   │   │  
│   │   ├── 📁 components/               \# Reusable Components  
│   │   │   │  
│   │   │   ├── 📁 common/               \# Common Components  
│   │   │   │   ├── 📁 Button/  
│   │   │   │   │   ├── Button.jsx  
│   │   │   │   │   ├── Button.module.css  
│   │   │   │   │   ├── Button.test.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Input/  
│   │   │   │   │   ├── Input.jsx  
│   │   │   │   │   ├── Input.module.css  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Modal/  
│   │   │   │   │   ├── Modal.jsx  
│   │   │   │   │   ├── Modal.module.css  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Card/  
│   │   │   │   ├── 📁 Loader/  
│   │   │   │   ├── 📁 Alert/  
│   │   │   │   ├── 📁 Avatar/  
│   │   │   │   ├── 📁 Badge/  
│   │   │   │   ├── 📁 Dropdown/  
│   │   │   │   ├── 📁 Pagination/  
│   │   │   │   ├── 📁 Table/  
│   │   │   │   ├── 📁 Tabs/  
│   │   │   │   ├── 📁 Tooltip/  
│   │   │   │   └── index.js             \# Common exports  
│   │   │   │  
│   │   │   ├── 📁 layout/               \# Layout Components  
│   │   │   │   ├── 📁 Header/  
│   │   │   │   │   ├── Header.jsx  
│   │   │   │   │   ├── Header.module.css  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Footer/  
│   │   │   │   │   ├── Footer.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Sidebar/  
│   │   │   │   │   ├── Sidebar.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 Navbar/  
│   │   │   │   ├── 📁 Breadcrumb/  
│   │   │   │   ├── MainLayout.jsx  
│   │   │   │   ├── AuthLayout.jsx  
│   │   │   │   ├── AdminLayout.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 forms/                \# Form Components  
│   │   │   │   ├── 📁 LoginForm/  
│   │   │   │   │   ├── LoginForm.jsx  
│   │   │   │   │   ├── LoginForm.module.css  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 RegisterForm/  
│   │   │   │   ├── 📁 ProductForm/  
│   │   │   │   ├── 📁 CheckoutForm/  
│   │   │   │   ├── 📁 ProfileForm/  
│   │   │   │   ├── 📁 SearchForm/  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 features/             \# Feature Components  
│   │   │   │   ├── 📁 auth/  
│   │   │   │   │   ├── LoginButton.jsx  
│   │   │   │   │   ├── LogoutButton.jsx  
│   │   │   │   │   ├── SocialLogin.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 products/  
│   │   │   │   │   ├── ProductCard.jsx  
│   │   │   │   │   ├── ProductList.jsx  
│   │   │   │   │   ├── ProductDetails.jsx  
│   │   │   │   │   ├── ProductFilter.jsx  
│   │   │   │   │   ├── ProductSearch.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 cart/  
│   │   │   │   │   ├── CartItem.jsx  
│   │   │   │   │   ├── CartList.jsx  
│   │   │   │   │   ├── CartSummary.jsx  
│   │   │   │   │   └── index.js  
│   │   │   │   ├── 📁 orders/  
│   │   │   │   ├── 📁 reviews/  
│   │   │   │   ├── 📁 user/  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   └── index.js                 \# All components export  
│   │   │  
│   │   ├── 📁 pages/                    \# Page Components  
│   │   │   ├── 📁 public/               \# Public Pages  
│   │   │   │   ├── HomePage.jsx  
│   │   │   │   ├── AboutPage.jsx  
│   │   │   │   ├── ContactPage.jsx  
│   │   │   │   ├── ProductsPage.jsx  
│   │   │   │   ├── ProductDetailPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 auth/                 \# Auth Pages  
│   │   │   │   ├── LoginPage.jsx  
│   │   │   │   ├── RegisterPage.jsx  
│   │   │   │   ├── ForgotPasswordPage.jsx  
│   │   │   │   ├── ResetPasswordPage.jsx  
│   │   │   │   ├── VerifyEmailPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 user/                 \# User Pages  
│   │   │   │   ├── ProfilePage.jsx  
│   │   │   │   ├── DashboardPage.jsx  
│   │   │   │   ├── OrdersPage.jsx  
│   │   │   │   ├── OrderDetailPage.jsx  
│   │   │   │   ├── WishlistPage.jsx  
│   │   │   │   ├── SettingsPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 admin/                \# Admin Pages  
│   │   │   │   ├── AdminDashboard.jsx  
│   │   │   │   ├── UsersManagement.jsx  
│   │   │   │   ├── ProductsManagement.jsx  
│   │   │   │   ├── OrdersManagement.jsx  
│   │   │   │   ├── AnalyticsPage.jsx  
│   │   │   │   ├── SettingsPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 checkout/             \# Checkout Pages  
│   │   │   │   ├── CartPage.jsx  
│   │   │   │   ├── CheckoutPage.jsx  
│   │   │   │   ├── PaymentPage.jsx  
│   │   │   │   ├── ConfirmationPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   ├── 📁 errors/               \# Error Pages  
│   │   │   │   ├── NotFoundPage.jsx  
│   │   │   │   ├── ServerErrorPage.jsx  
│   │   │   │   ├── UnauthorizedPage.jsx  
│   │   │   │   └── index.js  
│   │   │   │  
│   │   │   └── index.js                 \# Pages export  
│   │   │  
│   │   ├── 📁 hooks/                    \# Custom Hooks  
│   │   │   ├── useAuth.js               \# Authentication hook  
│   │   │   ├── useApi.js                \# API calls hook  
│   │   │   ├── useForm.js               \# Form handling  
│   │   │   ├── useLocalStorage.js       \# Local storage  
│   │   │   ├── useDebounce.js           \# Debounce hook  
│   │   │   ├── useTheme.js              \# Theme switching  
│   │   │   ├── usePagination.js         \# Pagination logic  
│   │   │   ├── useModal.js              \# Modal control  
│   │   │   ├── useOutsideClick.js       \# Click outside  
│   │   │   ├── useWindowSize.js         \# Window dimensions  
│   │   │   ├── useSocket.js             \# WebSocket hook  
│   │   │   ├── useCart.js               \# Cart operations  
│   │   │   └── index.js                 \# Hooks export  
│   │   │  
│   │   ├── 📁 context/                  \# React Context  
│   │   │   ├── AuthContext.jsx          \# Auth state  
│   │   │   ├── CartContext.jsx          \# Cart state  
│   │   │   ├── ThemeContext.jsx         \# Theme state  
│   │   │   ├── NotificationContext.jsx  \# Notifications  
│   │   │   ├── SocketContext.jsx        \# WebSocket  
│   │   │   └── index.js                 \# Context export  
│   │   │  
│   │   ├── 📁 redux/                    \# Redux Store (Alternative)  
│   │   │   ├── 📁 slices/               \# Redux Slices  
│   │   │   │   ├── authSlice.js  
│   │   │   │   ├── userSlice.js  
│   │   │   │   ├── productSlice.js  
│   │   │   │   ├── cartSlice.js  
│   │   │   │   ├── orderSlice.js  
│   │   │   │   └── uiSlice.js  
│   │   │   ├── 📁 actions/              \# Async Actions  
│   │   │   │   ├── authActions.js  
│   │   │   │   ├── productActions.js  
│   │   │   │   └── orderActions.js  
│   │   │   ├── 📁 selectors/            \# Memoized Selectors  
│   │   │   │   ├── authSelectors.js  
│   │   │   │   └── cartSelectors.js  
│   │   │   ├── store.js                 \# Store configuration  
│   │   │   └── index.js                 \# Redux exports  
│   │   │  
│   │   ├── 📁 routes/                   \# Route Configuration  
│   │   │   ├── AppRoutes.jsx            \# Main routes  
│   │   │   ├── PrivateRoute.jsx         \# Protected routes  
│   │   │   ├── AdminRoute.jsx           \# Admin routes  
│   │   │   ├── PublicRoute.jsx          \# Public only routes  
│   │   │   ├── routeConfig.js           \# Route definitions  
│   │   │   └── index.js                 \# Routes export  
│   │   │  
│   │   ├── 📁 services/                 \# Frontend Services  
│   │   │   ├── authService.js           \# Auth logic  
│   │   │   ├── storageService.js        \# Local storage  
│   │   │   ├── analyticsService.js      \# Analytics  
│   │   │   ├── notificationService.js   \# Browser notifications  
│   │   │   └── index.js                 \# Services export  
│   │   │  
│   │   ├── 📁 utils/                    \# Utility Functions  
│   │   │   ├── formatters.js            \# Data formatting  
│   │   │   ├── validators.js            \# Form validation  
│   │   │   ├── constants.js             \# App constants  
│   │   │   ├── helpers.js               \# Helper functions  
│   │   │   ├── dateUtils.js             \# Date manipulation  
│   │   │   ├── stringUtils.js           \# String helpers  
│   │   │   └── index.js                 \# Utils export  
│   │   │  
│   │   ├── 📁 config/                   \# App Configuration  
│   │   │   ├── app.config.js            \# App settings  
│   │   │   ├── api.config.js            \# API settings  
│   │   │   ├── theme.config.js          \# Theme settings  
│   │   │   └── index.js                 \# Config export  
│   │   │  
│   │   ├── 📁 constants/                \# Constants  
│   │   │   ├── actionTypes.js           \# Redux action types  
│   │   │   ├── apiEndpoints.js          \# API endpoints  
│   │   │   ├── routes.js                \# Route paths  
│   │   │   ├── messages.js              \# UI messages  
│   │   │   └── index.js                 \# Constants export  
│   │   │  
│   │   ├── 📁 types/                    \# TypeScript Types (if using TS)  
│   │   │   ├── auth.types.ts  
│   │   │   ├── user.types.ts  
│   │   │   ├── product.types.ts  
│   │   │   └── index.ts  
│   │   │  
│   │   ├── App.jsx                      \# Root component  
│   │   ├── App.css                      \# Root styles  
│   │   ├── index.jsx                    \# Entry point  
│   │   ├── index.css                    \# Global styles  
│   │   └── reportWebVitals.js           \# Performance  
│   │  
│   ├── 📁 tests/                        \# Test Files  
│   │   ├── 📁 \_\_mocks\_\_/                \# Mock files  
│   │   │   ├── fileMock.js  
│   │   │   └── styleMock.js  
│   │   ├── 📁 unit/                     \# Unit tests  
│   │   ├── 📁 integration/              \# Integration tests  
│   │   ├── 📁 e2e/                      \# E2E tests (Cypress)  
│   │   │   ├── 📁 fixtures/  
│   │   │   ├── 📁 support/  
│   │   │   └── 📁 integration/  
│   │   └── setupTests.js                \# Test setup  
│   │  
│   ├── .env                             \# Environment variables  
│   ├── .env.example                     \# Example env  
│   ├── .env.development                 \# Development env  
│   ├── .env.production                  \# Production env  
│   ├── .env.test                        \# Test env  
│   ├── .gitignore                       \# Git ignore  
│   ├── .eslintrc.js                     \# ESLint config  
│   ├── .prettierrc                      \# Prettier config  
│   ├── jsconfig.json                    \# JS config  
│   ├── tailwind.config.js               \# Tailwind config  
│   ├── postcss.config.js                \# PostCSS config  
│   ├── craco.config.js                  \# CRACO config  
│   ├── cypress.config.js                \# Cypress config  
│   ├── Dockerfile                       \# Docker config  
│   ├── nginx.conf                       \# Nginx config  
│   ├── package.json                     \# Dependencies  
│   ├── package-lock.json                \# Lock file  
│   └── README.md                        \# Documentation  
│  
│  
├── 📁 shared/                           \# Shared Code (Optional)  
│   ├── 📁 types/                        \# Shared types  
│   ├── 📁 constants/                    \# Shared constants  
│   ├── 📁 utils/                        \# Shared utilities  
│   └── 📁 validation/                   \# Shared validation  
│  
├── 📁 docs/                             \# Documentation  
│   ├── API.md                           \# API documentation  
│   ├── DEPLOYMENT.md                    \# Deployment guide  
│   ├── CONTRIBUTING.md                  \# Contribution guide  
│   └── ARCHITECTURE.md                  \# Architecture overview  
│  
├── 📁 scripts/                          \# Project Scripts  
│   ├── setup.sh                         \# Project setup  
│   ├── deploy.sh                        \# Deployment script  
│   └── test.sh                          \# Test runner  
│  
├── .github/                             \# GitHub Configuration  
│   ├── 📁 workflows/                    \# GitHub Actions  
│   │   ├── ci.yml                       \# CI pipeline  
│   │   ├── cd.yml                       \# CD pipeline  
│   │   └── test.yml                     \# Test pipeline  
│   ├── ISSUE\_TEMPLATE.md                \# Issue template  
│   └── PULL\_REQUEST\_TEMPLATE.md         \# PR template  
│  
├── docker-compose.yml                   \# Docker compose  
├── docker-compose.dev.yml               \# Dev compose  
├── docker-compose.prod.yml              \# Prod compose  
├── Makefile                             \# Make commands  
├── .gitignore                           \# Root gitignore  
├── .editorconfig                        \# Editor config  
├── package.json                         \# Root package (monorepo)  
├── lerna.json                           \# Lerna config (monorepo)  
└── README.md                            \# Project documentation

