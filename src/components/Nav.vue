<template>
  <nav class="z-[44] fixed pt-[5.7rem] px-[5.4rem]">
    <div class="flex gap-[4.7rem] items-center mobile">
      <div class="open">
        <svg width="20" height="14" xmlns="http://www.w3.org/2000/svg">
          <path
            d="M20 12v2H0v-2h20zm0-6v2H0V6h20zm0-6v2H0V0h20z"
            fill="#FFF"
            fill-rule="evenodd"
          />
        </svg>
      </div>
      <div class="w-full max-w-[5rem] mobileImg">
        <img class="w-full" src="../assets/images/logo.svg" alt="" />
      </div>
      <div class="flex gap-[3rem] mobileNav">
        <div @click="close" class="close">
          <svg width="16" height="16" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M14.364.222l1.414 1.414L9.414 8l6.364 6.364-1.414 1.414L8 9.414l-6.364 6.364-1.414-1.414L6.586 8 .222 1.636 1.636.222 8 6.586 14.364.222z"
              fill="#000"
              fill-rule="evenodd"
              opacity=".201"
            />
          </svg>
        </div>
        <a href="#">home</a>
        <a href="#">shop</a>
        <a href="#">about</a>
        <a href="#">contact</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { onMounted } from "vue";

onMounted(() => {
  const menu = document.querySelector(".mobileNav");
  const closeBtn = document.querySelector(".close");
  closeBtn.addEventListener("click", () => {
    menu.classList.remove("showNav");
  });
  const openBtn = document.querySelector(".open");
  openBtn.addEventListener("click", () => {
    menu.classList.add("showNav");
  });
});
</script>

<style scoped>
a {
  transition: 0.4s;
  position: relative;
  display: block;
  font-weight: 700;
  font-size: 18px;
  color: rgb(255, 255, 255);
}

a::after {
  content: "";
  position: absolute;
  left: 50%;
  transform: translate(-50%, 50%);
  display: block;
  bottom: -30%;
}

a:hover::after {
  border: 1px solid rgb(255, 255, 255);
  width: 70%;
}
nav {
  max-width: 1920px;
  width: 100%;
  margin: 0 auto;
}
.close,
.open {
  display: none;
}

@media screen and (max-width: 768px) {
  nav {
    width: 100%;
    height: 136px;
    padding: 0;
  }

  .open,
  .close {
    position: absolute;
    top: 0;
    height: 136px;
    transform: translate(-50%, 50%);
    display: block;
    left: 30px;
  }

  .mobile {
    display: block;
  }
  .mobileNav {
    position: absolute;
    transform: translateX(-100vh);
    transition: 0.4s;
    background-color: rgb(255, 255, 255);
    width: 100%;
    height: 136px;
    top: 0;
    padding: 0 1rem;
    gap: 1.8rem;
    flex-wrap: wrap;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .mobileImg {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, 50%);
    height: 136px;
  }

  .mobileImg img {
    max-width: 5rem;
  }
  .showNav {
    transform: translateX(0);
  }

  a {
    color: black !important;
  }
}
</style>