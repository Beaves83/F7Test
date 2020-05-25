<template>
  <f7-app :params="f7params" >

  <navBar />
  <leftPanel :version=version :imageSize= imageSize :opcionesMenu= opcionesMenu  />

  <!-- Your main view, should have "view-main" class -->
  <f7-view main class="safe-areas" url="/"></f7-view>
    
  </f7-app>
</template>
<script>

  import routes from '../js/routes.js';
  import navBar from '../components/navBar'
  import leftPanel from '../components/leftPanel'
  import opcionesMenu from '../json/menuList.json'

  export default {
    components:{
        'navBar': navBar,
        'leftPanel': leftPanel,
      },
    data() {
    
      const version = "v 0.10";
      const imageSize = "50";
      return {
        version,
        imageSize,
        opcionesMenu,
        // Framework7 Parameters
        f7params: {
          name: 'BibiTestF7', // App name
          theme: 'auto', // Automatic theme detection
          titulo: 'titulo desde app vue',
          // App routes
          routes: routes,
        },
        // Login screen data
        username: '',
        password: '',
      }
    },
    methods: {
      alertLoginData() {
        this.$f7.dialog.alert('Username: ' + this.username + '<br>Password: ' + this.password, () => {
          this.$f7.loginScreen.close();
        });
      }
    },
    mounted() {
      this.$f7ready((f7) => {

        // Call F7 APIs here
      });
    }
  }
</script>