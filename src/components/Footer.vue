<script setup>
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-left">© {{ currentYear }} Portfolio ZIHONG. All rights reserved.</div>
      <div class="footer-center">
        <!-- <a href="/privacy">Privacy Policy</a>
        <a href="/terms">Terms & Conditions</a> -->
      </div>
      <div class="footer-right">Design By <a href="#" class="designer-link">ZIHONG</a></div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: var(--bg-color);
  padding: 1rem 0;
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
}

.footer-content {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.9rem;
  color: #888;
}

.footer-center {
  display: flex;
  gap: 2rem;
}

.footer-center a,
.designer-link {
  color: #888;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-center a:hover,
.designer-link:hover {
  color: var(--primary-color);
}

@media (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
    padding: 1rem;
  }

  .footer-center {
    gap: 1rem;
  }
}
</style>
