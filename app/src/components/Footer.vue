<template>
  <footer class="bg-gray-300 text-black">
    <div class="container px-6 py-16 mx-auto">
      <!-- Logo and Social Media Icons Section -->
      <div
        class="w-full max-w-screen-xl mx-auto flex flex-col items-center justify-between md:flex-row md:justify-between md:items-center mb-8"
      >
        <img src="https://img.freepik.com/premium-vector/drone-logo_629862-146.jpg" alt="DroneX Logo" class="h-16 mb-4 md:mb-0" />
        <ul class="flex space-x-6">
          <li>
            <a href="https://twitter.com" target="_blank" aria-label="Twitter">
              <!-- <img
                src=""
                class="w-6 h-6 hover:w-7 hover:h-7 transition hover:text-yellow-400"
                alt="Twitter"
              /> -->
            </a>
          </li>
          <li>
            <a
              href="https://whatsapp.com"
              target="_blank"
              aria-label="WhatsApp"
            >
              <!-- <img
                src=""
                class="w-6 h-6 hover:w-7 hover:h-7 transition hover:text-yellow-400"
                alt="WhatsApp"
              /> -->
            </a>
          </li>
          <li>
            <a
              href="https://instagram.com"
              target="_blank"
              aria-label="Instagram"
            >
              <!-- <img
                src=""
                class="w-6 h-6 hover:w-7 hover:h-7 transition hover:text-yellow-400"
                alt="Instagram"
              /> -->
            </a>
          </li>
          <li>
            <a
              href="https://www.facebook.com/profiainstitute/"
              target="_blank"
              aria-label="Facebook"
            >
              <!-- <img
                src=""
                class="w-6 h-6 hover:w-7 hover:h-7 transition hover:text-yellow-400"
                alt="Facebook"
              /> -->
            </a>
          </li>
        </ul>
      </div>

      <!-- Links Section -->
      <div
        class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 text-center md:text-left"
      >
        <!-- Company Section -->
        <div>
          <h3 class="text-lg font-semibold text-black mb-4">Company</h3>
          <ul class="space-y-2">
            <li>
              <router-link to="/about" class="hover:text-yellow-400"
                >About DroneX</router-link
              >
            </li>
            <li>
              <router-link to="/contact" class="hover:text-yellow-400"
                >Contact Us</router-link
              >
            </li>
            <li>
              <router-link to="/careers" class="hover:text-yellow-400"
                >Careers</router-link
              >
            </li>
            <li>
              <router-link to="/partners" class="hover:text-yellow-400"
                >Partnerships</router-link
              >
            </li>
          </ul>
        </div>

        <!-- Resources Section -->
        <div>
          <h3 class="text-lg font-semibold text-black mb-4">Resources</h3>
          <ul class="space-y-2">
            <li>
              <router-link to="/blog" class="hover:text-yellow-400"
                >Blog</router-link
              >
            </li>
            <li>
              <router-link to="/tutorials" class="hover:text-yellow-400"
                >Drone Tutorials</router-link
              >
            </li>
            <li>
              <router-link to="/guides" class="hover:text-yellow-400"
                >Buying Guides</router-link
              >
            </li>
            <li>
              <router-link to="/faq" class="hover:text-yellow-400"
                >FAQs</router-link
              >
            </li>
          </ul>
        </div>

        <!-- Support Section -->
        <div>
          <h3 class="text-lg font-semibold text-black mb-4">Support</h3>
          <ul class="space-y-2">
            <li>
              <router-link to="/support" class="hover:text-yellow-400"
                >Customer Support</router-link
              >
            </li>
            <li>
              <router-link to="/warranty" class="hover:text-yellow-400"
                >Warranty Information</router-link
              >
            </li>
            <li>
              <router-link to="/shipping" class="hover:text-yellow-400"
                >Shipping & Returns</router-link
              >
            </li>
            <li>
              <router-link to="/contact-support" class="hover:text-yellow-400"
                >Contact Support</router-link
              >
            </li>
          </ul>
        </div>
      </div>

      <!-- Copyright Section -->
      <div class="mt-10">
        <div class="text-center">
          <p class="text-sm text-black">
            © 2024 Blacknites. All Rights Reserved.
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
footer ul li a {
  transition: color 0.3s ease;
}

footer ul li a:hover {
  color: #f59e0b; /* Tailwind's yellow-400 */
}
</style>
