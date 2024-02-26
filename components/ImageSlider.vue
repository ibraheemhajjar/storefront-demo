<template>
  <Carousel v-bind="settings" class="carousel">
    <Slide
      v-for="(image, index) in images"
      :key="index"
      @click="selectImage(index)"
      class="slide"
    >
      <NuxtImg
        :class="{ selected: index === currentImage }"
        :src="image"
        class="carousel-item"
      />
    </Slide>

    <template #addons>
      <Navigation class="slide-nav" />
    </template>
  </Carousel>
</template>

<script setup>
import { Carousel, Navigation, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

const props = defineProps({
  images: {
    type: Array,
  },
});

const emit = defineEmits(["select"]);

let currentImage = ref(0);

const settings = {
  itemsToShow: 4,
  snapAlign: "center",
};

function selectImage(index) {
  currentImage.value = index;
  emit("select", index);
}
</script>

<style>
.carousel {
  width: 55%;
}
.carousel__slide {
  justify-content: space-around;
}
.carousel-item {
  width: 4rem;
}
.slide-nav {
  background-color: black;
  border-radius: 50%;
  color: white;
}
.slide-nav:hover {
  color: white;
}
.selected {
  border: 3px solid red;
}

@media (max-width: 1200px) {
  .carousel {
    width: 65%;
  }
}

@media (max-width: 850px) {
  .carousel {
    width: 75%;
  }
}
@media (max-width: 700px) {
  .carousel {
    width: 100%;
  }
}

@media (max-width: 500px) {
  .carousel-item {
    width: 3rem;
  }
}
</style>
