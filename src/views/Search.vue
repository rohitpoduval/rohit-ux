<template>
<div class="block">
      
      <el-date-picker v-model="daterange" valueType="format"></el-date-picker>
      {{date}}
    </div>
</template>

<script>

export default {
    name: 'Search',

    data(){
        return{
            date: '',
            check_in_date: '',
            check_out_date: ''
           
        }
    },


    methods: {
        checkRates(){
           
           
           console.log(this.date)

        }
    }
}
</script>



<style scoped>


</style>
