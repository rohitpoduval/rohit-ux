<template>
<div class="block">
      
      <el-date-picker type="date" v-model="check_in_date" format="DD MMM, YYYY" value-format="YYYY-MM-DD" placeholder="Select a Date"></el-date-picker>
      <el-date-picker type="date" v-model="check_out_date" format="DD MMM, YYYY" value-format="YYYY-MM-DD" placeholder="Select a Date"></el-date-picker>
      <el-button type = "primary" size="large" @click="getRates()">Check Availability</el-button> 

       

   

    

    </div>
</template>

<script>
import axios from 'axios'




export default {
    name: 'Search',

    data(){
        return{
            check_in_date: '',
            check_out_date: '',
            rates: ''
        }
    },

    methods:  {
        getRates(){
            axios.get('https://00.us-east-1.hkdev0.hotelkeyapp.com/hk-crs/properties/0f3788b1-5759-4b45-8939-77a975f940ce/mini-rates-with-availability/v3',
            {
                params: {
                check_in_date : this.check_in_date,
                check_out_date: this.check_out_date
                }
            })
            .then(res => {
            let data = res.data.rate_details
            this.rates = data
            })
            
        }
    }

}
</script>



<style scoped>


</style>
