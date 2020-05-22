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

  export default {
    components:{
        'navBar': navBar,
        'leftPanel': leftPanel,
      },
    data() {
      const opcionesMenu = [
                        { url: '#', image: 'https://image.flaticon.com/icons/svg/2943/2943218.svg', name: 'enlace1' },
                        { url: '#', image: 'https://banner2.cleanpng.com/20180410/zje/kisspng-borderlands-2-borderlands-3-tales-from-the-borderl-alphabet-collection-5acd7b9d83f218.3032657615234159655405.jpg', name: 'enlace2'  },
                        { url: '#', image: 'https://cdn.icon-icons.com/icons2/1070/PNG/512/darth-vader_icon-icons.com_76959.png', name: 'enlace3'  },
                        { url: '#', image: 'https://i.ya-webdesign.com/images/skyrim-icon-png-8.png', name: 'enlace4' },
                        { url: '#', image: 'https://image.flaticon.com/icons/svg/528/528111.svg', name: 'enlace5'  },
                        { url: '#', image: 'https://image.flaticon.com/icons/svg/743/743958.svg', name: 'enlace6'  }
                    ];
      const version = "v 0.10";
      const imageSize = "60";
      return {
        opcionesMenu,
        version,
        imageSize,
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