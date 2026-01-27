<script setup></script>

<template>
  <header class="app-header">
    <!-- 1. Top Bar -->
    <div class="header-top">
      <div class="container top-content">
        <div class="top-left">
          <span class="hotline-text">Shopping Hotline:</span>
          <span class="hotline-number"><strong>(+228) 93 41 52 11</strong></span>
        </div>
        <div class="top-right">
          <ul>
            <li><a href="#">Guide & Support</a></li>
            <li><a href="#">English ▾</a></li>
            <li><a href="#">Recent Viewed ▾</a></li>
            <li><a href="#">Order Tracking</a></li>
            <li><a href="#">Login Or Register</a></li>
          </ul>
        </div>
      </div>
    </div>

    <!-- 2. Main Header (Logo, Search, Cart) -->
    <div class="header-main">
      <div class="container main-content">
        <!-- Logo -->
        <router-link to="/" class="logo">
          <div class="logo-icon">✔</div>
          <!-- Placeholder for the tick icon -->
          <span class="logo-text">Besa</span>
        </router-link>

        <!-- Search Bar -->
        <div class="search-bar">
          <div class="search-category-wrapper">
            <select class="search-category">
              <option>All</option>
            </select>
            <span class="arrow">▾</span>
          </div>
          <div class="search-divider"></div>
          <input type="text" placeholder="Search for products..." />
          <button class="search-btn">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="20"
              height="20"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <circle cx="11" cy="11" r="8"></circle>
              <line x1="21" y1="21" x2="16.65" y2="16.65"></line>
            </svg>
          </button>
        </div>

        <!-- Icons -->
        <div class="header-icons">
          <div class="icon-group">
            <span class="icon">
              <!-- Heart SVG -->
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path
                  d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"
                ></path>
              </svg>
            </span>
            <span class="badge">0</span>
          </div>
          <div class="icon-group cart-group">
            <span class="icon">
              <!-- Cart SVG (keeping unicode for now or replacing if requested, but user specifically asked for heart) -->
              🛒
            </span>
            <span class="badge">0</span>
            <div class="cart-info">
              <span class="cart-label">Shopping Cart</span>
              <span class="cart-price">$0.00</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- 3. Navigation Bar -->
    <div class="header-nav-bar">
      <div class="container nav-content">
        <div class="all-departments">
          <span>☰</span>
          <span class="dept-text">All Departments</span>
        </div>
        <nav class="main-nav">
          <ul>
            <li>
              <router-link to="/">
                <span>Home</span>
                <span class="dropdown-icon">▾</span>
              </router-link>
            </li>
            <li>
              <router-link to="/shop">
                <span>Shop</span>
                <span class="dropdown-icon">▾</span>
              </router-link>
            </li>
            <li>
              <a href="#">
                <span>Pages</span>
                <span class="dropdown-icon">▾</span>
              </a>
            </li>
            <li>
              <a href="#">
                <span>Electronics Devices</span>
                <span class="dropdown-icon">▾</span>
              </a>
            </li>
            <li>
              <a href="#">
                <span>Blog</span>
                <span class="dropdown-icon">▾</span>
              </a>
            </li>
            <li><a href="#">Become A Vendor</a></li>
            <li><a href="#">Flash Deals</a></li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<style scoped>
/* General Reset for Header */
.app-header {
  background-color: var(--white);
  font-size: 14px;
}

/* 1. Top Bar */
.header-top {
  border-bottom: 1px solid var(--border-color);
  color: var(--text-light);
  font-size: 13px;
  padding: 10px 0;
}

.top-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap; /* Allow wrapping on small screens */
  gap: 10px;
}

.top-left {
  display: flex;
  align-items: center;
  flex-wrap: wrap; /* Allow number to wrap */
  gap: 5px;
}

.hotline-number {
  color: var(--primary-color);
}

.top-right ul {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 0; /* Gap handled by padding/border */
}

.top-right li {
  display: flex;
  align-items: center;
  padding: 0 10px;
  border-right: 1px solid #e5e5e5;
}

.top-right li:last-child {
  border-right: none;
  padding-right: 0;
}

