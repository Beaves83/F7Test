<template>
  <f7-panel left cover theme-auto :visible-breakpoint="960">
    <!-- <f7-block>
      <f7-link
        v-for="(item, index) in opcionesMenu"
        :key="index"
        :href="item.url"
        class="opcionMenu"
      >
        <img slot="media" :src="item.image" :width="imageSize" />
        <a>{{item.name}}</a>
      </f7-link>
    </f7-block> -->

    <!-- <f7-list>
  <f7-list-item title="Item 1"></f7-list-item>
  <f7-list-item title="Item 2"></f7-list-item>
    </f7-list>-->

    <f7-list >       
        <f7-list-item
            v-for="(item, index) in opcionesMenu"
            :key="index"
                    
            :link="item.url">
            <img slot="media" :src="item.image" :width="imageSize"/>
            <a>{{item.name}}</a>   
            <!-- <div slot="root">{{item.name}}</div> -->
        </f7-list-item>
    </f7-list>
    <!-- <f7-block class>
      <img
        src="https://pluspng.com/img-png/exit-png-exit-icon-image-4600-512.png"
        width="40"
      />
      <p>{{version}}</p>
    </f7-block> -->
     
  </f7-panel>
</template>

<script>
export default {
  props: ["version", "opcionesMenu", "imageSize"]
};
</script>

<style lang="scss" scoped>
// .panel {
//   max-width: 7vw;
// }
// .opcionMenu {
//   padding: 10%;
// }
</style>