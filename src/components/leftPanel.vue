<template>
  <f7-panel left parallax>
    <f7-list>
      <f7-list-item v-for="(item, index) in opcionesMenu" :key="index" :link="item.url">
        <f7-icon
          icon="icon-menu"
          v-bind:style="{ 'background-image': 'url(' + item.image + ')' }"
          :link="item.url"
        />
        <a :href="item.url">{{item.name}}</a>
      </f7-list-item>
    </f7-list>
  </f7-panel>
</template>

<script>
export default {
  props: ["opcionesMenu"]
};
</script>

<style lang="scss">
.icon-menu {
  width: 30px;
  height: 30px;
}
</style>