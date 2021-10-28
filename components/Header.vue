<template>
  <div class="flex items-center flex-col justify-center">
    <div
      class="
        container
        relative
        flex
        mt-4
        justify-between
        sm:items-center sm:pt-0
        max-w-screen-xl
      "
    >
      <div class="flex">
        <NuxtLink to="/" class="mr-3">
          <img src="images/location.png" loading="lazy" alt="" class="logo" />
        </NuxtLink>
        <p class="text-yellow-600 font-bold leading-4">
          723 Broad Street <br />
          Lake Charles, LA 70601
        </p>
      </div>
      <div class="text-yellow-600 font-bold">
        <Nuxt-link to="/testimonials" class="m-5">Testimonials</Nuxt-link>
        <Nuxt-link to="/videos" class="m-5">Videos</Nuxt-link>
        <Nuxt-link to="/scholarship" class="m-5">Scholarship</Nuxt-link>
      </div>
      <NuxtLink to="/" class="mr-3">
        <img src="images/search.png" loading="lazy" alt="" class="logo" />
      </NuxtLink>
    </div>
    <div
      class="
        container
        relative
        flex
        justify-between
        sm:items-start sm:pt-12
        max-w-screen-xl
      "
    >
      <NuxtLink to="/" class="mr-3">
        <img src="images/logo-desktop.png" loading="lazy" alt="" class="logo" />
      </NuxtLink>
      <div class="text-white font-bold">
        <Nuxt-link to="/home" class="m-5">Home</Nuxt-link>
        <Nuxt-link to="/our-firm" class="m-5">Our firm</Nuxt-link>
        <Nuxt-link to="/practice-areas" class="m-5">Practice Areas</Nuxt-link>
        <Nuxt-link to="/blog" class="m-5">Blog</Nuxt-link>
        <Nuxt-link to="/contact-us" class="m-5">Contact Us</Nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // data() {
  //   return {
  //     isOpen: false,
  //     burgerOpen: false,
  //   };
  // },
  // methods: {
  //   toggle() {
  //     this.isOpen = !this.isOpen;
  //     document.getElementById("myDropdown").classList.toggle("show");
  //     document.getElementById("myDropdown").classList.add("w--open");
  //   },
  //   burgerToggle() {
  //     this.burgerOpen = !this.burgerOpen;
  //     document.getElementById("myDropdown").classList.toggle("show");
  //     document.getElementById("myDropdown").classList.add("w--open");
  //   },
  // },
};
</script> 
