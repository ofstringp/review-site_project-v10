<template lang="">
  <section class="hero bg-img is-large">
    <!-- Hero head: will stick at the top -->

    <div class="hero-head">
      <nav class="navbar">
        <div class="container">
          <div class="navbar-brand">
            <a class="navbar-item">
              <img
                src="https://bulma.io/images/bulma-type-white.png"
                alt="Logo"
              >
            </a>
            <span class="navbar-burger" data-target="navbarMenuHeroA">
              <span />
              <span />
              <span />
            </span>
          </div>
          <div id="navbarMenuHeroA" class="navbar-menu">
            <div class="navbar-end">
              <span class="navbar-item">
                <button class="button is-inverted is-link">
                  <span class="icon">
                    <i class="fab fa-check" />
                  </span>
                  <span>Leave a Review!</span>
                </button>
              </span>
            </div>
          </div>
        </div>
      </nav>
    </div>

    <!-- Hero content: will be in the middle -->
    <div class="hero-body">
      <div class="container ">
        <div class="columns is-justify-content-center">
          <div class="column is-8 box">
            <div class="columns is-align-items-end">
              <div class="column is-3">
                <b-field label="Cusine">
                  <b-autocomplete
                    :data="['jQuery', 'Vue', 'React']"
                    placeholder="e.g. jQuery"
                    icon="alert"
                    clearable
                    @select="option => (selected = option)"
                  >
                    <template #empty>
                      No results found
                    </template>
                  </b-autocomplete>
                </b-field>
              </div>
              <div class="column">
                <b-field label="Location">
                  <b-input
                    v-model="email"
                    placeholder="Email"
                    type="email"
                    icon="email"
                    icon-right="close-circle"
                    icon-right-clickable
                    @icon-right-click="clearIconClick"
                  />
                </b-field>
              </div>
              <div class="column is-1">
                <b-button
                  type="is-warning"
                  icon-right="magnify"
                  size="is-large"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
// const data1 = require('@/data/sample.json')
export default {
  layout: 'LandingPageLayout',
  data () {
    return {}
  }
}
</script>
<style lang="css">
.bg-img {
  background-image: url('/backdrop.jpeg');
  background-position: center center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-size: cover;
  background-color: #999;
}
</style>
