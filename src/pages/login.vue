<template>
  <f7-page name="login" no-toolbar no-navbar no-swipeback login-screen>
    <f7-block>
      <!-- Login -->
      <div class="text-align-center">
        <img
          width="280"
          height="auto"
          src="https://agqlabs.es/wp-content/uploads/logo-1-01_sr.png"
          alt="AGQLabs"
        />
      </div>
      <div class="label-text">Acceso</div>
      <f7-list form id="list-form">
        <!-- Username -->
        <f7-list-input
          outline
          label="Username"
          item-label
          type="text"
          placeholder="Your username"
          clear-button
          @input="username = $event.target.value"
          name="username"
          max="255"
          required
        />
        <!-- Password -->
        <f7-list-input
          outline
          label="Password"
          item-label
          type="password"
          placeholder="Your password"
          clear-button
          @input="password = $event.target.value"
          name="password"
          max="255"
          required
        />
      </f7-list>

      <!-- Remember me -->
      <f7-list>
        <f7-list-item
          checkbox
          title="Remember me"
          name="restore-checkbox"
          
         
        ></f7-list-item>
        <!-- :checked="wantToRemember" -->
         <!-- ^^ @change="setWantToRemember" ^^ -->
      </f7-list>

      <!-- Buttons -->
      <f7-list>
        <f7-button
          col
          button
          button-large
          button-raised
          fill
          @click="signIn"
          
        >Sign in</f7-button>
        <!-- ^^ :disabled="btnDisable" ^^ -->
      </f7-list>
      <f7-list>
        <f7-button col button button-large button-raised fill @click="quit">Return</f7-button>
      </f7-list>
    </f7-block>
  </f7-page>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {
      username: "",
      password: ""
    };
  },
  //   computed: {
  //     btnDisable: function() {
  //       return this.username && !this.wantToRemember && !this.password;
  //     },
  //     appName: function() {
  //       return this.appConfig.name;
  //     },
  //     appLogo() {
  //       return localStorage.getItem("applogo") || this.appConfig.logoUrl;
  //     },
  //     ...mapState("authentication", ["isLogged", "wantToRemember", "appConfig"])
  //   },

  methods: {
    signIn() {
      const self = this;
      const app = self.$f7;
      const router = self.$f7router;
      app.dialog.alert(
        `Username: ${self.username}<br>Password: ${self.password}`,
        () => {
          router.back();
        }
      );
    },
    quit() {
      const self = this;
      const app = self.$f7;
      const router = self.$f7router;
      router.back();
    }
    // async signIn(event) {
    //     this.$f7.preloader.show();
    //     let user = {
    //       username: this.username,
    //       password: this.password
    //     }
    //     try {
    //       await this.login(user);
    //     } catch (reason) {
    //       this.$f7.dialog.alert(reason);
    //     }
    //     this.$f7.preloader.hide();
    //   },
    //   ...mapActions('authentication', ['login']),
    //   ...mapMutations('authentication', ['setWantToRemember'])
  }
};
</script>