<template>
  <div class="about">
    <h1>This is an about page</h1>
    <van-tabbar route>
      <van-tabbar-item 
        replace
        to="/home"
        icon="home-o">
        标签
      </van-tabbar-item>
      <van-tabbar-item 
        replace
        to="/about"
        icon="home-o"
      >
        关于
      </van-tabbar-item>
    </van-tabbar>
  </div>
</template>
