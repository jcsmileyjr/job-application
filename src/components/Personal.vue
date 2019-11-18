<template>
    <section>
        <div fluid id="personal">
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Full Name</label></b-col>
                <b-col><input type="text" v-model="personalData.fullName" /></b-col>
                <b-col><label class="example-label">Ex. John Smith</label></b-col>
            </b-form-row>
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Home Address</label></b-col>
                <b-col><input type="text" v-model="personalData.homeAddress" /></b-col>
                <b-col><label class="example-label">Ex. Future Developer Ave.</label></b-col>
            </b-form-row>
            <b-form-row class="input-form">
                <b-col><label class="bold-label">City</label></b-col>
                <b-col><input type="text" v-model="personalData.homeCity" /></b-col>
                <b-col><label class="example-label">Ex. Code City</label></b-col>
            </b-form-row>        
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Zip Code</label></b-col>
                <b-col><input type="text" v-model="personalData.homeZipCode" /></b-col>
                <b-col><label class="example-label">Ex. 10101</label></b-col>
            </b-form-row>       
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Phone Number</label></b-col>
                <b-col><input type="text" v-model="personalData.homeNumber" /></b-col>
                <b-col><label class="example-label">Ex. 111-222-3333</label></b-col>
            </b-form-row>  
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Email</label></b-col>
                <b-col><input type="text" v-model="personalData.homeEmail" /></b-col>
                <b-col><label class="example-label smallEmail">best@hero.com</label></b-col>
            </b-form-row> 
            <b-form-row class="input-form">
                <b-col><label class="bold-label">College Degree</label></b-col>
                <b-col><input type="text" v-model="personalData.homeDegree" /></b-col>
                <b-col><label class="example-label">Ex. Computer Science</label></b-col>
            </b-form-row> 
            <div class="centerButton">
                <b-button variant="success" type="submit" size="sm" @click="updateState">Continue</b-button>
            </div>                   
        </div>
    </section>
</template>

<script>
export default {
    name: "personal",
    data(){
        return {
            personalData:{
                fullName:"",
                homeAddress:"",
                homeCity:"",
                homeZipCode: "",
                homeNumber: "",
                homeEmail:"",
                homeDegree:"",
            }
        }
    },
    methods:{
        updateState(){
            this.$emit("update:personal-info", this.personalData);
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

    #personal {
        background-color: white;
        padding: 2rem;
        margin-bottom: 1rem;
    }

    @media only screen and (max-width: 500px) {
        .smallEmail {
            font-size: .8rem;
        }
    }
</style>