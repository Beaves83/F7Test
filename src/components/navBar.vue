<template>
  <f7-navbar :sliding="false" medium>
    <f7-nav-left>
      <f7-link icon-ios="f7:menu" icon-aurora="f7:menu" icon-md="material:menu" panel-open="left"></f7-link> 
    </f7-nav-left>
    <f7-nav-title>
      <img slot="media" src="https://agqlabs.es/wp-content/uploads/logo-1-01_sr.png" :width="120" />
    </f7-nav-title>
    <f7-nav-right sliding>
      <f7-link>Consultas avanzadas</f7-link>
      <f7-link>
        <f7-icon
          icon="icon-menu"
          v-bind:style="{ 'background-image': 'url(../static/img/fileCabinet.svg)' }"
        />
      </f7-link>
      <f7-link>
        <f7-icon
          icon="icon-menu"
          v-bind:style="{ 'background-image': 'url(../static/img/pepper.svg)' }"
        >
          <f7-badge color="red">99</f7-badge>
        </f7-icon>
      </f7-link>
      <f7-link>...</f7-link>
      <f7-link 
        href="/login/">
        <f7-icon
          icon="icon-menu"
          v-bind:style="{ 'background-image': 'url(../static/img/userProfile.svg)' }"
         
        />
      </f7-link>
    </f7-nav-right>
  </f7-navbar>
</template>

<style lang="scss" scoped>

</style>

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