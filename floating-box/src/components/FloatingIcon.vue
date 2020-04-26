<template>
  <div v-if="href == null" class="floating-container" ref="image-ref">
    <img ref="img" :src="image"/>
    <p>{{width}}</p>
  </div>
  <div v-else class="floating-container">
    <a :href="href">
      <img :src="image"/>
    </a>
  </div>
</template>

<script>
  export default {
    name: 'FloatingIcon',
    props: {
      image: {
        required: true,
        type: String
      },
      // height: {
      //   required: true,
      //   type: Number
      // },
      href: String,
    },
    data: function() {
      return {
          // width: this.$refs["image-ref"].width
          width: this.$refs["image-ref"].width
        };
    },
    mounted:function(){
      // let height = this.$refs["image-ref"].style.backgroundColor = 'black';
    },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  $height: 200px;
  img {
    width: 70%;
    transition: 0.5s;
    max-height: 90%;
  }
  img:hover {
    width: 80%;
  }
  .floating-container {
    background-color: blue;
    height: $height;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>
