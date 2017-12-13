<template>
  <div style="margin-top:-60px;">
    <header>
      <flexbox :gutter="0" class="part1">
        <flexbox-item :span="2"><p class="title">菜场</p></flexbox-item>
        <flexbox-item :span="10">
          <div class="search">
            <i slot="icon" class="fa fa-search" aria-hidden="true"></i>
            <input type="text" placeholder="搜索任何食材、辅料、调料" style="width:200px;"/>
          </div>
        </flexbox-item>
      </flexbox>
      <nav>
        <ul>
          <li class="current">蔬菜</li>
          <li>水果</li>
          <li>肉类</li>
          <li>水产</li>
          <li>禽蛋</li>
          <li>豆制</li>
          <li>五谷</li>
        </ul>
      </nav>
    </header>
    <div style="clear: both; height: 0px;"></div>
    <div class="main">
      <group-title class="goodsType">叶菜类</group-title>
      <grid :cols="3">
        <grid-item class="goodsItem" v-for="i in 6" :key="i">
          <img src="http://img.dev.moredian.com:8000/temporary/2017/12/13/13/92d99e9883a8431296b2f80be76c5bb0.jpg">
          <br/>
          <p>苹果</p>
          <p>4.5元/斤</p>
        </grid-item>
      </grid>
      <group-title class="goodsType">根菜类</group-title>
      <grid :cols="3">
        <grid-item class="goodsItem" v-for="i in 6" :key="i">
          <img src="http://img.dev.moredian.com:8000/temporary/2017/12/13/13/92d99e9883a8431296b2f80be76c5bb0.jpg">
          <br/>
          <p>苹果</p>
          <p>4.5元/斤</p>
        </grid-item>
      </grid>
      <group-title class="goodsType">根菜类</group-title>
      <grid :cols="3">
        <grid-item class="goodsItem" v-for="i in 6" :key="i">
          <img src="http://img.dev.moredian.com:8000/temporary/2017/12/13/13/92d99e9883a8431296b2f80be76c5bb0.jpg">
          <br/>
          <p>苹果</p>
          <p>4.5元/斤</p>
        </grid-item>
      </grid>
    </div>
    <tabbar class="tabbar">
      <tabbar-item>
        <i slot="icon" class="fa fa-compass" aria-hidden="true"></i>
        <span slot="label">发现</span>
      </tabbar-item>
      <tabbar-item>
        <i slot="icon" class="fa fa-book" aria-hidden="true"></i>
        <span slot="label">菜谱</span>
      </tabbar-item>
      <tabbar-item selected link="/component/demo">
        <i slot="icon" class="fa fa-leaf" aria-hidden="true"></i>
        <span slot="label">菜场</span>
      </tabbar-item>
      <tabbar-item badge="2">
        <i slot="icon" class="fa fa-shopping-basket" aria-hidden="true"></i>
        <span slot="label">菜篮</span>
      </tabbar-item>
      <tabbar-item>
        <i slot="icon" class="fa fa-user" aria-hidden="true"></i>
        <span slot="label">我的</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
import { Tabbar, TabbarItem, XHeader, Flexbox, FlexboxItem, Search, Grid, GridItem } from 'vux'

export default {
  components: {
    Tabbar,
    TabbarItem,
    XHeader,
    Search,
    Flexbox,
    FlexboxItem,
    Grid,
    GridItem
  }
}
</script>

<style scoped lang="less">
@import '~vux/src/styles/1px.less';

* {
  font-size: 12px;
}
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  .part1 {
    height: 40px;
    background-color: #08BB07;
  .title {
    height: 40px;
    text-align: center;
    line-height: 40px;
    color: #FFF;
    font-weight: bold;
    font-size: 14px;
  }
  .search {
    float:left;
    padding-right:10px;
    margin: 5px 5px;
    border-radius: 5px;
    height: 30px;
    background-color: #FFF;
    i {
      float: left;
      padding:9px 8px;
    }
    input {
      border-width: 0px;
      height: 30px;
      padding-right: 10px;
      float: left;
    }
  }
  }
}

nav {
  background-color: #DADADA;
  overflow: hidden;
  ul {
    list-style: none;
    li {
      float: left;
      width:50px;
      height: 40px;
      line-height: 40px;
    }
    li.current {
      color: green;
    }
  }
}

.main {
  position: relative; 
  margin-top:80px; 
  z-index: -1;
}
.goodsType {
  display: block;
  padding-left: 20px;
  text-align: left;
  line-height: 50px;
  color: #08BB07;
}
.goodsItem {
  padding: 8px;
  img {
    height: 90px;
    margin-bottom: 5px;
  }
  p {
    color: #666666;
  }
}
.tabbar {
  position: fixed;
}
</style>
