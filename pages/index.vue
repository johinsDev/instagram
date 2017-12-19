<template lang="pug">
  div.align-center#main-container
    section
      v-layout(row)
        v-flex(xs12 sm12 md8 offset-md2 lg8 offset-lg2)
          v-layout(row align-center)
            v-flex.text-xs-center(sm6 hidden-xs-only)
              img.iphone(src="../static/iphone.png" alt="iphone")
            v-flex(xs12 sm6)
              div.signup-box
                h1.instagram Instagram
                v-form.signup-form
                  h2 Registrate para ver fotos de tu amigos programando.
                  div.section
                    v-btn.btn-fb.hidden-xs-only(color="primary") Iniciar Sesión con Facebook
                    v-btn.hidden-md-and-up(color="primary") Iniciar Sesión
                  div.section
                    v-text-field(label="Name" name="name")
                    v-text-field(label="E-mail" name="email")
                    v-text-field(label="Username" name="username")
                    v-text-field(label="Password" type="password")
                    v-btn(color="primary") Registrarse
                
              v-layout(row mt-3)
                div.login-box ¿Tienes una cuenta?
                  a(href="/signin") Entrar
  
    footer.site-footer
      v-layout(row)
        v-flex(xs12 md10 offset-md1)
          v-layout(row justify-space-between align-center)
            v-flex(xs12 lg3)
              v-select(
                :items="languages"
                append-icon=""
                label="Idioma"
                single-line
                bottom
              )
            v-flex.text-lg-right.text-xs-right.text-sm-right(xs12 lg3 justify-end) © 2017 Instagram
</template>

<script>
  export default {
    data () {
      return {
        languages: [
          { text: 'Español' },
          { text: 'Inglés' }
        ]
      }
    }
  }
</script>

<style lang="stylus" scoped>
  #main-container
    margin: 0 auto

  .iphone
    max-width: 100%
    max-height: 700px

  .site-footer
    text-transform: uppercase
    font-size: 12px

  .login-box
    background-color: white
    border: 1px solid #edeeee
    padding: 10px 0
    text-align: center
    width: 100%

  .signup-box
    @extend .login-box
  
  .signup-box
    .instagram
      font-family: 'Oleo Script'
      font-size: 42px
  
  .signup-form
    width: 65%
    margin: 0 auto
    h2
      font-size: 1.2em
      color: #a5a7aa
   .btn-fb
    background-color: #4090db !important
    font-size: .9em
    &:hover
      background-color: #2d6599 !important
</style>