<script setup></script>

<template>
  <footer class="app-footer">
    <div class="container footer-content">
      <div class="footer-section">
        <h3>About Besa</h3>
        <p>
          Your premium e-commerce destination for everything you need. Quality products, fast
          delivery.
        </p>
      </div>
      <div class="footer-section">
        <h3>Quick Links</h3>
        <ul>
          <li><a href="#">About Us</a></li>
          <li><a href="#">Terms & Conditions</a></li>
          <li><a href="#">Privacy Policy</a></li>
          <li><a href="#">Help Center</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h3>Contact</h3>
        <p>1234 Street Name, City, Country</p>
        <p>+1 123 456 7890</p>
        <p>support@besa.com</p>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container copyright">&copy; 2026 Besa. All rights reserved.</div>
    </div>
  </footer>
</template>

<style scoped>
.app-footer {
  background-color: var(--secondary-color);
  color: #cccccc;
  margin-top: 50px;
  padding-top: 60px;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 40px;
  padding-bottom: 60px;
}

.footer-section h3 {
  color: var(--white);
  margin-bottom: 20px;
  font-size: 18px;
}

.footer-section ul li {
  margin-bottom: 10px;
}

.footer-section a {
  color: #cccccc;
}

.footer-section a:hover {
  color: var(--primary-color);
}

.footer-bottom {
  border-top: 1px solid #333;
  padding: 20px 0;
  text-align: center;
  font-size: 14px;
}
</style>
