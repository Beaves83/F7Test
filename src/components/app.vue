<template>
  <f7-app :params="f7params" >



  <!-- Left panel with cover effect when hidden -->
  <f7-panel left cover theme-auto :visible-breakpoint="960">
    <f7-view>
      <f7-page>
        <!-- <f7-navbar title="Left Panel"></f7-navbar>
        <f7-block-title>Left View Navigation</f7-block-title>
        <f7-list>
          <f7-list-item link="/left-page-1/" title="Left Page 1"></f7-list-item>
          <f7-list-item link="/left-page-2/" title="Left Page 2"></f7-list-item>
        </f7-list>
        <f7-block-title>Control Main View</f7-block-title>
        <f7-list>
          <f7-list-item link="/about/" view=".view-main" panel-close title="About"></f7-list-item>
          <f7-list-item link="/form/" view=".view-main" panel-close title="Form"></f7-list-item>
          <f7-list-item link="#" view=".view-main" back panel-close title="Back in history"></f7-list-item>
        </f7-list> -->
        <!-- <f7-block-title>Nueva botonera</f7-block-title> -->
        <f7-list>
          <f7-list-item icon-f7="home" link="/about/" view=".view-main" panel-close title=""><i class="f7-icons">ant_circle_fill</i></f7-list-item>
          <f7-list-item link="/form/" view=".view-main" panel-close title=""><i class="f7-icons">house_fill</i></f7-list-item>
          <f7-list-item  link="#" view=".view-main" back panel-close title=""><i class="f7-icons">leaf_arrow_circlepath</i></f7-list-item>
          <f7-list-item  link="#" view=".view-main" back panel-close title=""><i class="f7-icons">light_max</i></f7-list-item>
          <f7-list-item  link="#" view=".view-main" back panel-close title=""><i class="f7-icons">logo_apple</i></f7-list-item>
          <f7-list-item  link="#" view=".view-main" back panel-close title=""><i class="f7-icons">ant_circle_fill</i></f7-list-item>
        </f7-list>
      </f7-page>
    </f7-view>
  </f7-panel>


  <!-- Right panel with reveal effect-->
  <!-- <f7-panel right reveal theme-dark>
    <f7-view>
      <f7-page>
        <f7-navbar title="Right Panel"></f7-navbar>
        <f7-block>Right panel content goes here</f7-block>
      </f7-page>
    </f7-view>
  </f7-panel> -->


  <!-- Your main view, should have "view-main" class -->
  <f7-view main class="safe-areas" url="/"></f7-view>

    <!-- Popup -->
    <f7-popup id="my-popup">
      <f7-view>
        <f7-page>
          <f7-navbar title="Popup">
            <f7-nav-right>
              <f7-link popup-close>Close</f7-link>
            </f7-nav-right>
          </f7-navbar>
          <f7-block>
            <p>Popup content goes here.</p>
          </f7-block>
        </f7-page>
      </f7-view>
    </f7-popup>

    <f7-login-screen id="my-login-screen">
      <f7-view>
        <f7-page login-screen>
          <f7-login-screen-title>Login</f7-login-screen-title>
          <f7-list form>
            <f7-list-input
              type="text"
              name="username"
              placeholder="Your username"
              :value="username"
              @input="username = $event.target.value"
            ></f7-list-input>
            <f7-list-input
              type="password"
              name="password"
              placeholder="Your password"
              :value="password"
              @input="password = $event.target.value"
            ></f7-list-input>
          </f7-list>
          <f7-list>
            <f7-list-button title="Sign In" @click="alertLoginData"></f7-list-button>
            <f7-block-footer>
              Some text about login information.<br>Click "Sign In" to close Login Screen
            </f7-block-footer>
          </f7-list>
        </f7-page>
      </f7-view>
    </f7-login-screen>
  </f7-app>
</template>
<script>

  import routes from '../js/routes.js';

  export default {
    data() {
      return {
        // Framework7 Parameters
        f7params: {
          name: 'BibiTestF7', // App name
          theme: 'auto', // Automatic theme detection
          titulo: 'titulo desde app vue',
          listado: ['elemento1','elemento2','elemento3','elemento4'],


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