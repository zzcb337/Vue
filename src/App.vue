<template>
  <div id="app">
    
    <nav class="navbar is-transparent has-shadow">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item" href="https://bulma.io">
            Daz
          </a>
          <div class="navbar-burger burger" v-on:click="toggleNav" v-bind:class="{ 'is-active': isActive }">
            <span></span>
            <span></span>
            <span></span>
          </div>
        </div>

        <div class="navbar-menu" v-bind:class="{ 'is-active': isActive }">
          <div class="navbar-end">
            <router-link to="/" class="navbar-item r-item">Home</router-link>
            <router-link to="faq" class="navbar-item r-item">Features</router-link>
            <router-link to="faq" class="navbar-item r-item">About</router-link>
            <router-link to="faq" class="navbar-item r-item">FAQ</router-link>
            <div class="navbar-item">
              <p class="control">
                <a class="button is-primary is-outlined">
                  <span class="icon">
                    <i class="fa fa-download"></i>
                  </span>
                  <span>Join Now</span>
                </a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </nav>
    
    <router-view></router-view>
    
    <footer class="footer">
      <div class="container">
        <div class="columns">
          <div class="column">
            <p>This is my first vue project, and I am so excited. I wish I can meet Mr. Evan You and...
            </p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#">
              <i class="fa fa-facebook-official fa-2x" aria-hidden="true"></i>
            </a>
            <a class="icon" href="#">
              <i class="fa fa-twitter fa-2x" aria-hidden="true"></i>
            </a>
          </div>
        </div>
      </div>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'App',
  data: function () {
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function () {
      this.isActive = !this.isActive;
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'
.navbar 
  background-color: #383838
  a:hover
    color:#ddd
.navbar-brand a
  color:#fff
  text-transform: uppercase
  font-size: 1.2em
  font-weight: bold
a.r-item
  color: #c1c1c1
  padding: 0.5rem 1.75rem
  +mobile
    color: #777
    &:hover
      background-color: #f1f1f1
.navbar-burger
  color: #c1c1c1
.navbar-burger:hover
      color: #777
      background-color: #f1f1f1
footer
  background-color: $primary !important
  p, a
    color:#fff
  .icon
    margin-left: 15px
</style>
