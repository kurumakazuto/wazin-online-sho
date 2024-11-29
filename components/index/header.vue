<script setup lang="ts">

const hamburgerButton = ref();
hamburgerButton.value = "open";

</script>

<template>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">

  <header class="header">
    <h1 class="headerLogo">
      <a href="#"><img src="../img/wazin.svg" alt="Wazin online shop"></a>
    </h1>

    <button class="searchButton">
      <i class="bi bi-search"></i>
    </button>
    <button type="button" class="hamburgerButton">
      <span class="hamburgerButtonBar"></span>
      <span class="hamburgerButtonBar"></span>
      <span class="hamburgerButtonBar"></span>
    </button>

    <div class="hamburgerMenu" v-if="hamburgerButton === 'open'">
      <nav class="hamburgerNavList">
        <ul class="hamburgerNavListgroup">
          <li>
            <NuxtLink :to="{name: 'contents-newArrival'}">新着情報</NuxtLink>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>

img {
  max-width: 100%;
  height: auto;
  vertical-align: bottom;
}

.header {
  position: fixed;
  top: 12px;
  left: 8px;
  z-index: 1;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 3.75rem;
  width: calc(100% - 16px);
  border-bottom: solid 2px black;
}

.headerLogo img {
  max-width: 10rem;
}

.searchButton {
  position: fixed;
  top: 1.5rem;
  right: 4.875rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: none;
  background-color: white;
  font-size: 1.75rem;
}

.hamburgerButton {
  position: fixed;
  top: 1.6875rem;
  right: 1.25rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  border: none;
  background-color: white;
}

.hamburgerButtonBar {
  width: 1.5rem;
  height: 0.125rem;
  background-color: black;
}

.hamburgerButtonBar:first-child,
.hamburgerButtonBar:nth-child(2) {
  margin-bottom: 0.5rem;
}

@media (max-width: 47.9937rem) {
  .hamburgerMenu[data-v-e58b9687] {
    position: fixed;
    top: 4.625rem;
    left: 0;
    width: 100%;
    padding-top: 1.625rem;
    background-color: #ececec;
    transition: all 0.6s;
  }
}

</style>