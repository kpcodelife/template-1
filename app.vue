<template>
  <div ref="scrollContainer" class="relative scroll-container h-screen" :style="`background-color: ${currentBackgroundColor}` ">
      <swiper
        class="h-screen"
        :direction="'vertical'"
        :slidesPerView="1"
        :modules="[Mousewheel]"
        :mousewheel="mousewheelOptions"
        :speed="500"
        @slideChange="onSlideChange"
        @swiper="onSwiper"
      >
        <swiper-slide class="h-screen">
          <ShowCaseItem id="a1" class="showCaseItem" imageSrc="andrey-k-iQeNACvNFVc-unsplash.jpg" heading="Item #1" :description="item1Description" fontColor="" linkColor=""/>
        </swiper-slide>
        <swiper-slide class="h-screen">
          <ShowCaseItem id="a2" class="showCaseItem" imageSrc="greg-rosenke-ej5GSCjHXRs-unsplash.jpg" heading="Item #2" :description="item2Description" fontColor="" linkColor=""/>
        </swiper-slide>
        <swiper-slide class="h-screen">
          <ShowCaseItem id="a3" class="showCaseItem" imageSrc="marcus-lenk-CH_KY7MK0Jc-unsplash.jpg" heading="Item #3" :description="item2Description" fontColor="" linkColor=""/>
        </swiper-slide>
        <swiper-slide class="h-screen">
          <ShowCaseItem id="a4" class="showCaseItem" imageSrc="pawel-czerwinski-A_ywJp2bN3w-unsplash.jpg" heading="Item #4" :description="item2Description" fontColor="" linkColor=""/>
        </swiper-slide>
        <swiper-slide class="h-screen">
          <ShowCaseItem id="a5" class="showCaseItem" imageSrc="s-tsuchiya-aXqpGHceDu4-unsplash.jpg" heading="Item #5" :description="item2Description" fontColor="" linkColor=""/>
        </swiper-slide>
      </swiper>

      <PageHeading class="fixed top-[20px] left-[20px]" pageHeading="Showcase" />
      <PageNav class="fixed hidden md:block bottom-[20px] right-[40px]" @navigateTo="switchSlides" />
      <PageDescription class="relative text-center md:text-left md:fixed md:bottom-[100px] md:left-[20px] px-4 md:px-0 mb-12 md:mb-0" :pageDescription="pageDescription" />
      <PagePrivacyPolicy class="relative text-center md:text-left md:fixed md:bottom-[20px] md:left-[20px] px-4 md:px-0 mb-12 md:mb-0" :pagePrivacyText="privacyPolicyText" :pagePrivacyLink="privacyPolicyLink" />
      <PageContact class="relative text-center md:text-left md:fixed md:top-[20px] md:right-[40px] mb-12 md:mb-0" :pageContact="pageContact" />
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { register } from 'swiper/element/bundle';
import { Mousewheel } from 'swiper/modules';
register();

const swiperInstance = ref()

function onSwiper(swiper) {
  swiperInstance.value = swiper
}


const item1Description = "This is a brief description about item number 1."
const item2Description = "This is a brief description about item number 2."
const pageDescription = "This is a brief description about item number 2. This is a brief description about item number 2. This is a brief description about item number 2. This is a brief description about item number 2."
const pageContact = "email@thisiscool.com"
const privacyPolicyText = "Privacy Policy"
const privacyPolicyLink = "www.google.com"

const mousewheelOptions = {
  forceToAxis: true, // Allow only vertical scrolling
  sensitivity: 5,   // Adjust sensitivity as needed
};

// List of background colors corresponding to each slide
const slideBackgroundColors = [
  '#00c1b5',
  '#ff651a',
  '#ffbe00',
  '#1d3fbb',
  '#e30512',
];

// Current slide index
let currentSlideIndex = 0;

// Method to update the current slide index when a slide change occurs
const onSlideChange = (e) => {
  currentSlideIndex = e.activeIndex;
  currentBackgroundColor.value = slideBackgroundColors[currentSlideIndex]; // Update currentBackgroundColor
};

// Computed property to get the background color based on the current slide index
const currentBackgroundColor = ref(slideBackgroundColors[currentSlideIndex]);

const switchSlides = index => {
  console.log(swiperInstance)
  swiperInstance.value.slideTo(index)
}
</script>

<style lang="scss">
.scroll-container {
  transition: background-color 0.5s ease;
}
.swiper-wrapper {
    transition-timing-function: linear;
 }
</style>