<template>
  <div class="floating-container" ref="image-ref">  
    <!-- <div class="inner-container" ref="image-ref">   -->
      <img ref="img" :src="image"/>
    <!-- </div> -->
  </div>
</template>

<script>
  export default {
    name: 'FloatingIconTwo',
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
    object-fit: contain;
    height: 100%;
  }
  img:hover {
    // width: 80%;
  }
  .floating-container {
    box-sizing: border-box;
    background-color: yellow;
    margin: 0% 10%;
    height: 200px;
    padding: 10px;
    width: 80%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: 0.5s;
  }
  .floating-container:hover {
    padding: 0px;
  }
</style>
