## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Available Scripts](#-available-scripts)
- [Components Overview](#-components-overview)
- [State Management](#-state-management)
- [Styling](#-styling)
- [Browser Support](#-browser-support)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

## 🛠 Tech Stack

- **Frontend Framework:** React 18+
- **Routing:** React Router DOM
- **Styling:** Tailwind CSS
- **Icons:** Lucide React & Heroicons
- **Font:** Inter (Google Fonts)
- **Build Tool:** Vite
- **Package Manager:** npm/yarn

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Node.js** (version 16.0 or higher)
  - Download from [nodejs.org](https://nodejs.org/)
  - Verify installation: `node --version`
- **npm** (comes with Node.js) or **yarn**
  - Verify npm: `npm --version`
  - Or install yarn: `npm install -g yarn`
- **Git** (for version control)
  - Download from [git-scm.com](https://git-scm.com/)
- **Code Editor** (recommended: VS Code)
  - Download from [code.visualstudio.com](https://code.visualstudio.com/)

## 🚀 Installation

Follow these step-by-step instructions to set up the project locally:

### Step 1: Clone the Repository

Clone the repository
git clone https://github.com/yourusername/styleloom.git

Navigate to the project directory
cd styleloom

text

### Step 2: Install Dependencies

Using npm
npm install

OR using yarn
yarn install

text

### Step 3: Install Required Packages

Make sure you have all the necessary dependencies:

Core dependencies
npm install react react-dom react-router-dom

UI and Icons
npm install lucide-react @heroicons/react

Styling
npm install tailwindcss postcss autoprefixer

Development dependencies
npm install --save-dev vite @vitejs/plugin-react

text

### Step 4: Configure Tailwind CSS

Create `tailwind.config.js`:

/** @type {import('tailwindcss').Config} /
export default {
content: [
"./index.html",
"./src/**/.{js,ts,jsx,tsx}",
],
theme: {
extend: {
fontFamily: {
'inter': ['Inter', 'sans-serif'],
},
colors: {
slate: {
850: '#1e293b',
950: '#0f172a',
}
}
},
},
plugins: [],
}

text

### Step 5: Update CSS File

Add this to your `src/index.css`:

@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');

body {
font-family: 'Inter', sans-serif;
margin: 0;
padding: 0;
box-sizing: border-box;
}

.line-clamp-2 {
display: -webkit-box;
-webkit-line-clamp: 2;
-webkit-box-orient: vertical;
overflow: hidden;
}

text

### Step 6: Configure Vite

Create `vite.config.js`:

import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
plugins: [react()],
server: {
port: 3000,
open: true
}
})

text

### Step 7: Start the Development Server

Using npm
npm run dev

OR using yarn
yarn dev

text

### Step 8: Open in Browser

Open your browser and navigate to:
http://localhost:3000

text

## 📁 Project Structure

styleloom/
├── public/
│ ├── index.html
│ └── favicon.ico
├── src/
│ ├── Pages/
│ │ ├── Home.jsx
│ │ ├── Products/
│ │ │ └── Products.jsx
│ │ ├── ProductDetail.jsx
│ │ ├── Cart/
│ │ │ └── Cart.jsx
│ │ ├── Wishlist.jsx
│ │ └── CheckoutForm.jsx
│ ├── App.jsx
│ ├── main.jsx
│ └── index.css
├── package.json
├── vite.config.js
├── tailwind.config.js
└── README.md

text

## 📜 Available Scripts

- **`npm run dev`** - Starts the development server
- **`npm run build`** - Builds the app for production
- **`npm run preview`** - Preview the production build locally
- **`npm run lint`** - Run ESLint for code quality

## 🧩 Components Overview

### 1. App.jsx (Main Application)
- **Purpose:** Root component with routing and global state management
- **Features:** 
  - React Router setup
  - Global cart and wishlist state
  - Session storage persistence
  - Product data management

### 2. Home.jsx
- **Purpose:** Landing page component
- **Features:**
  - Hero section
  - Featured products
  - Category navigation

### 3. Products.jsx
- **Purpose:** Product catalog and category pages
- **Features:**
  - Product grid/carousel display
  - Category filtering
  - Price sorting
  - Search functionality
  - Wishlist integration

### 4. ProductDetail.jsx
- **Purpose:** Individual product page
- **Features:**
  - Product image gallery
  - Detailed product information
  - Add to cart/wishlist
  - Related products section
  - Size and quantity selection

### 5. Cart.jsx
- **Purpose:** Shopping cart management
- **Features:**
  - Cart items display
  - Quantity updates
  - Remove items
  - Price calculations
  - Responsive design (mobile, tablet, desktop)

### 6. Wishlist.jsx
- **Purpose:** Wishlist management
- **Features:**
  - Saved products display
  - Move to cart functionality
  - Remove from wishlist

### 7. CheckoutForm.jsx
- **Purpose:** Checkout process
- **Features:**
  - Shipping information form
  - Order summary
  - Payment method display
  - Form validation

## 🗃 State Management

The application uses React's built-in state management with:

### Global State (App.jsx)
// Cart state
const [cartItems, setCartItems] = useState([]);

// Wishlist state
const [wishlistItems, setWishlistItems] = useState([]);

// Product navigation state
const [productState, setProductState] = useState({
currentPage: 'home',
selectedCategory: null,
sortBy: 'popularity',
priceRange: 'all'
});

text

### Persistence
- **Session Storage:** Cart and wishlist data persist across browser sessions
- **State Recovery:** Application state is restored on page refresh

## 🎨 Styling

### Design System
- **Color Palette:** Dark theme with slate gradients
- **Typography:** Inter font family
- **Components:** Modern cards, buttons, and form elements
- **Responsive:** Mobile-first approach

### Key Classes
/* Background gradients */
bg-gradient-to-br from-[#1e293b] via-[#334155] to-[#475569]

/* Card styling */
bg-gradient-to-r from-[#0f172a] to-[#1e293b]

/* Button gradients */
bg-gradient-to-r from-blue-500 to-purple-600

text

## 🌐 Browser Support

- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📱 Responsive Breakpoints

- **Mobile:** < 768px
- **Tablet:** 768px - 1024px  
- **Desktop:** > 1024px
- **Large Desktop:** > 1280px

## 🚀 Deployment

### Deploy to Netlify

1. **Build the project:**
npm run build

text

2. **Upload dist folder to Netlify:**
- Go to [netlify.com](https://netlify.com)
- Drag and drop the `dist` folder
- Your site will be live!

### Deploy to Vercel

1. **Install Vercel CLI:**
npm install -g vercel

text

2. **Deploy:**
vercel

text

### Deploy to GitHub Pages

1. **Install gh-pages:**
npm install --save-dev gh-pages

text

2. **Add to package.json:**
{
"homepage": "https://yourusername.github.io/styleloom",
"scripts": {
"predeploy": "npm run build",
"deploy": "gh-pages -d dist"
}
}

text

3. **Deploy:**
npm run deploy

text

## 🔧 Development Tips

### VS Code Extensions (Recommended)
- **ES7+ React/Redux Snippets** - Code snippets
- **Tailwind CSS IntelliSense** - Tailwind autocomplete
- **Auto Rename Tag** - HTML tag renaming
- **Prettier** - Code formatting
- **GitLens** - Git integration

### Code Formatting
Add `.prettierrc` file:
{
"semi": true,
"trailingComma": "es5",
"singleQuote": true,
"printWidth": 80,
"tabWidth": 2
}

text

## 🐛 Troubleshooting

### Common Issues

1. **Port already in use:**
Kill the process
npx kill-port 3000

Or use different port
npm run dev -- --port 3001

text

2. **Module not found errors:**
Clear node_modules and reinstall
rm -rf node_modules package-lock.json
npm install

text

3. **Build errors:**
Check for ESLint errors
npm run lint

Fix automatically
npm run lint -- --fix

text

4. **Tailwind styles not working:**
- Ensure `tailwind.config.js` content paths are correct
- Check if `@import` statements are in `index.css`

## 📈 Performance Optimization

- **Lazy Loading:** Images and components load on demand
- **Code Splitting:** React Router handles route-based splitting
- **Session Storage:** Efficient state persistence
- **Optimized Images:** WebP format with fallbacks

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **React Team** - For the amazing framework
- **Tailwind CSS** - For the utility-first CSS framework
- **Lucide** - For the beautiful icons
- **Unsplash** - For the placeholder images

## 📞 Support

If you have any questions or need help, please:

1. Check the issues tab on GitHub
2. Create a new issue with detailed description
3. Join our community discussions

## 🚨 Quick Start for Absolute Beginners

If you're completely new to programming, follow these simplified steps:

### 1. Install Node.js
- Go to [nodejs.org](https://nodejs.org/)
- Download the LTS version
- Run the installer
- Restart your computer

### 2. Install VS Code
- Go to [code.visualstudio.com](https://code.visualstudio.com/)
- Download and install

### 3. Open Terminal/Command Prompt
- **Windows:** Press `Win + R`, type `cmd`, press Enter
- **Mac:** Press `Cmd + Space`, type `terminal`, press Enter
- **Linux:** Press `Ctrl + Alt + T`

### 4. Navigate to Desktop
cd Desktop

text

### 5. Clone This Project
git clone https://github.com/yourusername/styleloom.git
cd styleloom

text

### 6. Install Dependencies
npm install

text

### 7. Start the Project
npm run dev

text

### 8. Open in Browser
Your browser should automatically open `http://localhost:3000`

**Congratulations! 🎉 You now have StyleLoom running locally!**

## 📸 Screenshots

### Home Page
![Home Page](https://via.placeholder.com/800x600/1e293b/ffffff?text=Home+Page)

### Products Page
![Products Page](https://via.placeholder.com/800x600/1e293b/ffffff?text=Products+Page)

### Shopping Cart
![Shopping Cart](https://via.placeholder.com/800x600/1e293b/ffffff?text=Shopping+Cart)

### Checkout
![Checkout](https://via.placeholder.com/800x600/1e293b/ffffff?text=Checkout+Page)
