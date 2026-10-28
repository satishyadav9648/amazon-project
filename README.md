# 🛒 Amazon Clone - JavaScript Course Project

A fully responsive, interactive e-commerce web application inspired by Amazon. Built from scratch with **Vanilla HTML5, CSS3, and Modern JavaScript (ES6+ Modules)** as part of hands-on JavaScript course learning.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Key Features](#-key-features)
- [Tech Stack](#-tech-stack)
- [Project Architecture](#-project-architecture)
- [Core JavaScript Concepts Covered](#-core-javascript-concepts-covered)
- [Getting Started](#-getting-started)
- [How to Run Locally](#-how-to-run-locally)
- [Project Roadmap & Milestones](#-project-roadmap--milestones)
- [Author](#-author)
- [Acknowledgments](#-acknowledgments)

---

## 🌟 Overview

The **JavaScript Amazon Project** is a comprehensive hands-on project designed to bridge the gap between basic JavaScript fundamentals and real-world frontend web development.

It transforms static e-commerce HTML pages into a dynamic, data-driven web application with modular JavaScript, state management, interactive shopping cart logic, and modular code organization.

---

## 🚀 Key Features

- **🛍️ Dynamic Product Catalog**: Renders products dynamically from structured data objects (`data/products.js`) with ratings, prices in cents (converted accurately to dollars), images, and keywords.
- **🛒 Interactive Shopping Cart**:
  - Add items to cart with unique product IDs via `data-*` dataset attributes.
  - Cart quantity recalculation and live badge update in the navigation header.
  - Multi-item matching logic (increments quantity if already in cart).
- **📦 Multi-Page Layout**:
  - `amazon.html`: Main store catalog and search header.
  - `checkout.html`: Order review, delivery options, and payment summary.
  - `orders.html`: Placed orders and order history.
  - `tracking.html`: Package delivery tracking progress bar.
- **🧩 ES6 Modules Architecture**: Strict separation of concerns using JavaScript Modules (`import` / `export`) to keep data, business logic, and UI code clean and maintainable.
- **📱 Responsive Design**: Fully responsive styling adapted for desktop, tablet, and mobile viewport sizes.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Semantic structure for product grids, cart, checkout, and tracking pages |
| **CSS3 (Vanilla)** | Custom styling, CSS Grid, Flexbox, media queries, and responsive layouts |
| **JavaScript (ES6+)** | Dynamic DOM manipulation, Event Handling, Array methods, and ES Modules |
| **Google Fonts (Roboto)** | Clean, modern e-commerce typography |
| **Git & GitHub** | Version control, atomic commit history, and code hosting |

---

## 📂 Project Architecture

```plaintext
javascript-amazon-project/
│
├── amazon.html                 # Main store product catalog page
├── checkout.html               # Cart review and checkout page
├── orders.html                 # Orders history page
├── tracking.html               # Package delivery tracking page
│
├── data/                       # Data layer & state models
│   ├── cart.js                 # Cart state and mutation functions (addToCart)
│   └── products.js             # Product catalog dataset
│
├── scripts/                    # Application logic (Controller / UI)
│   └── amazon.js               # Main page rendering and event listeners
│
├── backend/                    # Backend data representations
│   └── products.json           # Raw JSON product data
│
├── styles/                     # CSS stylesheets organized by scope
│   ├── shared/                 # Shared header and general styles
│   │   ├── general.css
│   │   └── amazon-header.css
│   └── pages/                  # Page-specific styling
│       ├── amazon.css
│       ├── orders.css
│       ├── tracking.css
│       └── checkout/
│           ├── checkout.css
│           └── checkout-header.css
│
├── images/                     # Icons, logos, ratings, and product images
└── README.md                   # Project documentation
```

---

## 🧠 Core JavaScript Concepts Covered

Through this project, key production-grade JavaScript concepts are practiced:

1. **DOM Generation & Manipulation**:
   - Building dynamic HTML strings using ES6 Template Literals.
   - Inserting dynamic HTML using `element.innerHTML`.
2. **Event-Driven Programming**:
   - Attaching event listeners to dynamically rendered buttons using `document.querySelectorAll()` and `.forEach()`.
   - Accessing custom HTML data using `button.dataset.productId`.
3. **Data Representation & Normalization**:
   - Storing prices as integers (`priceCents`) to avoid floating-point inaccuracies in currency calculations.
   - Formatting prices using `(priceCents / 100).toFixed(2)`.
4. **State Management**:
   - Centralizing the cart state in `data/cart.js`.
   - Keeping the cart state in sync with DOM elements.
5. **Modern ES6 Modules**:
   - Splitting code across files using `export` and `import`.
   - Utilizing `<script type="module">` for clean modular dependencies without polluting the global scope.

---

## 💻 Getting Started

### Prerequisites

Make sure you have:
- A modern web browser (Google Chrome, Firefox, Safari, or Microsoft Edge).
- A code editor such as **VS Code**.
- (Recommended) The **Live Server** extension for VS Code or any local HTTP static server (required because ES6 Modules have CORS restrictions when opened directly via `file://`).

---

## 🏃 How to Run Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/satishyadav9648/amazon-project.git
   ```

2. **Navigate into the project directory**:
   ```bash
   cd "javascript-amazon-project"
   ```

3. **Start a local development server**:
   - **Option A (VS Code Live Server)**:
     - Open the folder in VS Code.
     - Right-click `amazon.html` and select **"Open with Live Server"**.
   - **Option B (Python)**:
     ```bash
     # Python 3
     python3 -m http.server 8000
     ```
     Then open `http://localhost:8000/amazon.html` in your browser.
   - **Option C (Node.js `npx serve`)**:
     ```bash
     npx serve .
     ```

---

## 🗺️ Project Roadmap & Milestones

- [x] **Milestone 1**: Set up project structure and multi-page HTML/CSS layouts.
- [x] **Milestone 2**: Generate product catalog dynamically using JavaScript.
- [x] **Milestone 3**: Implement interactive "Add to Cart" button and cart quantity counter.
- [x] **Milestone 4**: Refactor code into ES6 Modules (`data/cart.js`, `data/products.js`, `scripts/amazon.js`).
- [ ] **Milestone 5**: Handle quantity selector dropdowns & "Added" checkmark notifications.
- [ ] **Milestone 6**: Build dynamic Checkout page (`order-summary` and `payment-summary`).
- [ ] **Milestone 7**: Add item removal, update quantity, and delivery options calculation.
- [ ] **Milestone 8**: Implement persistent cart storage using `localStorage`.
- [ ] **Milestone 9**: Object-Oriented Programming (OOP) and Classes refactoring.
- [ ] **Milestone 10**: Unit testing with Jasmine / automated testing.
- [ ] **Milestone 11**: Backend API integration using `fetch()` and `async/await`.

---

## 👤 Author

**Satish Yadav**
- GitHub: [@satishyadav9648](https://github.com/satishyadav9648)
- Repository: [amazon-project](https://github.com/satishyadav9648/amazon-project)

---

## 💡 Acknowledgments

- Built as part of the hands-on curriculum from the JavaScript Course by [SuperSimpleDev](https://www.youtube.com/c/SuperSimpleDev).
- Amazon brand assets and icons are used strictly for educational and portfolio demonstration purposes.
