<template>
  <f7-panel left cover theme-auto :visible-breakpoint="960">
    <f7-list media-list>      
        <f7-list-item
            v-for="(item, index) in opcionesMenu"
            :key="index"
            :link="item.url">
            <img slot="media" :src="item.image" :width="imageSize" />
            <a>{{item.name}}</a>
        </f7-list-item>
    </f7-list>
    <f7-block>
      <img src="https://t4.ftcdn.net/jpg/03/35/77/15/240_F_335771581_9cT3JjRzxYbgDh0rqy0Lu2dWEtGTd7pd.jpg" width="40" />
          <p >{{version}}</p>
    </f7-block>

  </f7-panel>
</template>

<script>

export default {
    props: ['version','opcionesMenu', 'imageSize'],

};
</script>

<style lang="scss" scoped>
 
</style>