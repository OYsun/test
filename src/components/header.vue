<template>
  <div class="header">
    <div class="header__logo">
      <div class="header__login__bottom_1" ></div>
      <img src="../assets/logo.png" alt="logo" class="header__login__img" >
      <div class="header__login__bottom_2"></div>
    </div>
    <div class="header__nav">
      <div class="header__NavBox " :class="{'header__nav--BottomLine':!OriclOne}">
        <div class="header__oricl" v-show="OriclOne"></div>
        <div class="header__oricl--apha" v-show="OriclOne"></div>
        <a href="#" @click="OriclOneClick">首页</a>
      </div>
      <div class="header__NavBox " :class="{'header__nav--BottomLine':!OriclTwo}">
        <div class="header__oricl" v-show="OriclTwo"></div>
        <div class="header__oricl--apha" v-show="OriclTwo"></div>
        <a href="#" @click='OriclTwoClick'>自我评估</a>
      </div>
      <div class="header__NavBox" :class="{'header__nav--BottomLine':!OriclThree}">
        <div class="header__oricl" v-show="OriclThree"></div>
        <div class="header__oricl--apha" v-show="OriclThree"></div>
        <a href="#" @click='OriclThreeClick'>名校展示</a>
      </div>
    </div>
    <div class="header__Right">
      <div class="header__login"><a href="#">登入</a><span>&nbsp&nbsp\&nbsp&nbsp</span><a href="#">注册</a></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'header',
  data () {
    return {
      OriclOne: true,
      OriclTwo: false,
      OriclThree: false
    }
  },
  methods: {
    OriclOneClick () {
      this.OriclOne = true
      this.OriclTwo = false
      this.OriclThree = false
    },
    OriclTwoClick () {
      this.OriclOne = false
      this.OriclTwo = true
      this.OriclThree = false
    },
    OriclThreeClick () {
      this.OriclOne = false
      this.OriclTwo = false
      this.OriclThree = true
    }
  }

}
</script>

<style scoped>
a{
  display: block;
  color:white;
  text-align: center;
  line-height: 80px;
  text-decoration:none;
  font-size: 13px;
}
a:hover,a:active{
  color:rgb(177, 218, 217)
}
.header{
  height: 60px;
  width:100%;


}
.header__logo{
  width: 30%;
  height:100%;
  float: left;
  position: relative;

}
.header__login__img{
  position:absolute;
  width:35%;

}
.header__login__bottom_1{
  border-bottom:1px solid rgb(177, 218, 217);
  height:100%;
  width:20%;
  position: absolute;

}
.header__login__bottom_2{
  border-bottom:1px solid rgb(177, 218, 217);
  height:100%;
  width:45%;
  position: absolute;
  right: 0;
  overflow: hidden;
}
.header__logo img{

  left:20%;
  bottom:-20%;
}
.header__nav{
  width:35%;
  height: 60px;
  float: left;


}
.header__nav--BottomLine{
  border-bottom:1px solid rgb(177, 218, 217);

}
.header__NavBox{
  position: relative;
  width:33.33%;
  height:100%;
  float: left;

}
.header__oricl{
  position:absolute;
  z-index:-1;
  bottom:0;
  width:100%;
  height: 50px;
  border-top: 2px solid rgb(177, 218, 217);
  border-left: 2px solid rgb(177, 218, 217);
  border-right: 2px solid rgb(177, 218, 217);
  transform:  perspective(1em) rotateX(5deg);
  transform-origin: bottom;
}
.header__oricl--apha{
  position:absolute;
  bottom: 0;
  left:1.5%;
  z-index: -1;
  /*background-color: rgba(177, 218, 217,0.1);*/
  background: -webkit-linear-gradient(top,rgba(177, 218, 217,0.3),rgba(67, 142, 219, 0.1));
  transform:  perspective(1em) rotateX(5deg);
  width:100%;
  height: 50px;
  transform-origin: bottom;
}
.header__Right{
  width: 35%;
  height:100%;
  float: left;
  position: relative;
  border-bottom:1px solid rgb(177, 218, 217);
}
.header__login{
  position: absolute;
  right: 20%;
}
.header__login a{
  display: inline;

}
.header__login span{
  color: white;
  font-size: 1.5em;
  font-weight: lighter;
}
</style>
