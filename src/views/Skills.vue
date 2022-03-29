<template>
   
   <div class="work">
        <el-row>
            <el-col :span="24">
                <div class="header">Core Competencies</div>
                <div class="sub-header">Product Development Life Cycle, Customer Interviews, Roadmapping, Personas and Journey Maps


                </div>
            </el-col>
        </el-row>
   </div>
   
   <div class="work">
        <el-row>
            <el-col :span="24">     
                <div class="header">Analysis and Data Tools</div>
                <div class="sub-header">Google Analytics, MixPanel and Third Party Payment Integrations</div>
            </el-col>
        </el-row>
   </div>

    <div class="work">
        <el-row>
            <el-col :span="24">     
                <div class="header">Product and Creative Tools </div>
                <div class="sub-header">Adobe Suite, Figma, JIRA and Git Basics</div>
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
