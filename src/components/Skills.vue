<template>
    <section>
        <div id="skills">
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Front-End Skill</label></b-col>
                <b-col><input type="text" v-model="skillsData.feSkills" /></b-col>
                <b-col><label class="example-label">Vue</label></b-col>
            </b-form-row>    
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Back-End Skills</label></b-col>
                <b-col><input type="text" v-model="skillsData.beSkills" /></b-col>
                <b-col><label class="example-label">.Net</label></b-col>
            </b-form-row>
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Database Skill</label></b-col>
                <b-col><input type="text" v-model="skillsData.dbSkills" /></b-col>
                <b-col><label class="example-label">MongoDB</label></b-col>
            </b-form-row>    
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Dev-Ops Skill</label></b-col>
                <b-col><input type="text" v-model="skillsData.doSkills" /></b-col>
                <b-col><label class="example-label">Microsoft Google Platform</label></b-col>
            </b-form-row>                           
            <div class="centerButton">
                <b-button variant="success" type="submit" size="sm" @click="updateState">Continue</b-button>
            </div>              
        </div>
    </section>
</template>

<script>
export default {
    name:"skills",
    data(){
        return{
            skillsData:{
                feSkills:"",
                beSkills:"",
                dbSkills:"",
                doSkills:"",
            }
        }
    },
    methods:{
        updateState(){
            this.$emit("update:skills-info", this.skillsData);
        }
    }
}
</script>

<style>
    .centerButton {
        text-align: center;
    }

    input {
        box-shadow: 4px 4px 8px grey;
        border: 1px solid grey;
    }

    .input-form {
        margin-bottom: .5rem;
    }

    .bold-label {
        font-weight:bold;
    }

    .example-label {
        color: grey;
    }

    #skills {
        background-color: white;
        padding: 1rem;
        margin-bottom: 1rem;
    }

    @media only screen and (max-width: 500px) {
        .smallEmail {
            font-size: .8rem;
        }
    }
</style>