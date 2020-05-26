<template>
  <f7-page name="borderland">
    <navBar />
    <f7-block>
      <div class="image">
        <img
          src="https://banner2.cleanpng.com/20180410/zje/kisspng-borderlands-2-borderlands-3-tales-from-the-borderl-alphabet-collection-5acd7b9d83f218.3032657615234159655405.jpg"
          width="300"
        />
      </div>
    </f7-block>

    <f7-block-title>Borderland</f7-block-title>
    <f7-block strong>
      <p>Fugiat perspiciatis excepturi, soluta quod non ullam deleniti. Nobis sint nemo consequuntur, fugiat. Eius perferendis animi autem incidunt vel quod tenetur nostrum, voluptate omnis quasi quidem illum consequuntur, a, quisquam.</p>
      <p>Laudantium neque magnam vitae nemo quam commodi, in cum dolore obcaecati laborum, excepturi harum, optio qui, consequuntur? Obcaecati dolor sequi nesciunt culpa quia perspiciatis, reiciendis ex debitis, ut tenetur alias.</p>
    </f7-block>
    <f7-block>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni molestiae laudantium dignissimos est nobis delectus nemo ea alias voluptatum architecto, amet similique, saepe iste consectetur in repellat ut minus quibusdam!</p>
      <p>Molestias et distinctio porro nesciunt ratione similique, magni doloribus, rerum nobis, aliquam quae reiciendis quasi modi. Nam a recusandae, fugiat in ea voluptates fuga eius, velit corrupti reprehenderit dignissimos consequatur!</p>
      <p>Blanditiis, cumque quo adipisci. Molestiae, dolores dolorum quos doloremque ipsa ullam eligendi commodi deserunt doloribus inventore magni? Ea mollitia veniam nostrum nihil, iusto doloribus a at! Ea molestiae ullam delectus!</p>
    </f7-block>
  </f7-page>
</template>

<style>
    .image {
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>

<script>
import navBar from "../components/navBar";

export default {
  components: {
    navBar
  },
  data() {
    return {
      navBar
    };
  }
};
</script>