<template>
   
   <div class="work">
        <el-row>
            <el-col :span="24">
                <div class="header">Product Manager/UX Designer</div>
                <div class="sub-header">Mar 2018 - Present</div>
            </el-col>
        </el-row>
   </div>
   
   <div class="work">
        <el-row>
            <el-col :span="24">     
                <div class="header">Quality Assurance</div>
                <div class="sub-header">Oct 2017 - Mar 2018</div>
            </el-col>
        </el-row>
   </div>

    <div class="work">
        <el-row>
            <el-col :span="24">     
                <div class="header">Implementation Consultant</div>
                <div class="sub-header">Nov 2016 - Oct 2017</div>
            </el-col>
        </el-row>
    </div>

</template>

<script>

export default {
    name: 'Work'
}
</script>

<style scoped>


.header{
    font-size: 16px;
    font-weight: bold;
}


.sub-header{
    font-size: 14px;
}

.el-row{
    text-align: left;
}

.work{
    border: 1px solid #eaeaea;
    border-radius: 5px;
    padding: 20px;
    margin-bottom: 15px;

}
</style>
