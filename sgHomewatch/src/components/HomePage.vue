<script setup lang="ts">
// HomePage.vue - Main landing page component
</script>

<template>
  <div>
    <!-- Hero Section -->
    <section id="home" class="hero">
      <div class="container">
        <div class="hero-content animate-fade-in">
          <img src="/logo.jpg" alt="S&G Homewatch Logo" class="hero-logo">
          <h1 class="hero-title">S&G Homewatch LLC</h1>
          <p class="hero-subtitle">We are here to keep an EYE on your Home while you are away!</p>
          <div class="cta-buttons">
            <button>Get Started</button>
            <button class="btn-secondary">Learn More</button>
          </div>
        </div>
      </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="section">
      <div class="container">
        <h2 class="text-center">Our Services</h2>
        <p class="text-center">We offer a range of services to keep your home safe and maintained while you're away.</p>
        
        <div class="grid grid-cols-1 grid-cols-md-2 grid-cols-lg-3">
          <!-- Service 1 -->
          <div class="service-card text-center">
            <i class="fas fa-home"></i>
            <h3>Homewatch</h3>
            <p>Regular checks on your home to ensure everything is secure and functioning properly.</p>
          </div>
          
          <!-- Service 2 -->
          <div class="service-card text-center">
            <i class="fas fa-user-tie"></i>
            <h3>Meet Vendors</h3>
            <p>We'll meet service providers and contractors at your home so you don't have to.</p>
          </div>
          
          <!-- Service 3 -->
          <div class="service-card text-center">
            <i class="fas fa-shopping-cart"></i>
            <h3>Grocery Shopping</h3>
            <p>We'll stock your fridge and pantry before you return home.</p>
          </div>
          
          <!-- Service 4 -->
          <div class="service-card text-center">
            <i class="fas fa-plane"></i>
            <h3>Airport Pickup/Dropoff</h3>
            <p>Transportation services to and from the airport for your convenience.</p>
          </div>
          
          <!-- Service 5 -->
          <div class="service-card text-center">
            <i class="fas fa-envelope"></i>
            <h3>Check Mail</h3>
            <p>We'll collect and secure your mail while you're away.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="section" style="background-color: var(--light-bg);">
      <div class="container">
        <h2 class="text-center">About Us</h2>
        <div class="grid grid-cols-1 grid-cols-md-2">
          <div class="about-image">
            <!-- Placeholder for about image -->
            <div class="about-image-placeholder" style="background-color: var(--primary-color); height: 300px; border-radius: 8px;"></div>
          </div>
          <div class="about-content">
            <h3>Blair and Maria Stocking</h3>
            <p class="subtitle">Owner/Operators</p>
            <p>
              At S&G Homewatch, we understand the importance of having peace of mind when you're away from your home.
              Our dedicated team provides professional homewatch services to ensure your property remains safe and well-maintained
              during your absence.
            </p>
            <p>
              With years of experience and a commitment to excellence, we treat each home with the utmost care and attention,
              just as we would our own. Whether you're a seasonal resident or frequently away on business,
              you can trust S&G Homewatch to keep an eye on your valuable investment.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section">
      <div class="container">
        <h2 class="text-center">Contact Us</h2>
        <p class="text-center">Reach out to us for more information about our services or to schedule a consultation.</p>
        
        <div class="grid grid-cols-1 grid-cols-md-2">
          <div class="contact-info">
            <h3>Get In Touch</h3>
            <div class="contact-item">
              <i class="fas fa-phone"></i>
              <span>239-692-3106</span>
            </div>
            <div class="contact-item">
              <i class="fas fa-envelope"></i>
              <span>info@sghomewatch.com</span>
            </div>
            <div class="contact-item">
              <i class="fas fa-map-marker-alt"></i>
              <span>Serving Southwest Florida</span>
            </div>
          </div>
          
          <div class="contact-form">
            <form>
              <div class="form-group">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" placeholder="Your Name">
              </div>
              <div class="form-group">
                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="Your Email">
              </div>
              <div class="form-group">
                <label for="message">Message</label>
                <textarea id="message" name="message" rows="4" placeholder="Your Message"></textarea>
              </div>
              <button type="submit">Send Message</button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style scoped>
.hero-logo {
  width: 120px;
  height: 120px;
  border-radius: 8px;
  margin: 0 auto 1.5rem;
  object-fit: cover;
}

.cta-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 2rem;
}

.about-image-placeholder {
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 1.5rem;
}

.subtitle {
  color: var(--gray);
  margin-bottom: 1rem;
}

/* Form styles */
.form-group {
  margin-bottom: 1.5rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 600;
}

input,
textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid var(--light-gray);
  border-radius: 4px;
  font-family: 'Open Sans', sans-serif;
}

input:focus,
textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 2px rgba(215, 95, 78, 0.2);
}

@media (max-width: 768px) {
  .cta-buttons {
    flex-direction: column;
  }
  
  .cta-buttons button {
    width: 100%;
  }
}
</style>
