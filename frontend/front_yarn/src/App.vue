<script setup lang="ts"></script>

<template>
  <div id="app">
    <router-view />

    <div class="announcement_bar">
      <h3 class="announcement_bar_text">Welcome to our shop</h3>
    </div>
    <header>
      <div class="sidebar" id="sidebar"></div>
      <!--       <div class="sandwich" id="btn" v-on:click="switch_sidebar()">
        <div class="stick"></div>
        </div> -->
      <div class="logo"><img src="../pictures/Scottish_Yarns_LOGO00000000000.png" /></div>
      <div class="search"><img src="../pictures/magnifying-glass.svg" /></div>
      <div class="bin"><img src="../pictures/cart-shopping.svg" /></div>
    </header>

    <footer>
      <div class="columns">
        <div class="first_column">
          <ul class="footer_list">
            <li><h3 class="footer_header">shop</h3></li>
            <li>Tallinn</li>
            <li>Tallinn</li>
            <li>Tallinn</li>
            <li>Tallinn</li>
          </ul>
        </div>

        <div class="second_column">
          <ul class="footer_list">
            <li><h3 class="footer_header">contact</h3></li>
            <li>sc0tt1sh.y4rns@gmail.com</li>
            <li>+372 5057976</li>
            <li>ACQUIRO OÜ</li>
            <li>Tallinn</li>
          </ul>
        </div>
      </div>

      <hr class="line_in_footer" />

      <div class="copyright_payments">
        <p class="copyright">
          2024, Scottish Yarns Powered by @artjom_sidorenko
        </p>

        <div id="payments">
          <ul id="ul_of_payments">
            <li>paypal</li>
            <li>swedband</li>
            <li>sberbank</li>
          </ul>
        </div>
      </div>
    </footer>
  </div>
</template>

<style>
.announcement_bar {
  position: absolute;
  width: 100%;
  background-color: #3e4a51;
  height: 40px;
  top: 0;
  left: 0;
  display: flex;
  justify-content: center;
}

.announcement_bar_text {
  color: white;
  text-transform: uppercase;
  padding: auto;
  margin: auto;
}

.sidebar {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 0;
  top: 0;
  left: 0;
  opacity: 80%;
  background: rgb(255, 255, 255);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  border-radius: 10px;
  overflow-x: hidden;
  padding-right: 20px;
  transition-property: width;
  transition-duration: 1s;
  transition-timing-function: ease-out;
}

.sidebar.active {
  width: 45%;
  opacity: 80%;
  background: rgb(255, 255, 255);
  backdrop-filter: blur(4px);
  -webkit-backdrop-filter: blur(4px);
  border-radius: 10px;
  border: 1px solid rgba(255, 255, 255, 0.18);
}

.sandwich {
  position: relative;
  top: 15px;
  width: 15px;
  height: 8px;
  z-index: 2;
  cursor: pointer;
}

.stick,
.stick::before,
.stick::after {
  position: absolute;
  width: 25px;
  height: 2px;

  background: black;

  transition: all 0.6s;
  transform-origin: 50% 50%;
}

.stick::before {
  content: "";
  position: absolute;
  top: -6px;
  left: 0;
}

.stick::after {
  content: "";
  position: absolute;
  top: 6px;
  left: 0;
}

.stick.trigger {
  transform: rotate(180deg);
}

.stick.trigger::after {
  transform-origin: 100% 50%;
  transform: translateY(-7px) rotate(-45deg) scaleX(0.7);
}

.stick.trigger::before {
  transform-origin: 100% 50%;
  transform: translateY(7px) rotate(45deg) scaleX(0.7);
}

header {
  position: absolute;
  width: 100%;
  height: 100px;
  /*   color: #F5F3F0; */
  background-color: #f5f3f0;
  top: 40px;
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.logo {
max-width: 128px;
max-height: 128px;
}
.search,
.bin {
  width: 20px;
  height: 20px;
}

footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  background-color: #3e4a51;
  height: 300px;
}

.footer_list {
  list-style: none;
}

.first_column {
}

.second_column {
}

.footer_header {
  text-transform: uppercase;
  padding-bottom: 10%;
}

.line_in_footer {
  width: 100%;
  size: 1px;
  position: absolute;
  margin-top: 15px;
  background: white;
}

.columns {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  margin-top: 15px;
}

.copyright_payments {
  position: absolute;
  bottom: 0;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.copyright {
  font-size: 10px;
  letter-spacing: 1px;
}

#payments {
  display: inline;
}
#ul_of_payments li {
  display: inline;
  padding: 5px;
}
</style>
