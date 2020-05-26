<template>
  <f7-panel left cover theme-auto :visible-breakpoint="960">
    <f7-list>       
        <f7-list-item
            v-for="(item, index) in opcionesMenu"
            :key="index"                   
            :link="item.url">
            <img slot="media" :src="item.image" :width="50"/>
            <!-- <f7-icon material="inbox"
            size="45px"
            ></f7-icon> -->
            <a>{{item.name}}</a>   
        </f7-list-item>
    </f7-list>
  </f7-panel>
</template>

<script>
export default {
  props: ["opcionesMenu"]
};
</script>