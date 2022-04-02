<template>
    <div>
       <el-input v-model="username" placeholder="Username" size="large" clearable />
       <el-input v-model="password" type="password" placeholder="Password"  size="large" clearable />
       <el-button type="primary" @click="login()">Login</el-button>
    </div>
</template>

<script>



export default {
    name: 'Login',

    data(){
        return{
            username: '',
            password: ''

        }
    },

    methods: {

    }
}
</script>



<style scoped>


</style>
