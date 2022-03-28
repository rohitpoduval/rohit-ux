<template>
  <div class="main">
    <div class="profile-logo">
      <img alt="Vue logo" src="../assets/logo.jpg" style="height:128px; width:128px; border-radius: 80px;">
    </div>  
    <h1>Hello! My Name is Rohit Poduval</h1>
    <h2>I work as a UX Designer at HotelKey, Inc</h2>
    
    <div class="social">
      <ul>
        <li>LinkedIn</li>
        <li>Github</li>
        <li>Facebook</li>
        <li>Instagram</li>
      </ul>

      <div class="resume">
        <el-tabs v-model="activeName" class="demo-tabs" @tab-click="handleClick">
          <el-tab-pane label="Work Experience" name="first"> <Work/> </el-tab-pane>
          <el-tab-pane label="Skills" name="second">Skills</el-tab-pane>
          <el-tab-pane label="Contact" name="third">Contact</el-tab-pane>
        </el-tabs>
      </div>

    </div>

   

  </div>
</template>

<script>
import Work from './Work.vue'

export default {
  name: 'HelloWorld',
  components: { Work },
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}



ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
