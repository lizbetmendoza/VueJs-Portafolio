<template>
  <div id="app">
    <div class="navbar has-shadow">
      <div class="container ">
        <div class="navbar-start">
          <a class="navbar-item">My portafolio</a>
        </div>

        <span class="navbar-burger" v-on:click="toggleNav" v-bind:class="{'is-active': isActive}">
          <span></span>
          <span></span>
          <span></span>
        </span>

        <div class="navbar-end navbar-menu" v-bind:class="{'is-active': isActive }">
          <router-link to="/" class="navbar-item r-item">Home</router-link>
          <router-link to="/" class="navbar-item r-item">AboutMe</router-link>
          <router-link to="/" class="navbar-item r-item">ContactMe</router-link>

        </div>
      </div>
    </div>
    <router-view></router-view>

    <footer class="footer is-primary">
      <div class="container">
        <div class="columns">
          <div class="columns">
            <p>This is an space, where you can put information about footer</p>
          </div>
          <div class="column has-text-right">
            <a class="icon" href="#"><i class="fa fa-facebook"></i></a>
            <a class="icon" href="#"><i class="fa fa-twitter"></i></a>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function(){
    return {
      isActive: false
    }
  },
  methods: {
    toggleNav: function() {
      this.isActive =!this.isActive; 
    }
  }
}
</script>

<style lang="sass">
@import '../node_modules/bulma/bulma.sass'
@import 'mq'


.navbar 
  background-color: #383838
  a hover
    color: gray

.navbar-start a
  color: #fff
  font-weight:bold

a.r-item
  color: #C1C1C1
  padding: 0.5rem 1.75rem
  +mobile
      color: gray
      &:hover
        background-color: #F1F1F1

.navbar-end a
  
  font-weight:bold

.navbar-burger span
  background-color: #F1F1F1

footer
  background-color: $primary !important
  color: #fff

  .icon
    color: #fff
    margin-left: 20px

    .icon hover
      color: red

</style>