.top-right li:first-child {
  padding-left: 0;
}

.top-right a {
  white-space: nowrap; /* Prevent individual text wrapping */
}

.top-right a:hover {
  color: var(--primary-color);
}

/* 2. Main Header */
.header-main {
  padding: 25px 0;
}

.main-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 30px;
}

.logo {
  display: flex;
  align-items: center;
  gap: 10px;
  text-decoration: none;
  font-size: 28px;
  font-weight: 800;
  color: var(--secondary-color);
}

.logo-icon {
  background-color: var(--primary-color);
  color: white;
  width: 35px;
  height: 35px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 5px;
  font-size: 18px;
}

/* Search Bar */
.search-bar {
  flex: 1;
  max-width: 600px;
  display: flex;
  border: 2px solid var(--primary-color);
  border-radius: 4px;
  overflow: hidden;
  height: 45px;
  align-items: center;
}

.search-category-wrapper {
  position: relative;
  display: flex;
  align-items: center;
  padding: 0 15px;
  background-color: #fff;
  cursor: pointer;
}

.search-category {
  appearance: none;
  border: none;
  background: transparent;
  color: var(--text-color);
  outline: none;
  font-weight: 500;
  padding-right: 5px;
  cursor: pointer;
}

.search-category-wrapper .arrow {
  font-size: 10px;
  color: var(--text-light);
  margin-left: 5px;
}

.search-divider {
  width: 1px;
  height: 20px;
  background-color: #ddd;
}

.search-bar input {
  flex: 1;
  border: none;
  padding: 0 15px;
  outline: none;
  color: var(--text-light);
}

.search-btn {
  background-color: var(--primary-color);
  color: white;
  border: none;
  width: 50px;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: background-color 0.3s;
}

.search-btn:hover {
  opacity: 0.9;
}

/* Icons Group */
.header-icons {
  display: flex;
  gap: 25px;
  align-items: center;
}

.icon-group {
  position: relative;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 20px; /* Increased from 15px */
}

.icon {
  font-size: 24px;
  color: #999999;
  display: flex; /* Center SVG */
  align-items: center;
}

.badge {
  position: absolute;
  top: -5px;
  left: 15px;
  background-color: var(--yellow-color);
  color: var(--secondary-color);
  font-size: 11px;
  height: 18px;
  min-width: 18px;
  padding: 0 5px;
  border-radius: 9px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: bold;
}

.cart-info {
  display: flex;
  flex-direction: column;
  line-height: 1.2;
}

.cart-label {
  font-size: 12px;
  color: var(--text-light);
}

.cart-price {
  font-weight: bold;
  color: var(--primary-color);
}

/* 3. Navigation Bar */
.header-nav-bar {
  background-color: var(--primary-color);
  color: white;
}

.nav-content {
  display: flex;
  height: 50px; /* Fixed height for easier vertical centering */
}

/* All Departments */
.all-departments {
  background-color: var(--secondary-color);
  width: 260px; /* Slightly wider */
  padding: 0 25px;
  font-weight: 700;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 15px; /* Increased gap */
}

.dept-text {
  white-space: nowrap;
}

/* Main Nav */
.main-nav {
  flex: 1;
  display: flex;
  align-items: center;
  padding-left: 30px;
  overflow: hidden; /* For truncation container */
}

.main-nav ul {
  display: flex;
  gap: 30px;
  align-items: center; /* Ensure vertical centering */
  width: 100%;
}

.main-nav li {
  /* Allow shrinking */
  min-width: 0;
  flex-shrink: 1;
}

.main-nav a {
  color: white;
  font-weight: 500;
  font-size: 14px;
  text-transform: capitalize;
  display: flex;
  align-items: center;
  gap: 5px; /* Gap between text and icon */
  white-space: nowrap; /* Keep icon with text */
}

.main-nav a span:first-child {
  overflow: hidden;
  text-overflow: ellipsis;
}

.dropdown-icon {
  font-size: 10px;
  margin-top: 1px;
}

.main-nav a:hover {
  opacity: 0.9;
}
</style>
