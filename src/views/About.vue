<template>
  <div class="main">
    <div class="profile-logo">
      <img alt="Vue logo" src="../assets/logo.jpg" style="height:100px; width:100px; border-radius: 80px;">
    </div>  
    <h1>Hello! My Name is Rohit Poduval</h1>
    <h2>I work as a UX Designer at HotelKey, Inc</h2>
    
    <div class="social">
      <ul>
        <li><a href="https://www.instagram.com/rohit.poduval/"><img alt="Vue logo" src="../assets/1.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
        <li><a href="https://www.linkedin.com/in/rohit-poduval"><img alt="Vue logo" src="../assets/2.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
        <li><a href="https://www.behance.net/rohitpoduval21"><img alt="Vue logo" src="../assets/3.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
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
