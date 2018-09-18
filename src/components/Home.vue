<template>
  <div class="home">
    <section class="hero">
      <div class="hero-body">
        <div class="container">
          <h1 class="title">{{ heading }}</h1>
          <div class="is-two-thirds column is-paddingless">
            <h2 class="subtitle is-2 has-text-centered">{{ subheading }}</h2>
          </div>
        </div>
      </div>
    </section>

    <section class="section">
      <div class="container">
        <div class="columns pd is-desktop">
          <!--<div class="column is-1 has-text-centered">    
            <i class="fa fa-cog is-primary"></i>
          </div>-->
          <div class="column has-text-centered"> <!-- is-one-third-desktop -->
            <!--<p class="title"><strong>We provide superior logistics so that your business can succeed in a crazy world.</strong></p>-->
            <img src="../assets/me.svg">
          </div>
          <div class="column has-text-centered">
            <p class="title is-1 is-primary">Hi, my name is Liz<br>I am a Web Developer</p><br>
            <p class="subtitle is-4">I am interested in pursuing a career in software development<br> I have experience as a web developer,<br> I consider myself a fast learner,<br> involved in different projects and <br>complete project cycles, testing, <br>and final implementations.</p>
          </div>
        </div>
      </div>

      <div class="columns pd">
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="subtitle">- Technical Skills</p>
              <p class="subtitle">C#. Net, ASP.Net, PHP, jQuery, jQuery Mobile,	JavaScript, Adobe Photoshop.<br>
	              Databases:	 MySQL, SQL server
                Webserver: 	XAMPP control (cross-platform), AWS Amazon Web Services 
              </p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="subtitle">Web Sites</p>
              <p class="subtitle">"I think it's an absolutely excellent tool for our business. I can't survive without this thing."</p>
            </div>
          </div>
        </div>
        <div class="column">
          <div class="card">
            <div class="card-content">
              <p class="subtitle">GitHub</p>
              <p class="subtitle">"I think it's an absolutely excellent tool for see my playground :-)<br>
                 I can't survive without this thing."</p>
              
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      heading: 'This is me :-)',
      subheading: '...and I love what I do'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
  @import '../mq'

  .hero
    background: url('../assets/header.png')
    background-size: cover

  .title
    +mobile
      font-weight: bold
    +tablet
      font-size: 2.5rem
    +desktop
      font-size: 4rem
      margin-top: 2rem
  h1
    margin: 1.5rem 0 2rem 18rem !important
  h2
    margin: 1.5rem 0 2rem 0 !important

  .fa-cog
    font-size: 40px

  #learn
    +desktop
      margin-bottom: 2rem

  .pd
    +tablet
      padding: 2em 0

</style>
