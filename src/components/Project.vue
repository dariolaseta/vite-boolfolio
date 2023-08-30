<template>
    <div>
        
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: "Project",
    data(){
        return {
            projectUrl: "http://localhost:81/api/projects",
            projects: "",
        }
    },
    mounted(){
        axios.get(this.projectUrl)
        .then(response=>{
            this.projects = response.data.projects;
            console.log(this.projects);
        })
    }
}
</script>

<style lang="">
    
</style>