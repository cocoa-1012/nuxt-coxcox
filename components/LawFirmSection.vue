<template>
  <div>
    <section class="flex flex-col relative items-center justify-center">
      <div class="flex flex-row items-center justify-around w-4/5 mb-28 z-10">
        <div v-for="(data, index) in linkData" :key="index">
          <NuxtLink :to="data.url" class="mr-3 w-32">
            <img :src="data.image" loading="lazy" alt="" class="w-32" />
          </NuxtLink>
        </div>
      </div>

      <p
        class="
          absolute
          bottom-0
          left-32
          text-8xl text-gray-100
          font-semibold
          z-0
        "
      >
        MORE THAN A <br />PERSONAL INJURY <br />LAW FIRM
      </p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
      burgerOpen: false,
      cardData: [
        {
          price: "$262 M.",
          title: "Class Judgment",
        },
        {
          price: "$36 M.",
          title: "Train Accident",
        },
        {
          price: "$17.5 M.",
          title: "Class Settlement",
        },
        {
          price: "$10.8 M.",
          title: "Truck Accident",
        },
      ],
      linkData: [
        {
          id: 0,
          image: "images/Image 12@1X.png",
          url: "#",
        },
        {
          id: 1,
          image: "images/Image 14@1X.png",
          url: "#",
        },
        {
          id: 2,
          image: "images/Image 16@1X.png",
          url: "#",
        },
        {
          id: 3,
          image: "images/Image 15@1X.png",
          url: "#",
        },
      ],
    };
  },
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
