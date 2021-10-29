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
      <p class="text-3xl my-4">Meet the attorneys</p>
      <p class="text-2xl text-center pb-28">
        Brothers James and Will Cox founded what is today the law firm of Cox,
        Cox, Filo, Camel & Wilson L.L.C. <br />
        in 1969, with a passionate sense of civic duty and a desire to champion
        client rights.
      </p>
    </div>
    <div class="-mt-20">
      <VueSlickCarousel
        ref="carousel"
        class="flex items-center justify-center max-w-screen-xl mb-2"
        :slidesToShow="4"
        :slidesToScroll="4"
      >
        <div v-for="(data, index) in cardData" :key="index">
          <div class="flex flex-col items-center">
            <img :src="data.image" loading="lazy" alt="" class="w-4/5" />
            <div
              :id="data.id"
              class="
                flex flex-col
                items-center
                font-semibold
                border-4
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
      </VueSlickCarousel>
      <div class="flex items-center justify-center mb-20 mt-5">
        <div class="text-2xl cursor-pointer" @click="showBefore">
          <img src="images/left-arrow.png" alt="" />
        </div>
        <p class="mx-4">{{ cardIndex + 1 }} / 4</p>
        <div class="cursor-pointer" @click="showNext">
          <img src="images/right-arrow.png" alt="" />
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
          name: "Michael Cox1",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 2,
          name: "PAUL COX1",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 3,
          name: "Kevin Camel1",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 4,
          name: "Tom Filo2",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 5,
          name: "Michael Cox2",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 6,
          name: "PAUL COX2",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 7,
          name: "Kevin Camel2",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 8,
          name: "Tom Filo3",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 9,
          name: "Michael Cox3",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 10,
          name: "PAUL COX3",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 11,
          name: "Kevin Camel3",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 12,
          name: "Tom Filo4",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 13,
          name: "Michael Cox4",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 14,
          name: "PAUL COX4",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
        {
          id: 15,
          name: "Kevin Camel4",
          image: "images/Image 7@1X.png",
          role: "Partner",
        },
      ],
      currentCardID: 0,
      cardIndex: 0,
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
      this.$refs.carousel.next();
      this.cardIndex === 3
        ? (this.cardIndex = 0)
        : (this.cardIndex = this.cardIndex + 1);
    },
    showBefore() {
      this.$refs.carousel.prev();
      this.cardIndex === 0
        ? (this.cardIndex = 3)
        : (this.cardIndex = this.cardIndex - 1);
    },
  },
};
</script> 