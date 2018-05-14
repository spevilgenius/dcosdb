<script>
  import Navbar from './Navbar.vue'

  export default {
    name: "app",

    components: {
      Navbar
    }
  }
</script>

<template>
    <el-container>
        <el-aside width="200px">Aside</el-aside>
        <el-container>
            <el-header><navbar></navbar></el-header>
            <el-main><router-view></router-view></el-main>
            <el-footer>Footer</el-footer>
        </el-container>
    </el-container>
</template>