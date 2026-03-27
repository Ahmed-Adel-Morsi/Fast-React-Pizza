# Fast React Pizza

A modern single-page pizza ordering app built with React, Redux Toolkit, React Router, and Tailwind CSS.

The app lets users:

- Browse a live pizza menu
- Add and update cart items
- Place an order with optional priority delivery
- Auto-fill address using browser geolocation
- Search and track existing orders by ID

## Tech Stack

- React 18
- React Router (data loaders and actions)
- Redux Toolkit + React Redux
- Tailwind CSS
- Vite

## Features

- Feature-based architecture (cart, menu, order, user)
- Centralized state management with Redux slices
- Async data loading with route loaders and thunks
- Responsive UI with reusable component primitives
- External API integration for menu/order data and reverse geocoding

## Project Structure

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

## Getting Started

### Prerequisites

- Node.js 16+ (recommended: latest LTS)
- npm

### Installation

```bash
npm install
```

### Run in Development

```bash
npm run dev
```

### Build for Production

```bash
npm run build
```

### Preview Production Build

```bash
npm run preview
```

## Deployment

This project is configured for GitHub Pages deployment.

```bash
npm run deploy
```

Note:

- Vite base path is set for a GitHub Pages subpath deployment.

## Main User Flow

1. Enter user name on home screen
2. Browse menu and add pizzas to cart
3. Open cart and adjust quantities
4. Submit order form (with optional geolocation-based address)
5. Get order ID and track order status
6. Optionally upgrade order to priority

## External APIs

- Pizza API (menu and orders): https://react-fast-pizza-api.jonas.io/api
- Reverse geocoding API: https://api.bigdatacloud.net

## Known Limitations

- Cart state is not persisted across full page refresh
- No authentication or payment integration
- Depends on availability of third-party APIs
- Geolocation auto-fill requires browser permission

## Scripts

- `npm run dev` - Start development server
- `npm run build` - Build production bundle
- `npm run preview` - Preview built app locally
- `npm run lint` - Run ESLint
- `npm run deploy` - Deploy to GitHub Pages

## Credits

This project was done while reviewing React through Jonas Schmedtmann's course material.  
It is a learning-focused implementation inspired by the Fast React Pizza project from the course.
