<template>
  <div class="home">
    <div class="Home__Nav">
      <div class="Cicrle__right" :class="{'Circle--paused':ToggleRight}">
        <div class="Cicrle__content" @mouseover='OpenRight' @mouseout='CloseRight' >
          <p>自我评估</p>
        </div>
      </div>
      <div class="Cicrle__left" :class="{'Circle--paused':ToggleLeft}">
        <div class="Cicrle__content" @mouseover='OpenLeft' @mouseout='CloseLeft' >
          <p>名校展示</p>
        </div>
      </div>
      <div class="Circuit">
        <img src="../assets/home.png" width="60%" class="Circuit__gear" :class="{'Circle--paused':Hover}">
      </div>
    </div>
    <div class="bottom">
      <div class="bottom__left">
        <div class="bottom__left__oricl"></div>
        <p>Copyright @ 2016 北京箐英天下国际教育咨询有限公司 版权所有 京ICP备 15000012号</p>
      </div>
      <div class="bottom__right">
        <div class="bottom__right__oricl"></div>
        <p>技术支持：&nbsp北京赛亚数据科技有限公司</p>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: 'HomeNav',
  data () {
    return {
      ToggleRight: false,
      ToggleLeft: false,
      Hover: false
    }
  },
  methods: {
    OpenRight () {
      this.ToggleRight = true
      this.Hover = true
    },
    CloseRight () {
      this.ToggleRight = false
      this.Hover = false
    },
    OpenLeft () {
      this.ToggleLeft = true
      this.Hover = true
    },
    CloseLeft () {
      this.ToggleLeft = false
      this.Hover = false
    }
  }

}
</script>

<style scoped>
.bottom{
  width:100%;
  height: 50px;
  position: fixed;
  bottom: 0;
}
.bottom__left{
  width:39.5%;
  position:absolute;
  bottom:0;
  left: -2%;
  height:40px;


}
.bottom__left__oricl{
  height:40px;
  position: absolute;
  bottom:0;
  width:100%;
  border-top:2px solid rgb(177, 218, 217);
  border-right: 3px solid rgb(177, 218, 217) ;
  transform:  perspective(1em) rotateX(5deg);
}
.bottom__right{
  width:38%;
  height:40px;
  position:absolute;
  bottom: 0;
  right: -2%;
}
.bottom__right__oricl{
  height:40px;
  position: absolute;
  bottom:0;
  width:100%;
  border-top:2px solid rgb(177, 218, 217);
  border-left: 3px solid rgb(177, 218, 217) ;
  transform:  perspective(1em) rotateX(5deg);
}
.bottom p{

  color:rgb(177, 218, 217);
  text-align: center;
  line-height:20px;
  font-size:12px;
  display:block;
}
.Home__Nav{
  width:730px;
  height:500px;
  margin: auto;
  position: fixed;
  bottom: 0;
  left: 0;
  right:0;
}
.Home__Nav p{
  color:white;
  text-align: center;
  line-height:75px;
}
.Cicrle__content{
  width:125px;
  height: 125px;
  cursor:pointer;
  position:absolute;
  top:25%;
  left:25%;
  border-radius:50%;


}
.Cicrle__content:hover{
  background-color:rgba(10, 218, 217,0.3);
}

.Cicrle__right {
  width: 250px;
  height: 250px;
  right: 63%;
  bottom:30%;
  position: absolute;
  background:url(../assets/ok.png);
  background-size:cover;
  animation: Cicrle 1s infinite  steps(23)
}
.Cicrle__left {
  width: 250px;
  height: 250px;
  position: absolute;
  right: 3%;
  bottom:30%;
  background:url(../assets/ok02.png);
  background-size:cover;
  animation: Cicrle 1s infinite  steps(23)
}
.Circuit__gear{
  position: absolute;
  bottom: -20%;
  left:23%;
  animation:gear 10s linear infinite;
  animation-direction:normal;
}
.Circle--paused{
  animation-play-state:paused;
}
.Circuit {
  width: 230px;
  height: 363px;
  position:absolute;
  bottom: 0;
  left:34%;
  animation: Circuit 1s infinite;
  animation-direction:alternate;
}



@keyframes Cicrle{
  from{
    background-position:0 0;
  }
  to{
    background-position:-5750px 0;
  }
}
@keyframes Circuit{
  from{
    background:url(../assets/chi.png);
  }
  to{
    background:url(../assets/chi_light.png);
  }
}
@keyframes gear{
  from {
    transform: rotateZ(0);
  }
  to {
    transform: rotateZ(360deg);
  }
}
</style>
