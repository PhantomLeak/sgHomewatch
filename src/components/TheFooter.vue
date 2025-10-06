<script setup lang="ts">
// TheFooter.vue - Site footer component
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="grid grid-cols-1 grid-cols-md-2 grid-cols-lg-3">
                <div>
                    <h3>S&G Homewatch LLC</h3>
                    <p>We are here to keep an EYE on your Home while you are away!</p>
                    <div class="social-icons">
                        <a href="#"><i class="fa-brands fa-facebook"></i></a>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                        <a href="#"><i class="fa-brands fa-linkedin"></i></a>
                    </div>
                </div>

                <div>
                    <h3>Contact</h3>
                    <div class="contact-info">
                        <div class="contact-item">
                            <i class="fas fa-phone"></i>
                            <a href="tel:239-692-3106">239-692-3106</a>
                        </div>
                        <div class="contact-item">
                            <i class="fas fa-envelope"></i>
                            <a href="mailto:southallscheduling@gmail.com">southallscheduling@gmail.com</a>
                        </div>
                    </div>
                </div>

                <div>
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#about">About</a></li>
                        <li><a href="#contact">Contact</a></li>
                        <li><a href="https://www.southallconstructionremodeling.com/" target="_blank">Construction
                                Needs</a> </li>
                    </ul>
                </div>
            </div>

            <div class="text-center copyright">
                <p>&copy; {{ new Date().getFullYear() }} S&G Homewatch LLC. All Rights Reserved.</p>
            </div>
        </div>
    </footer>
</template>

<style scoped>
.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-bottom: 0.75rem;
}

.copyright {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  margin-top: 2rem;
  padding-top: 1.5rem;
}
</style>
