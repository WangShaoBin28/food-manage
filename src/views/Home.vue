<template>
  <el-container>
    <!--头部-->
    <el-header>
      <div class="logo">
        Yin-music 后台管理
      </div>
      <div class="header-right">
        <div class="header-user-con">
          <!-- 用户头像 -->
          <div class="user-avator">
            <img src="../assets/logo.png" />
          </div>
          <!-- 用户名下拉菜单 -->
          <el-dropdown class="user-name" >
          <span class="el-dropdown-link">
            123
            <i class="el-icon-caret-bottom"></i>
          </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item command="loginout">修改密码</el-dropdown-item>
              <el-dropdown-item command="loginout">退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
      </div>
    </el-header>
    <!--左侧菜单-->
    <el-container>
      <el-aside width="201px">
        <el-menu
            default-active="/Info"
            class="el-menu-vertical-demo"
            background-color="#545c64"
            text-color="#fff"
            active-text-color="#ffd04b"
            router >

          <el-menu-item index="/Info">
            <i class="el-icon-s-home"></i>
            <span slot="title">系统首页</span>
          </el-menu-item>

          <el-menu-item index="/Info2">
            <i class="el-icon-s-order"></i>
            <span slot="title">订单管理</span>
          </el-menu-item>

          <el-submenu index="1">
            <template slot="title">
              <i class="el-icon-location"></i>
              <span>门店管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="1-1">菜品管理</el-menu-item>
              <el-menu-item index="1-1">菜品分类</el-menu-item>
              <el-menu-item index="1-1">菜品标签</el-menu-item>
              <el-menu-item index="1-2">餐桌管理</el-menu-item>
            </el-menu-item-group>
          </el-submenu>

          <el-submenu index="2">
            <template slot="title">
              <i class="el-icon-setting"></i>
              <span>系统管理</span>
            </template>
            <el-menu-item-group>
              <el-menu-item index="1-1">用户管理</el-menu-item>
              <el-menu-item index="1-2">权限管理</el-menu-item>
            </el-menu-item-group>
          </el-submenu>

        </el-menu>
      </el-aside>
      <!-- 主体     -->
      <el-main>
        <router-view/>
      </el-main>
    </el-container>
  </el-container>
</template>

<script>

export default {
  name: 'Home',
  components: {}
}
</script>
<style scoped lang="scss">
.el-header {

  background-color: #545c64;
  color: #333;
  text-align: center;
  line-height: 60px;
  display: flex;
  justify-content: space-between;
}

.el-aside {
  color: #333;
  text-align: center;
  line-height: 200px;
}
.el-menu{
  height: 100%;
}
.el-main {
  background-color: #E9EEF3;
  color: #333;
  text-align: center;
  line-height: 160px;
}
.header-right {
  float: right;
  padding-right: 50px;
}
.header-user-con {
  display: flex;
  height: 70px;
  align-items: center;
}
.user-name {
  margin-left: 10px;
}
.user-avator {
  margin-left: 20px;
}
.user-avator img {
  display: block;
  width: 40px;
  height: 40px;
  border-radius: 50%;
}
.el-dropdown-link {
  color: #B0B3B2;
  cursor: pointer;
}
.el-dropdown-menu__item {
  text-align: center;
}
.el-container {
  height: 100%;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>
