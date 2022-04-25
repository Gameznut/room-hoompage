<template>
  <div>
    <div class="carousel">
      <div class="carousel__item carousel__item--visible">
        <div class="desktop">
          <div class="imghero1">
            <img
              class="w-[100%] h-[100%]"
              src="../assets/images/mobile-image-hero-1.jpg"
              alt=""
            />
          </div>
          <div class="bg-[white] py-[5rem] px-[2rem]">
            <h1 class="text-black text-4xl">
              Discover innovative ways to decorate
            </h1>
            <p class="mt-[1rem] mb-[3.1rem]">
              We provide unmatched quality, comfort, and style for property
              owners across the country. Our experts combine form and function
              in bringing your vision to life. Create a room in your own style
              with our collection and make your property a reflection of you and
              what you love.
            </p>
            <small
              class="
                text-lg
                shopNow
                duration-500
                cursor-pointer
                text-black
                uppercase
                tracking-[0.5rem]
              "
              >Shop Now
              <span class="inline-block"
                ><svg width="40" height="12" xmlns="http://www.w3.org/2000/svg">
                  <path
                    d="M34.05 0l5.481 5.527h.008v.008L40 6l-.461.465v.063l-.062-.001L34.049 12l-.662-.668 4.765-4.805H0v-1h38.206l-4.82-4.86L34.05 0z"
                    fill="#000"
                  /></svg></span
            ></small>
          </div>
        </div>
      </div>
      <div class="carousel__item">
        <div class="grid">
          <div class="imghero1">
            <img
              class="w-[100%] h-[100%]"
              src="../assets/images/mobile-image-hero-2.jpg"
              alt=""
            />
          </div>
          <div class="bg-[white] py-[5rem] px-[2rem]">
            <h1 class="text-black text-4xl">
              Discover innovative ways to decorate
            </h1>
            <p class="mt-[1rem] mb-[3.1rem]">
              We provide unmatched quality, comfort, and style for property
              owners across the country. Our experts combine form and function
              in bringing your vision to life. Create a room in your own style
              with our collection and make your property a reflection of you and
              what you love.
            </p>
            <small
              class="
                text-lg
                shopNow
                duration-500
                cursor-pointer
                text-black
                uppercase
                tracking-[0.5rem]
              "
              >Shop Now
              <span class="inline-block"
                ><svg width="40" height="12" xmlns="http://www.w3.org/2000/svg">
                  <path
                    d="M34.05 0l5.481 5.527h.008v.008L40 6l-.461.465v.063l-.062-.001L34.049 12l-.662-.668 4.765-4.805H0v-1h38.206l-4.82-4.86L34.05 0z"
                    fill="#000"
                  /></svg></span
            ></small>
          </div>
        </div>
      </div>
      <div class="carousel__item">
        <div class="desktop">
          <div class="imghero1">
            <img
              class="w-[100%] h-[100%]"
              src="../assets/images/mobile-image-hero-3.jpg"
              alt=""
            />
          </div>
          <div class="bg-[white] py-[5rem] px-[2rem]">
            <h1 class="text-black text-4xl">
              Discover innovative ways to decorate
            </h1>
            <p class="mt-[1rem] mb-[3.1rem]">
              We provide unmatched quality, comfort, and style for property
              owners across the country. Our experts combine form and function
              in bringing your vision to life. Create a room in your own style
              with our collection and make your property a reflection of you and
              what you love.
            </p>
            <small
              class="
                text-lg
                shopNow
                duration-500
                cursor-pointer
                text-black
                uppercase
                tracking-[0.5rem]
              "
              >Shop Now
              <span class="inline-block"
                ><svg width="40" height="12" xmlns="http://www.w3.org/2000/svg">
                  <path
                    d="M34.05 0l5.481 5.527h.008v.008L40 6l-.461.465v.063l-.062-.001L34.049 12l-.662-.668 4.765-4.805H0v-1h38.206l-4.82-4.86L34.05 0z"
                    fill="#000"
                  /></svg></span
            ></small>
          </div>
        </div>
      </div>

      <div class="carousel__actions">
        <div
          id="carousel__button--prev"
          class="btn"
          aria-label="Previous slide"
        >
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M13 0L1 12l12 12"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </div>
        <div id="carousel__button--next" class="btn" aria-label="Next slide">
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M1 0l12 12L1 24"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
  <div>
    <div>
      <img src="../assets/images/image-about-dark.jpg" alt="" />
    </div>
    <div class="bg-white py-[4rem] px-[2rem]">
      <h1 class="text-[black] tracking-[0.3rem] font-bold uppercase">
        About our furniture
      </h1>
      <p class="mt-[1.3rem]">
        Our multifunctional collection blends design and function to suit your
        individual taste. Make each room unique, or pick a cohesive theme that
        best express your interests and what inspires you. Find the furniture
        pieces you need, from traditional to contemporary styles or anything in
        between. Product specialists are available to help you create your dream
        space.
      </p>
    </div>
    <div>
      <img src="../assets/images/image-about-light.jpg" alt="" />
    </div>
  </div>
