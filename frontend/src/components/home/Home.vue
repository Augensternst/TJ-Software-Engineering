<script setup lang="ts">
import {
  ElHeader,
  ElMain,
  ElContainer,
  ElAside,
  ElAvatar,
  ElDropdown,
  ElDropdownMenu,
  ElDropdownItem,
  ElRow,
  ElAffix,
  ElCol
} from 'element-plus';
import Menu from '../menu/Menu.vue'
import { useRouter } from 'vue-router'
import {useStore} from "vuex";

const store = useStore();
const router = useRouter()
const logout = () => {
  store.dispatch("logout")
  location.reload()
}
const goToPersonalCenter = () => {
  router.push('/personalCenter')
}
</script>
<template>
  <div class="common-layout" style="position: absolute;top: 0;left: 0;right: 0;bottom: 0;">
    <el-container style="height: 100vh;">
      <el-header height="">
        <el-affix :offset="0">
          <div class="system-header" style="text-align: left;">
            <el-row :gutter="24">
              <el-col :span="15">
                <div class="grid-content ep-bg-purple">表达小达人</div>
              </el-col>
              <el-col :span="1" :offset="8">
                <div class="grid-content ep-bg-purple-light">
                  <el-dropdown class="header-dropdown">
                    <span class="el-dropdown-link component" >
                        <el-avatar :src=$store.state.user.avatar></el-avatar>
                    </span>
                    <template #dropdown>
                      <el-dropdown-menu>
                        <el-dropdown-item @click="goToPersonalCenter">个人中心</el-dropdown-item>
                        <el-dropdown-item @click="logout">用户登出</el-dropdown-item>
                      </el-dropdown-menu>
                    </template>
                  </el-dropdown>
                </div>
              </el-col>
            </el-row>
          </div>
        </el-affix>
      </el-header>
      <el-container>
        <el-aside width="200px">
          <el-affix :offset="103">
            <Menu></Menu>
          </el-affix>
        </el-aside>
        <el-container>
          <el-main>
            <router-view/>
          </el-main>
        </el-container>
      </el-container>
    </el-container>
  </div>
</template>

<style>
/* 头部样式 */
.el-header {
  height: 100px;
}

.system-header {
  background: linear-gradient(45deg, #00b0e8, #3b5998, #8b9dc3);
  color: white;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
  border-radius: 10px;
  font-size: 36px;
  font-weight: bold;
  letter-spacing: 1px;
  height: 60px;
  margin-left: -22px;
  margin-right: -22px;
  padding: 20px;
}

/* 侧边栏样式 */
.el-aside {
  background: linear-gradient(to right, #85D8CE, #6FA8DC);
  color: white;
  box-shadow: 4px 0 20px rgba(0, 0, 0, 0.2);
}

/* 彩虹渐变文字效果 */
.el-aside h2 {
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
  background-image: linear-gradient(45deg, #ff00a9, #00eaff);
}

.el-header h1 {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  /* 根据项目需要选择字体 */
  font-size: 36px;
  font-weight: bold;
  letter-spacing: 1px;
  line-height: 1.5;
  /* 行高 */
  margin: 0;
  /* 去掉默认的外边距 */
}

/* 彩虹渐变边框效果 */
.el-header,
.el-aside {
  border: 2px solid transparent;
  background-clip: padding-box;
  -webkit-background-clip: padding-box;
  transition: border-color 0.3s ease;
}

.el-header:hover,
.el-aside:hover {
  border-color: #f39c12;
}


.el-main {
  background: rgb(151, 218, 247);
}

.el-footer {
  /*background: yellow;*/
}
.component:focus {
  /* 取消选中特效，可以根据需要修改样式 */
  outline: none;
}
</style>
