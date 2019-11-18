<template>
    <b-container fluid id="content-section">
        <b-row>
            <Personal />
        </b-row>
    </b-container>
</template>

<script>
import Personal from '@/components/Personal.vue';

export default {
    name:"content-section",
    components:{
        Personal,
    }    
}
</script>

<style scoped>
/*
    #content-section {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        background-color:#6A5555;
    }
    #work-area {
        background-color: white;
        height: 80vh;
        width: 100vh;
    }
    */
</style>