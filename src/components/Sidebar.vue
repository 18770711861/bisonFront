<template>
  <div class="sidebar">
    <nav class="sidebar-nav">
      <ul class="nav">
        <!--<li class="nav-item">
          <router-link :to="'/dashboard'" class="nav-link"><i class="icon-speedometer"></i> Dashboard <span class="badge badge-info">NEW</span></router-link>
        </li>-->
        <li class="nav-title">
          <router-link :to="'/dashboard'" class="nav-link" exact>首页</router-link>
        </li>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/components'}" disabled>
          <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="fa fa-globe"></i> 行业资讯</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/components/buttons'" class="nav-link" exact><i class="fa fa-globe"></i>监测方案</router-link>
            </li>
          </ul>
        </router-link>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/icons'}" disabled>
          <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="fa fa-university"></i> 企业信息</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/icons/font-awesome'" class="nav-link" exact><i class="fa fa-university"></i> Font Awesome</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="'/icons/simple-line-icons'" class="nav-link" exact><i class="fa fa-university"></i> Simple Line Icons</router-link>
            </li>
          </ul>
        </router-link>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/icons'}" disabled>
        <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="fa fa-cutlery"></i> 竞争对手</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/widgets'" class="nav-link" exact><i class="fa fa-cutlery"></i> 竞争对手 </router-link>
            </li>
          </ul>
        </router-link>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/icons'}" disabled>
        <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="fa fa-stethoscope"></i> 热点监测</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/charts'" class="nav-link" exact><i class="fa fa-stethoscope"></i> Charts</router-link>
            </li>
            </ul>
        </router-link>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/icons'}" disabled>
        <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="fa fa-mixcloud"></i> 舆情报告</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/charts'" class="nav-link" exact><i class="fa fa-mixcloud"></i> Charts</router-link>
            </li>
            </ul>
        </router-link>

        <router-link tag="li" class="nav-item nav-dropdown" :to="{ path: '/icons'}" disabled>
        <div class="nav-link nav-dropdown-toggle" @click="handleClick"><i class="icon-pie-chart"></i> 舆情监测</div>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/charts'" class="nav-link" exact><i class="icon-pie-chart"></i> Charts</router-link>
            </li>
            </ul>
        </router-link>

        <li class="divider"></li>
        <li class="nav-title">
          链接
        </li>
        <li class="nav-item nav-dropdown">
          <a class="nav-link nav-dropdown-toggle" href="#" @click="handleClick"><i class="icon-star"></i> Pages</a>
          <ul class="nav-dropdown-items">
            <li class="nav-item">
              <router-link :to="'/pages/login'" class="nav-link" exact><i class="icon-star"></i> Login</router-link>
            </li>
            <li class="nav-item">
                <router-link :to="'/pages/register'" class="nav-link" exact><i class="icon-star"></i> Register</router-link>
            </li>
            <li class="nav-item">
                <router-link :to="'/pages/404'" class="nav-link" exact><i class="icon-star"></i> Error 404</router-link>
            </li>
            <li class="nav-item">
              <router-link :to="'/pages/500'" class="nav-link" exact><i class="icon-star"></i> Error 500</router-link>
            </li>
          </ul>
        </li>
      </ul>
    </nav>
  </div>
</template>
<script>

export default {
  name: 'sidebar',
  methods: {
    handleClick (e) {
      e.preventDefault()
      e.target.parentElement.classList.toggle('open')
    }
  }
}
</script>

<style lang="css">
  .nav-link {
    cursor:pointer;
  }
</style>
