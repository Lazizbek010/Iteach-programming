<template>
  <div class="app">
    <div class="bg">
      <div class="circles">
      <div class="circle" v-for="(item, i) in 6" :key="`circle${i}`"></div>
      </div>
      <div class="back">
        <div class="blur" v-for="(item, i) in 3" :key="`blur${i}`"></div>
      </div>
    </div>
    <nav class="nav">
      <div class="container">
        <div class="nav-menu">
          <router-link class="logo" :to="{ name: 'home' }">
            <img src="/images/logo.svg" alt="" />
          </router-link>
          <div class="menu">
            <button
              class="hamburger"
              :class="{ open: menuOpen }"
              @click.prevent="openMenu()"
            >
              <span></span><span></span><span></span>
            </button>
            <ul :class="{'open': menuOpen}">
              <li><a class="active" href="#">Asosiy</a></li>
              <li><a href="#">Xizmatlar</a></li>
              <li><a href="#">Ish jarayoni</a></li>
              <li><a href="#">Portfolio</a></li>
              <li><a href="#">Kadrlar</a></li>
              <li><a href="#">Mijozlar fikri</a></li>
              <li><a href="#">Hamkorlar</a></li>
            </ul>
          </div>
        </div>
        <div class="nav-options">
          <div class="calc">
            <img src="/images/calc.svg" alt="calc icon" />
            Kalkulyator
          </div>
          <a class="phone" href="tel:998906310977">
            <img src="/images/phone.svg" alt="phone icon" />
            +998906310977
          </a>
          <div class="lang">
            <div class="current" @click="openLangs()">
              <img src="/images/Globus.svg" alt="" />
              UZ
              <img src="/images/Arrow down.svg" alt="" />
            </div>
            <div class="others" :class="{open: langsOpen}">
              <button>RU</button>
              <button>EN</button>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
  <!-- <router-view /> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      menuOpen: false,
      langsOpen: false,
    };
  },
  methods: {
    openMenu() {
      this.menuOpen = !this.menuOpen;
    },
    openLangs() {
      this.langsOpen = !this.langsOpen;
    },
  },
};
</script>


