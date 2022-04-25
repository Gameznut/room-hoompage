<template>
  <div>
    <div class="imghero1">
      <img
        class="w-[100%] h-[100%]"
        src="../assets/images/mobile-image-hero-1.jpg"
        alt=""
      />
      <div class="btns">
        <div class="btn">
          <svg width="14" height="24" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M13 0L1 12l12 12"
              stroke="#FFF"
              fill="none"
              fill-rule="evenodd"
            />
          </svg>
        </div>
        <div class="btn">
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
    <div class="bg-[white] py-[5rem] px-[2rem]">
      <h1 class="text-black text-4xl">Discover innovative ways to decorate</h1>
      <p class="mt-[1rem] mb-[3.1rem]">
        We provide unmatched quality, comfort, and style for property owners
        across the country. Our experts combine form and function in bringing
        your vision to life. Create a room in your own style with our collection
        and make your property a reflection of you and what you love.
      </p>
      <small
        class="
          text-lg
          shopNow duration-500
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
  <div>
      <div>
          <img src="../assets/images/image-about-dark.jpg" alt="">
      </div>
      <div class="bg-white py-[4rem] px-[2rem]">
          <h1 class="text-[black] tracking-[0.3rem] font-bold uppercase"> About our furniture</h1>
          <p class="mt-[1.3rem]">Our multifunctional collection blends design and function to suit your individual taste. Make each room unique, or pick a cohesive theme that best express your interests and what inspires you. Find the furniture pieces you need, from traditional to contemporary styles or anything in between. Product specialists are available to help you create your dream space.</p>
      </div>
            <div>
          <img src="../assets/images/image-about-light.jpg" alt="">
      </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.imghero1 {
  max-width: 1000px;
  position: relative;
}
.btns {
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  bottom: 0;
  right: 0;
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
</style>