</template>

<script setup >
import { onMounted, ref } from "@vue/runtime-core";

onMounted(() => {
  let slidePosition = 0;
  const slides = document.getElementsByClassName("carousel__item");
  const totalSlides = slides.length;

  document
    .getElementById("carousel__button--next")
    .addEventListener("click", function () {
      moveToNextSlide();
    });
  document
    .getElementById("carousel__button--prev")
    .addEventListener("click", function () {
      moveToPrevSlide();
    });

  const updateSlidePosition = () => {
    for (let slide of slides) {
      slide.classList.remove("carousel__item--visible");
      slide.classList.add("carousel__item--hidden");
    }

    slides[slidePosition].classList.add("carousel__item--visible");
  };

  const moveToNextSlide = () => {
    if (slidePosition === totalSlides - 1) {
      slidePosition = 0;
    } else {
      slidePosition++;
    }

    updateSlidePosition();
  };

  function moveToPrevSlide() {
    if (slidePosition === 0) {
      slidePosition = totalSlides - 1;
    } else {
      slidePosition--;
    }

    updateSlidePosition();
  }
});
</script>

<style scoped>
.imghero1 {
  max-width: 1000px;
  position: relative;
}

.btn {
  background-color: rgb(0, 0, 0);
  color: white;
  cursor: pointer;
  transition: 0.4s;
  padding: 1rem;
  font-size: 3rem;
}
.btn:hover {
  background-color: hsl(0, 0%, 27%);
}

.shopNow:hover,
.shopNow:hover path {
  color: gray;
  fill: gray;
}

.carousel {
  overflow: hidden;
  max-width: 425px;
  position: relative;
}

.carousel .carousel__item,
.carousel .carousel__item--hidden {
  display: none;
}

.carousel .carousel__item img {
  width: 100%;
  max-width: 600px;
  height: auto;
}

.carousel .carousel__item--visible {
  display: block;
  animation: fadeVisibility 0.5s;
}

.carousel .carousel__actions {
  display: flex;
  position: absolute;
  justify-content: center;
  align-items: center;
  right: 0;
  top: 37%;
}

/* .carousel .carousel__actions button {
  border-radius: 50px;
  border: 0;
  font-weight: bold;
  cursor: pointer;
  width: 40px;
  height: 40px;
} */

.carousel .carousel__actions button#carousel__button--prev {
  margin-left: 20px;
}

.carousel .carousel__actions button#carousel__button--next {
  margin-right: 20px;
}

@keyframes fadeVisibility {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
    transform: opacity linear;
  }
}

@media screen and (min-width: 1240px) {
  .desktop {
    display: grid;
    grid-template-columns:repeat(2, 1fr) ;
  }
  .carousel {
  overflow: hidden;
  max-width: 1920px;
  position: relative;
}
.carousel .carousel__item img {
  width: 100%;
  max-width: 100%;
  height: auto;
}

}
</style>