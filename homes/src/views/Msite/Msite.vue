<template>
   <section class="msite">
        <!--首页头部-->
        <header class="msite_header">
          <span class="header_search">
            <i class="iconfont icon-sousuo"></i>
          </span>
          <span class="header_title">
            <span class="header_title_text ellipsis">昌平区北七家宏福科技园(337省道北)</span>
          </span>
          <span class="header_login">
            <span class="header_login_text">登录|注册</span>
          </span>
        </header>
        <!--首页导航-->
       <div class="msite-content-wrapper">
         <div class="msite-content">
           <nav class="msite_nav">
             <ul class="type">
               <router-link tag='li' :to="'/list'+item.id" v-for="item in types" :key="item.id" >
                  <img :src="'/static/images'+item.img" alt="">
                  <p>{{item.text}}</p>
               </router-link>
             </ul>
           </nav>
         </div>
       </div>
      </section>
</template>
<style lang="scss" scoped>
.msite{
  background-color: #f6fff1;
  .msite_nav{
    .type{
      display: flex;
      background-color: #fff;
      padding: 15px 0px 5px;
      flex-wrap: wrap;
      li{
        width: 20%;
        text-align: center;
        img{
          width: 60%
        }
        p{
          font-size: 14px;
          padding: 4px 0 15px;
        }
      }
    }
  }
}
</style>
<script>
export default {
 data() {
   return {
    // 轮播图为首屏加载 
    types : [
      {id:1,img:'/nav/1.jpg',text:'甜品饮品'},
      {id:2,img:'/nav/2.jpg',text:'商超便利'},
      {id:3,img:'/nav/3.jpg',text:'美食'},
      {id:4,img:'/nav/4.jpg',text:'简餐'},
      {id:5,img:'/nav/5.jpg',text:'新店特惠'},
      {id:6,img:'/nav/6.jpg',text:'准时达'},
      {id:7,img:'/nav/7.jpg',text:'预定早餐'},
      {id:8,img:'/nav/8.jpg',text:'土豪推荐'},
      {id:9,img:'/nav/9.jpg',text:'甜品饮品'},
      {id:10,img:'/nav/10.jpg',text:'商超便利'},
    ]
   }
 }
}
</script>
