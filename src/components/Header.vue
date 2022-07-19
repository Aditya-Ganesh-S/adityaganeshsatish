<template>
  <div>
    <header class="header">
      <div class="header__container">
        <div class="header__text-box">
          <div class="header__primary">
            <div class="header__primary--sub">Hi I am</div>
            <div class="header__primary--main"
              >Aditya Ganesh
              <span class="header__text--yellow">Satish</span></div
            >
            <div class="header__primary--sub text-3xl">
              Aspring
              <span class="header__text--yellow">Full Stack Developer</span>
            </div>
          </div>
        </div>
        <div>
          <img
            class="header__Image"
            src="../assets/img/portfolioPic.jpg"
            alt=""
          />
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss">
@import "@/assets/_shared.scss";
@import "@/assets/_header.scss";
</style>