<template>
  <div class="box">
    <div class="line">
      <img src="../assets/line/line01.png" class="line01">
    </div>
    <div class="line">
      <img src="../assets/line/line02.png" class="line02">
    </div>
    <div class="line">
      <img src="../assets/line/line03.png" class="line03">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Circle'

}
</script>

<style scoped>
  .box{
    width: 250px;
    height: 250px;
  }
   .line img{
    width:250px;
    height:250px;
    border-radius:50%;
   }
   .line{
     position:absolute;
   }
   .line02{
    animation:line02 5s linear infinite;
    animation-direction:normal;
   }
  .line03{
    animation:line 5s linear infinite;
    animation-direction:normal;
   }
   @keyframes line{
      from {
        transform: rotateZ(0);
      }
      to {
        transform: rotateZ(360deg);
      }
    }
    @keyframes line02{
      from {
        transform: rotateZ(0);
      }
      to {
        transform: rotateZ(-360deg);
      }
    }
</style>
