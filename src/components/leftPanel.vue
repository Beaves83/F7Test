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
    
      <f7-card 
        class="demo-facebook-card" no-shadow
       >
        <f7-card-content>
          <img src="https://t4.ftcdn.net/jpg/03/35/77/15/240_F_335771581_9cT3JjRzxYbgDh0rqy0Lu2dWEtGTd7pd.jpg" width="40" />
          <p >{{version}}</p>
        </f7-card-content>
      </f7-card>

  </f7-panel>
  
</template>

<script>

export default {
    props: ['version','opcionesMenu', 'imageSize','version'],
    // data() {
    //   const items = [
    //                     { url: '#', image: 'https://image.flaticon.com/icons/svg/2943/2943218.svg', name: 'enlace1' },
    //                     // { url: '#', image: 'https://banner2.cleanpng.com/20180410/zje/kisspng-borderlands-2-borderlands-3-tales-from-the-borderl-alphabet-collection-5acd7b9d83f218.3032657615234159655405.jpg', name: 'enlace2'  },
    //                     // { url: '#', image: 'https://cdn.icon-icons.com/icons2/1070/PNG/512/darth-vader_icon-icons.com_76959.png', name: 'enlace3'  },
    //                     // { url: '#', image: 'https://i.ya-webdesign.com/images/skyrim-icon-png-8.png', name: 'enlace4' },
    //                     { url: '#', image: 'https://image.flaticon.com/icons/svg/528/528111.svg', name: 'enlace5'  },
    //                     { url: '#', image: 'https://image.flaticon.com/icons/svg/743/743958.svg', name: 'enlace6'  }
    //                 ];
    //     const imageSize = 60;
    //   return {
    //     items, 
    //     imageSize
    //   };
    // },
};
</script>

<style lang="scss" scoped>
</style>