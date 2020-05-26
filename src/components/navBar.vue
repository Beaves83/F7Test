<template>
  <f7-navbar>
 
    <f7-nav-left large :sliding="false">
      <f7-link icon-ios="f7:menu" icon-aurora="f7:menu" icon-md="material:menu" panel-open="left"></f7-link>
      <f7-link>
        <img slot="media" src="https://agqlabs.es/wp-content/uploads/logo-1-01_sr.png" :width="120" />
      </f7-link>
    </f7-nav-left>
    <!-- <f7-nav-title>My App</f7-nav-title> -->
    <f7-nav-right>
      <f7-link>Consultas avanzadas</f7-link>
      <f7-link>
        <f7-icon material="inbox"></f7-icon>
      </f7-link>
      <f7-link>
        <f7-icon md="material:language" class="icon material-icons">
          <f7-badge color="red">26</f7-badge>
        </f7-icon>
      </f7-link>
      <f7-link>...</f7-link>
      <f7-link>
        <f7-icon material="face"></f7-icon>
      </f7-link>
    </f7-nav-right>
  </f7-navbar>
</template>

<script>
export default {
  data() {
    const imageSize = "35";
    return {
      imageSize
    };
  }
};
</script>

<style lang="scss" scoped>

</style>