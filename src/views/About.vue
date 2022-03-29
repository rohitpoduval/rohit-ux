<template>
  <div class="main">
    
    <el-row :gutter=20>

      <el-col :span="10"> 
        <div class="profile">
         
          <h1>Hello! My Name is</h1> <div class="name">Rohit Poduval</div>
          <h2>I work as a Product Manager at HotelKey, Inc</h2>

          <div class="social">
            <ul>
              <li><a href="https://www.linkedin.com/in/rohit-poduval"><img alt="linkedIN logo" src="../assets/2.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
              <li><a href="https://www.behance.net/rohitpoduval21"><img alt="behance logo" src="../assets/3.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
              <li><a href="https://www.instagram.com/rohit.poduval/"><img alt="instagram logo" src="../assets/1.jpg" style="height:36px; width:36px; border-radius: 80px;"></a></li>
            </ul>
          </div>

          <div class="download">
            <a target="_blank" style="text-decoration: none" href="https://drive.google.com/file/d/1wKq1BD9EpznCBo-T1BSARQNi1ylLdTNu/view?usp=sharing"><el-button type="primary" plain>Download CV</el-button></a>
          </div>


          


        </div> 
      </el-col>

      <el-col :span="13">
        <div class="resume">
          <el-tabs v-model="activeName" class="demo-tabs" @tab-click="handleClick">
            <el-tab-pane label="Work Experience" name="first"> <Work/> </el-tab-pane>
            <el-tab-pane label="Skills" name="second"><Skills/></el-tab-pane>
          </el-tabs>
        </div>
      </el-col>  
      
      
    </el-row>

   
    


   

  </div>
</template>

<script>
import Work from './Work.vue'
import Skills from './Skills.vue'

export default {
  name: 'HelloWorld',
  components: { Work, Skills },
  props: {
    msg: String
  },

  data(){
    return{
      activeName: 'first'
    }
  }

}
</script>

<style scoped>

body{
  margin: 0%;
  padding: 0%;
}

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

.name{
  color: #42b983;
  font-size: 2em;
  font-weight: bold;
  display: block;
}

.main{
  display: block;
}

@media only screen and (max-width: 600px) {
  .el-row{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-content: center;
    align-items: stretch;
  }
  .profile{
    margin: 20px;
  }
  .resume{
    margin: 20px;
  }

  .el-col-13{
    max-width: 100%;
  }
  .el-col-10{
    max-width: 100%;
  }
}  

</style>
