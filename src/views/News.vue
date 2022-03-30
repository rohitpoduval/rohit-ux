<template>
    <div>
        <el-row :gutter="20" style="margin:0 30px 0 30px">
            <el-col
                v-for=" item in news"
                :key="item.title"
                :span="8"
                
            >
                <el-card :body-style="{ padding: '0px' }">
                    <img :src="item.imageUrl" class="image"/>
                    <div class="title">
                        <span>{{ item.author }}</span>
                        <div class="bottom">
                            <time class="time">{{ item.date }}</time>
                            <el-button type="primary" size="large" class="button">View on Behance</el-button>
                        </div>
                    </div>
                </el-card>
            </el-col>
        </el-row>
    </div>
</template>

<script>

import axios from 'axios'

export default {
    name: 'News',

    data(){
      return{
        loading: false,
        news:''
        }
    },
      
    mounted() {
        this.loading = true; 
        axios.get('https://inshortsapi.vercel.app/news?category=science')
        .then((resp) => {
        this.news = resp.data.data;
        this.loading = false; 
        })
    },
}

</script>

<style scoped>

@media only screen and (max-width: 600px) {
    .el-row{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    align-content: center;
    align-items: stretch;
    }
}

.title{
    padding: 14px;
    text-align: left;
}

.image{
    height: 250px;
    width: 459px;
    padding: 0px;
    margin: 0px;
}

.time {
  font-size: 13px;
  color: #999;
}

.bottom {
  margin-top: 13px;
  line-height: 12px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.button {
  padding: 10;
  min-height: auto;
}

.image {
  width: 100%;
  display: block;
}

.el-card {
    margin-bottom: 20px;
}

</style>