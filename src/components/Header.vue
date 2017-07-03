<template>
  <navbar>
    <button class="navbar-toggler mobile-sidebar-toggler d-lg-none" type="button" @click="mobileSidebarToggle">&#9776;</button>
    <a class="navbar-brand" href="#"></a>
    <ul class="nav navbar-nav d-md-down-none">
      <li class="nav-item">
        <a class="nav-link navbar-toggler sidebar-toggler" href="#" @click="sidebarMinimize">&#9776;</a>
      </li>
      <li class="nav-item px-3">
        <!--<a class="nav-link" href="#">舆情监测</a>-->
        <router-link :to="'/dashboard'" class="nav-link" exact>舆情监测</router-link>
      </li>
      <li class="nav-item px-3">
        <!--<a class="nav-link" href="#">行业指数</a>-->
        <router-link :to="'/dashboard'" class="nav-link" exact>行业指数</router-link>
      </li>
      <li class="nav-item px-3">
        <!--<a class="nav-link" href="#">研究报告</a>-->
        <router-link :to="'/dashboard'" class="nav-link" exact>研究报告</router-link>
      </li>
      <li class="nav-item px-3">
        <!--<a class="nav-link" href="#">配置</a>-->
        <router-link :to="'/dashboard'" class="nav-link" exact>配置</router-link>
      </li>
    </ul>
    <ul class="nav navbar-nav ml-auto">
      <li class="nav-item d-md-down-none">
        <a class="nav-link" href="#">全屏</a>
      </li>
      <li class="nav-item d-md-down-none">
        <a class="nav-link" href="#">锁屏</a>
      </li>
      <li class="nav-item d-md-down-none">
        <a class="nav-link" href="#">清除缓存</a>
      </li>
      <li class="nav-item d-md-down-none">
        <a class="nav-link" href="#">主题</a>
      </li>
      <dropdown size="nav" class="nav-item">
        <span slot="button">
          <img src="static/img/avatars/6.jpg" class="img-avatar" alt="admin@bootstrapmaster.com">
          <span class="d-md-down-none">admin</span>
        </span>
        <div slot="dropdown-menu"class="dropdown-menu dropdown-menu-right">
          <a class="dropdown-item" href="#"><i class="fa fa-bell-o"></i> 个人信息</a>
          <a class="dropdown-item" href="#"><i class="fa fa-envelope-o"></i> 修改密码</a>
          <a class="dropdown-item" href="#"><i class="fa fa-tasks"></i> 退出</a>
        </div>
      </dropdown>
      <li class="nav-item d-md-down-none">
        <a class="nav-link navbar-toggler aside-menu-toggler" href="#" @click="asideToggle">&#9776;</a>
      </li>
    </ul>
    <div class="navbar-hrbr"></div>
  </navbar>
</template>
<script>

import navbar from './Navbar'
import { dropdown } from 'vue-strap'

export default {
  name: 'header',
  components: {
    navbar,
    dropdown
  },
  methods: {
    click () {
      // do nothing
    },
    sidebarToggle (e) {
      e.preventDefault()
      document.body.classList.toggle('sidebar-hidden')
    },
    sidebarMinimize (e) {
      e.preventDefault()
      document.body.classList.toggle('sidebar-minimized')
    },
    mobileSidebarToggle (e) {
      e.preventDefault()
      document.body.classList.toggle('sidebar-mobile-show')
    },
    asideToggle (e) {
      e.preventDefault()
      document.body.classList.toggle('aside-menu-hidden')
    }
  }
}
</script>
