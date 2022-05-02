<template>
    <div class="container">
      <input type="text" v-model="productID">
      <button class="button--green" @click="showProduct"> Ürünü Göster</button>
      <button class="button--green mainPage" @click="goToMainPage">Ana Sayfa</button>
    </div>
</template>
<script>
  export default {
    layout : "product",
    data(){
      return {
        productID : null
      }
    },
    methods : {
      showProduct(){
        if(this.productID !== null){
          this.$router.push("/products/" + this.productID)
          this.productID = ""
        }else{

        }
      },
      goToMainPage(){
        this.$router.push("/")
      }
    }
  }
</script>
<style scoped>
  .container{
    padding: 20px;
    border: 1px solid #688fb9;
    /*margin-top: 50px;*/
    background-color: #35495e;
    box-shadow: 2px 3px 8px rgba(0,0,0,.1);
  }
  .mainPage{
    float: right;
  }
  input{
    border: none;
    outline: none;
    height: 35px;
    font-size: 18px;
    color: #35495e;
  }
</style>
