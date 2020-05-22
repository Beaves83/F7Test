<template>
    <f7-navbar theme-auto>
      <f7-nav-left>
        <f7-link>
          <img slot="media" src="https://agqlabs.es/wp-content/uploads/logo-1-01_sr.png" :width="120" />
        </f7-link>
      </f7-nav-left>
      <!-- <f7-nav-title>My App</f7-nav-title> -->
      <f7-nav-right>
        <f7-link class="consultas-avanzadas">Consultas avanzadas</f7-link>
        <!-- <f7-link><f7-icon material="inbox"></f7-icon></f7-link> -->
        <f7-link>
          <img slot="media" src="https://cdn.onlinewebfonts.com/svg/img_82283.png" :width="imageSize" />
        </f7-link>
        <f7-link>
            <!-- <f7-icon md="material:language" class="icon material-icons"> -->
              <img slot="media" src="https://toppng.com/uploads/preview/youtube-logo-transparent-square-for-kids-notification-bell-icon-11562857378pfhstovenl.png" :width="imageSize" />
            <f7-badge color="red">26</f7-badge>
        </f7-link> 
        <f7-link>
          <img slot="media" src="https://cdn.onlinewebfonts.com/svg/img_151687.png" :width="imageSize" />
        </f7-link>
        <f7-link>
          <img slot="media" src="https://pngimage.net/wp-content/uploads/2018/06/profile-png-icon-2.png" :width="imageSize" />
        </f7-link>
      </f7-nav-right>
    </f7-navbar>
</template>

<script>
    export default {
        data(){
          const imageSize = "35";
          return {
            imageSize
          }
      }
    }
    
</script>

<style lang="scss" scoped>
.consultas-avanzadas{
  background-color:red($color: #000000) ;
}
</style>