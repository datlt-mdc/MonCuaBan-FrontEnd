# Restaurant Management & Booking System

## 📋 README

### 1. 🎯 Overview

**Restaurant Management & Booking System** is a comprehensive restaurant management application with features:
- 🍴 Table booking & in-dining orders
- 💡 Personalized food recommendations based on dietary needs
- 💰 Payment via cash or PayOS
- 📊 Plan management, order tracking, revenue monitoring

**Main Technologies:**
- Backend: Spring Boot
- Frontend: React 19 + Vite
- UI: Tailwind CSS
- Charts: Recharts
- Maps: Leaflet

---

### 2. 🎨 Features

#### **A. For Customers**
- ✅ **Authentication**
  - Login / Register
  - Email verification
  - Google OAuth login
  - Forgot password & Reset
  
- ✅ **Table Booking**
  - Select date, time, number of guests
  - View booking history
  - Edit / Cancel booking

- ✅ **In-dining Orders**
  - View restaurant menu
  - Order directly at table
  - **Personalized food recommendations** based on:
    - BMR (Basal Metabolic Rate)
    - Dietary needs
    - Eating history

- ✅ **Payment & History**
  - Cash payment
  - PayOS payment
  - Payment history
  - Digital invoices

---

#### **B. For Staff**
- 📱 **Table Management**
  - View table layout & status
  - View guest information at each table
  
- 🍽️ **Service**
  - View list of orders to serve
  - Update service status
  - Service history

---

#### **C. For Managers**
- 📊 **Booking Management**
  - View, confirm, cancel bookings
  
- 🍴 **Dish Management**
  - Add / Edit / Delete dishes
  - Manage price, description, images
  
- 🔧 **Topping Management**
  - Add / Edit / Delete toppings
  - Set pricing
  
- 📅 **Daily Plan**
  - Plan dishes to sell for the day
  - Manage quantity & stock status
  
- 📈 **Statistics & Revenue**
  - View revenue by day/month
  - Sales & financial reports

---

#### **D. For Chef**
- 📋 **Order Management**
  - View orders to prepare
  - Update status: Not started → In progress → Completed
  - View order details (dishes, toppings, quantities)
  
- 📜 **History & Statistics**
  - Completed order history
  - Best-selling dish statistics

---

#### **E. For Admin**
- 🔐 **Account Management**
  - Create / Edit / Delete users
  - Assign roles (Admin, Manager, Chef, Staff, Customer)
  
- 💰 **Invoice Management**
  - View all invoices
  - Export reports
  
- 📊 **System Dashboard**
  - Revenue, booking, order statistics
  - User count by role

---

### 3. 🛠️ Tech Stack

| Technology | Version | Purpose |
|-----------|---------|---------|
| **React** | 19.1.1 | UI Framework |
| **Vite** | Latest | Build tool & Dev server |
| **React Router** | 7.9.2 | Routing & Navigation |
| **Tailwind CSS** | 4.1.13 | Styling (Utility-first) |
| **Axios** | 1.12.2 | HTTP Client |
| **Recharts** | 3.2.1 | Data Visualization & Charts |
| **Leaflet** | 1.9.4 | Interactive Maps |
| **date-fns** | 4.1.0 | Date Manipulation |
| **Lucide React** | 0.544.0 | Icon Library |

**Backend:** Spring Boot + RESTful API

---

### 4. 📁 Project Structure

```
src/
├── api/
│   └── apiConfig.js                    # API configuration
├── assets/                             # Images, fonts, media files
├── common/                             # Shared components
│   ├── ConfirmDialog.jsx
│   └── ToastHost.jsx
├── components/                         # Feature-specific components
│   ├── Admin/                         # Admin dashboard
│   │   ├── AccountManagement.jsx
│   │   ├── AdminDishStatistics.jsx
│   │   ├── Invoices.jsx
│   │   └── ...
│   ├── Chef/                          # Kitchen workspace
│   │   ├── ChefDailyDishes.jsx
│   │   ├── OrdersManagement.jsx
│   │   └── ...
│   ├── Handle/
│   │   └── ProtectedRoute.jsx         # Auth protection
│   ├── Home/                          # Customer pages
│   │   ├── BookingForm.jsx
│   │   ├── LoginForm.jsx
│   │   ├── MenuSection.jsx
│   │   ├── RegisterForm.jsx
│   │   └── ...
│   ├── Manager/                       # Manager dashboard
│   ├── Menu/                          # Menu components
│   ├── Staff/                         # Staff workspace
│   └── ui/                            # Generic UI components
├── constant/
│   └── routes.js                      # Route definitions
├── hooks/                             # Custom React Hooks
│   ├── useBMRCalculator.js
│   ├── useBooking.js
│   ├── useCartCalculator.js
│   ├── useMenuPersonalization.js
│   ├── useLogin.js
│   └── ...
├── layout/
│   └── MainLayout.jsx                 # Main layout wrapper
├── lib/                               # API calls & utilities
│   ├── apiBooking.js
│   ├── apiCustomer.js
│   ├── apiDish.js
│   ├── apiOrder.js
│   ├── apiPayment.js
│   ├── apiSuggestion.js
│   ├── apiStatistics.js
│   ├── auth.js
│   └── ...
├── pages/                             # Page components
│   ├── Admin.jsx
│   ├── Chef.jsx
│   ├── Home.jsx
│   ├── Login.jsx
│   ├── Manager.jsx
│   ├── Menu.jsx
│   ├── PaymentSuccess.jsx
│   └── ...
├── App.jsx                            # Root component
├── main.jsx                           # Entry point
└── index.css                          # Global styles
```

