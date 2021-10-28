<template>
  <div>
    <div
      class="
        flex
        h-screen
        bg-gray-100 bg-main-texture bg-center bg-no-repeat bg-cover
        -mt-24
        items-center
        justify-center
      "
    >
      <p class="mt-96 font-bold text-5xl text-center text-white">
        COMMITTED TO SOUTHWEST LOUISIANA. <br />COMMITTED TO HOME.
      </p>
    </div>
    <div
      class="
        flex flex-col
        bg-gray-200
        items-center
        justfy-center
        font-bold
        text-gray-800
      "
    >
      <p class="text-2xl mb-8 -mt-4">Real Case Results</p>
      <div class="flex max-w-screen-xl justify-around w-3/5">
        <div
          v-for="(data, index) in cardData"
          :key="index"
          class="flex flex-col items-left mb-24"
        >
          <p class="text-3xl">{{ data.price }}</p>
          <div class="bg-yellow-600 w-16 h-2 m-3 ml-6"></div>
          <p class="text-2xl">{{ data.title }}</p>
        </div>
      </div>
    </div>
    <div class="flex grid grid-cols-2 bg-white">
      <div>
        <img src="images/Image 3@1X.png" alt="" class="w-full" />
      </div>

      <div class="flex flex-col justify-around m-12">
        <p class="text-green-600 font-bold text-4xl mb-4">
          <span class="border-b-8 border-yellow-600">Why</span> Hire Us?
        </p>
        <p class="text-3xl font-semibold ml-12 w-4/5">
          Our team of skilled lawyers really is a team. We collaborate freely
          with one another to provide the best strategies for clients.
        </p>
        <p class="text-2xl ml-12 mt-4 w-4/5">
          Each of our Lake Charles attorneys today continues this sense of
          community and continuity. We apply our combined 135 years of
          experience to achieve great success for our clients. We invite you to
          look deeper into each attorney’s bios.
        </p>
      </div>
    </div>
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
