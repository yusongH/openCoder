<template>
  <a-layout id="components-layout-demo-custom-trigger">
    <a-layout-sider class="slider" :trigger="null" collapsible v-model="collapsed">
      <div class="logo">OpenCoder管理系统</div>
      <a-menu class="menu" theme="dark" mode="inline" :defaultSelectedKeys="['1']">
        <a-menu-item key="1">
          <span>首页</span>
        </a-menu-item>
        <a-menu-item key="2">
          <span>用户管理</span>
        </a-menu-item>
        <a-menu-item key="3">
          <span>博客管理</span>
        </a-menu-item>
        <a-menu-item key="4">
          <span>活动管理</span>
        </a-menu-item>
        <a-menu-item key="5">
          <span>可视化模版</span>
        </a-menu-item>
        <a-menu-item key="6">
          <span>博客管理</span>
        </a-menu-item>
        <a-menu-item key="7">
          <span>图片库</span>
        </a-menu-item>
        <a-menu-item key="8">
          <span>资料管理</span>
        </a-menu-item>
        <a-menu-item key="9">
          <span>友情链接</span>
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout>
      <a-layout-header class="header">
        <a-icon
          class="trigger"
          :type="collapsed ? 'menu-unfold' : 'menu-fold'"
          @click="()=> collapsed = !collapsed"
        />
      </a-layout-header>
      <a-layout-content
        class="content"
        :style="{ margin: '24px 16px', padding: '24px', background: '#fff', minHeight: '280px' }"
      >Content</a-layout-content>
    </a-layout>
  </a-layout>
</template>

<script>
export default {
  name: "index",
  data() {
    return {
      collapsed: false
    };
  }
};
</script>

<style lang="less">
#components-layout-demo-custom-trigger .header {
  background-color: #0E2E5A;
}

#components-layout-demo-custom-trigger .trigger {
  font-size: 14px;
  line-height: 35px;
  padding: 0 24px;
  cursor: pointer;
  transition: color 0.3s;
}

#components-layout-demo-custom-trigger .trigger:hover {
  color: #061a36;
}

#components-layout-demo-custom-trigger .logo {
  font-size: 14px;
  color: #fff;
  height: 32px;
  // background: rgba(255, 255, 255, 0.2);
  margin: 16px;
}
</style>