---

### 5. 📦 Installation Guide

#### **Prerequisites**

- **Node.js**: v18 or later
- **npm** or **yarn**: For package management
- **Git**: For cloning repository
- **Modern browser**: Chrome, Firefox, Safari, Edge

---

#### **Step 1: Clone Repository**

```bash
git clone <repository-url>
cd FrontEnd-BackUp
```

---

#### **Step 2: Install Dependencies**

```bash
npm install
```

Or if using yarn:

```bash
yarn install
```

---

#### **Step 3: Configure Environment (Optional)**

Create `.env.local` file (if needed) to configure environment variables:

```env
# Frontend origin
VITE_PUBLIC_ORIGIN=http://localhost:5173

# Backend API base URL (if different from localhost)
VITE_API_BASE_URL=http://localhost:8080
```

---

#### **Step 4: Run Development Server**

```bash
npm run dev
```

**Result:**
- Frontend runs at: `http://localhost:5173`
- Browser opens automatically
- Hot Module Replacement (HMR) enabled for auto-reload on code changes

---

#### **Step 5: Check Build**

```bash
npm run build
```

This command will:
- Compile React code
- Optimize assets
- Output to `dist/` folder
- Detect build errors if any

**Build output location:** `dist/`

---

#### **Step 6: Preview Production Build (Optional)**

```bash
npm run preview
```

This helps:
- Run production build locally for testing
- Check optimization before deployment

---

#### **Step 7: Linting & Code Quality Check (Optional)**

```bash
npm run lint
```

Check for code syntax errors or ESLint rule violations.

---

#### **Main Commands**

| Command | Purpose |
|---------|---------|
| `npm run dev` | Run development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Check code quality |

---

#### **Directory Structure After Installation**

```
FrontEnd-BackUp/
├── node_modules/          # Installed dependencies
├── public/                 # Static files
├── src/                    # Source code
├── dist/                   # Production build (after npm run build)
├── package.json            # Project configuration
├── package-lock.json       # Dependencies lock file
├── vite.config.js          # Vite configuration
├── eslint.config.js        # ESLint configuration
├── postcss.config.js       # PostCSS configuration
├── tailwind.config.js      # Tailwind CSS configuration (if exists)
└── README.md              # Project documentation
```

---

#### **Verify Successful Installation**

1. Run `npm run dev`
2. Open browser at `http://localhost:5173`
3. If you see login page → Installation successful ✅

---

#### **Troubleshooting**

| Issue | Solution |
|--------|----------|
| `npm install` fails | Delete `node_modules` and `package-lock.json`, run `npm install` again |
| Port 5173 already in use | Use different port: `npm run dev -- --port 3000` |
| Module not found | Run `npm install` again or check for typos in imports |
| Build error | Check `vite.config.js` and backend API URL |
| API calls fail | Verify backend server is running, check proxy URL in `vite.config.js` |

---

#### **Deploy to Production (Vercel)**

1. **Prepare Build:**
   ```bash
   npm run build
   ```

2. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Build for production"
   git push origin main
   ```

3. **Connect to Vercel:**
   - Visit https://vercel.com
   - Import project from GitHub
   - Vercel will auto-deploy on push
   - Deployed URL: `https://moncuaban.vercel.app`

---

## 📌 Summary

- ✅ Install dependencies: `npm install`
- ✅ Run dev server: `npm run dev`
- ✅ Build for production: `npm run build`
- ✅ Preview: `npm run preview`
- ✅ Lint code: `npm run lint`

