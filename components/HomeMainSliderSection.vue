<template>
  <div class="flex flex-col items-center">
    <div
      class="
        flex flex-col
        items-center
        justify-center
        bg-indigo-900
        text-white
        font-semibold
        w-full
      "
    >
      <div class="bg-yellow-600 w-2 h-12"></div>
      <p class="text-3xl m-4">Meet the attorneys</p>
      <p class="text-2xl text-center mb-20">
        Brothers James and Will Cox founded what is today the law firm of Cox,
        Cox, Filo, Camel & Wilson L.L.C. <br />
        in 1969, with a passionate sense of civic duty and a desire to champion
        client rights.
      </p>
    </div>
    <div class="w-4/5 z-10">
      <div class="container flex flex-col items-center justify-center">
        <div class="flex items-center justify-center max-w-screen-xl mb-2">
          <div
            class="flex flex-col items-center w-80"
            v-for="(data, index) in cardData"
            :key="index"
          >
            <img :src="data.image" loading="lazy" alt="" class="w-4/5 -mt-16" />
            <div
              :id="data.id"
              class="
                flex flex-col
                items-center
                font-semibold
                border-4
                m-3
                py-2
                border-yellow-600
                w-4/5
                leading-4
                cursor-pointer
              "
              @click="changeCard(data.id)"
            >
              <p>{{ data.name }}</p>
              <p>{{ data.role }}</p>
            </div>
          </div>
        </div>
        <div class="flex items-center justify-center mb-20">
          <div class="text-2xl cursor-pointer" @click="showBefore">
            <img src="images/left-arrow.png" alt="" />
          </div>
          <p class="mx-4">{{ currentCardID + 1 }} / {{ cardData.length }}</p>
          <div class="cursor-pointer" @click="showNext">
            <img src="images/right-arrow.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  name: "Carousel",
  components: { VueSlickCarousel },
  data() {
    return {
      cardData: [
        {
          id: 0,
          name: "Tom Filo",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 1,
          name: "Michael Cox",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 2,
          name: "PAUL COX",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 3,
          name: "Kevin Camel",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
      ],
      currentCardID: 0,
    };
  },
  mounted() {
    this.$nextTick(function () {
      this.chooseCard(0);
    });
  },
  methods: {
    chooseCard(id) {
      for (let i = 0; i < this.cardData.length; i++) {
        if (id === i) {
          document.getElementById(i).classList.add("bg-blue-900");
          document.getElementById(i).classList.add("text-white");
        } else {
          document.getElementById(i).classList.remove("bg-blue-900");
          document.getElementById(i).classList.remove("text-white");
        }
      }
    },
    changeCard(id) {
      this.currentCardID = id;
      this.chooseCard(id);
    },
    showNext() {
      this.currentCardID === this.cardData.length - 1
        ? (this.currentCardID = 0)
        : (this.currentCardID = this.currentCardID + 1);
      this.chooseCard(this.currentCardID);
    },
    showBefore() {
      this.currentCardID === 0
        ? (this.currentCardID = this.cardData.length - 1)
        : (this.currentCardID = this.currentCardID - 1);
      this.chooseCard(this.currentCardID);
    },
  },
};
</script> 

export default {
  
};