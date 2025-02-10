<script setup>
const contactInfo = {
  email: "pangzihong2@gmail.com",
  phone: "+601123009600",
  whatsapp: "+601123009600", // WhatsApp number with country code
  linkedin: "https://www.linkedin.com/in/pang-zi-hong-5577761b7/",
};
</script>

<template>
  <section class="contact-section" id="contact">
    <div class="section-header">
      <h2>Contact</h2>
      <p>Let's get in touch</p>
    </div>

    <div class="contact-container">
      <div class="contact-row">
        <a :href="`mailto:${contactInfo.email}`" class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-envelope"></i>
          </div>
          <div class="contact-info">
            <h3>Email</h3>
            <p>{{ contactInfo.email }}</p>
          </div>
        </a>

        <a :href="`tel:${contactInfo.phone}`" class="contact-item">
          <div class="contact-icon">
            <i class="fas fa-phone"></i>
          </div>
          <div class="contact-info">
            <h3>Phone</h3>
            <p>{{ contactInfo.phone }}</p>
          </div>
        </a>

        <a :href="`https://wa.me/${contactInfo.whatsapp}`" target="_blank" class="contact-item">
          <div class="contact-icon">
            <i class="fab fa-whatsapp"></i>
          </div>
          <div class="contact-info">
            <h3>WhatsApp</h3>
            <p>Message me on WhatsApp</p>
          </div>
        </a>

        <a :href="contactInfo.linkedin" target="_blank" class="contact-item">
          <div class="contact-icon">
            <i class="fab fa-linkedin"></i>
          </div>
          <div class="contact-info">
            <h3>LinkedIn</h3>
            <p>Connect with me</p>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  padding: 5rem 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-header h2 {
  font-size: 2.5rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.section-header p {
  color: #888;
  font-size: 1.1rem;
}

.contact-container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}

.contact-row {
  display: flex;
  justify-content: center;
  gap: 2rem;
}

.contact-item {
  flex: 1;
  background: rgba(255, 255, 255, 0.05);
  padding: 2rem;
  border-radius: 15px;
  text-decoration: none;
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.contact-item:hover {
  transform: translateY(-5px);
  background: rgba(255, 255, 255, 0.1);
}

.contact-icon {
  width: 50px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--primary-color);
  color: var(--bg-color);
  font-size: 1.5rem;
  margin-bottom: 1.5rem;
}

.contact-info h3 {
  color: #fff;
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
}

.contact-info p {
  color: #888;
  font-size: 0.9rem;
  word-break: break-word;
}

/* Tablet Responsive */
@media (max-width: 1024px) {
  .contact-row {
    flex-wrap: wrap;
    gap: 1.5rem;
  }

  .contact-item {
    flex: 1 1 calc(50% - 0.75rem);
  }

  .section-header {
    margin-bottom: 3rem;
  }

  .section-header h2 {
    font-size: 2.2rem;
  }
}

/* Mobile Responsive */
@media (max-width: 640px) {
  .contact-section {
    padding: 3rem 0;
  }

  .contact-container {
    padding: 0 1rem;
  }

  .contact-row {
    flex-direction: column;
    gap: 1rem;
  }

  .contact-item {
    flex: 1 1 100%;
    padding: 1.5rem;
  }

  .section-header {
    margin-bottom: 2rem;
  }

  .section-header h2 {
    font-size: 2rem;
  }

  .section-header p {
    font-size: 1rem;
  }

  .contact-icon {
    width: 40px;
    height: 40px;
    font-size: 1.2rem;
    margin-bottom: 1rem;
  }

  .contact-info h3 {
    font-size: 1.1rem;
  }

  .contact-info p {
    font-size: 0.85rem;
  }
}

/* Small Mobile Responsive */
@media (max-width: 380px) {
  .contact-section {
    padding: 2rem 0;
  }

  .contact-item {
    padding: 1rem;
  }

  .section-header h2 {
    font-size: 1.8rem;
  }

  .contact-icon {
    width: 35px;
    height: 35px;
    font-size: 1rem;
  }
}
</style>
