<template>
  <div>
    <group>
      <cell is-link title="Simple" link="/component/tabbar-simple"></cell>
      <cell is-link title="Switch icons" link="/component/tabbar-icon"></cell>
    </group>
    <tabbar>
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
import { Tabbar, TabbarItem, Group, Cell } from 'vux'

export default {
  components: {
    Tabbar,
    TabbarItem,
    Group,
    Cell
  }
}
</script>
