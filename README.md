# Fast React Pizza Co. 🍕

Fast React Pizza Co. is a modern single-page pizza ordering app built with React and a feature-first architecture.
It demonstrates production-style patterns including route data loading/actions, centralized Redux state, async flows, and clean reusable UI components.

## ✨ Overview

This project allows users to:

- Browse a live pizza menu from a remote API
- Add pizzas to a cart and adjust quantities in real time
- Create orders with form validation and optional priority delivery
- Auto-fill address using browser geolocation + reverse geocoding
- Track existing orders by ID and update an order to priority

## 🚀 Features

- Feature-based folder structure: cart, menu, order, user
- Redux Toolkit slices for user and cart state management
- React Router data APIs:
	- loader for menu and order fetching
	- action for order creation and order priority update
- Fetcher-based background menu loading on order details page
- Responsive Tailwind UI with reusable building blocks
- Dedicated loading, error, empty-state, and search flows
- GitHub Pages deployment support out of the box

## 🧱 Tech Stack

### Core

- React 18
- React DOM 18
- React Router DOM 6 (loaders, actions, useFetcher)
- Redux Toolkit
- React Redux

### Styling

- Tailwind CSS
- PostCSS
- Autoprefixer

### Tooling

- Vite
- ESLint (+ React, React Hooks, React Refresh plugins)
- Prettier (+ Tailwind plugin)

### Deployment

- GitHub Pages via gh-pages

## 🗂️ Project Structure

```text
src/
	features/
		cart/
		menu/
		order/
		user/
	services/
	ui/
	utils/
	App.jsx
	main.jsx
	store.js
```

## 🔄 Main App Flow

1. User enters a name on the home page.
2. User opens the menu and adds pizzas to cart.
3. User reviews cart, updates quantities, or clears cart.
4. User submits a new order (phone validation included).
5. User can request automatic address fill using geolocation.
6. App creates order and redirects to order details by order ID.
7. User can search any order by ID and optionally mark it as priority.

## 🌐 External APIs

- Pizza API (menu + orders)
	- https://react-fast-pizza-api.jonas.io/api
- Reverse Geocoding API
	- https://api.bigdatacloud.net/data/reverse-geocode-client

## ⚙️ Getting Started

### Prerequisites

- Node.js 16+ (LTS recommended)
- npm

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

### Production Build

```bash
npm run build
```

### Preview Build

```bash
npm run preview
```

### Lint

```bash
npm run lint
```

## 📦 Deployment

This project is preconfigured for GitHub Pages deployment.

```bash
npm run deploy
```

Deployment notes:

- Vite base path is set to /Fast-React-Pizza.
- Router basename is also set to /Fast-React-Pizza.

## 📜 Available Scripts

- npm run dev: start Vite development server
- npm run build: build production assets
- npm run preview: preview built app locally
- npm run lint: run ESLint checks
- npm run predeploy: run production build before deployment
- npm run deploy: publish dist to GitHub Pages

## ⚠️ Current Limitations

- Cart state is in-memory (not persisted on full refresh)
- No authentication or payment processing
- Relies on third-party API availability
- Geolocation-based address fill depends on browser permission

## 🙌 Acknowledgment

Built as part of React learning and practice inspired by Jonas Schmedtmann's Fast React Pizza project, then extended and organized as a reusable portfolio-ready app.
