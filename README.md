# Fast React Pizza Co. 🍕

Fast React Pizza Co. is a modern single-page pizza ordering app built with React and a feature-first architecture.
It demonstrates production-style patterns including route data loading/actions, centralized Redux state, async flows, and clean reusable UI components.

## Live Versions

- Latest: https://fast-pizza-restaurant.vercel.app/
- Old (legacy): https://ahmed-adel-morsi.github.io/Fast-React-Pizza

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
- Vercel production deployment

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

- Vercel (current production)
- GitHub Pages (legacy hosted version)

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

This project is currently deployed on Vercel.

Latest deployment:

- https://fast-pizza-restaurant.vercel.app/

Legacy deployment:

- https://ahmed-adel-morsi.github.io/Fast-React-Pizza

To deploy updates, connect the repository to Vercel and deploy from the main branch (or run deployment through the Vercel dashboard/CLI workflow).

```bash
npm run build
```

Deployment notes:

- Vite config and router currently use /Fast-React-Pizza as base/basename, which is required for the legacy GitHub Pages path.
- For a root-domain Vercel-only setup, update/remove that base path in configuration.

## 📜 Available Scripts

- npm run dev: start Vite development server
- npm run build: build production assets
- npm run preview: preview built app locally
- npm run lint: run ESLint checks

## ⚠️ Current Limitations

- Cart state is in-memory (not persisted on full refresh)
- No authentication or payment processing
- Relies on third-party API availability
- Geolocation-based address fill depends on browser permission

## 🙌 Acknowledgment

Built as part of React learning and practice inspired by Jonas Schmedtmann's Fast React Pizza project, then extended and organized as a reusable portfolio-ready app.
