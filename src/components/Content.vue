<template>
    <section id="content-section">
        <div id="work-area">
            <InputForm title="Full Name"  example="John Smith" />
        </div>
    </section>
</template>

<script>
import InputForm from '@/components/Input-Form.vue';

export default {
    name:"content-section",
    components:{
        InputForm,
    }    
}
</script>

<style scoped>

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
</style>