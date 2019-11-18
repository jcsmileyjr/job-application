<template>
    <b-container fluid class="justify-content-md-center" id="personal">
        <b-form-row>
            <b-col><label>Full Name</label></b-col>
            <b-col><input type="text" v-model="fullName" /></b-col>
            <b-col><label>Ex. John Smith</label></b-col>
        </b-form-row>
        <b-form-row>
            <b-col><label>Home Address</label></b-col>
            <b-col><input type="text" v-model="homeAddress" /></b-col>
            <b-col><label>Ex. Future Developer Ave.</label></b-col>
        </b-form-row>
        <b-form-row>
            <b-col><label>City</label></b-col>
            <b-col><input type="text" v-model="homeCity" /></b-col>
            <b-col><label>Ex. Code City</label></b-col>
        </b-form-row>        
        <b-form-row>
            <b-col><label>Zip Code</label></b-col>
            <b-col><input type="text" v-model="homeZipCode" /></b-col>
            <b-col><label>Ex. 10101</label></b-col>
        </b-form-row>       
        <b-form-row>
            <b-col><label>Phone Number</label></b-col>
            <b-col><input type="text" v-model="homeNumber" /></b-col>
            <b-col><label>Ex. 111-222-3333</label></b-col>
        </b-form-row>  
        <b-form-row>
            <b-col><label>Email</label></b-col>
            <b-col><input type="text" v-model="homeEmail" /></b-col>
            <b-col><label>Ex. best@hero.com</label></b-col>
        </b-form-row> 
        <b-form-row>
            <b-col><label>College Degree</label></b-col>
            <b-col><input type="text" v-model="homeDegree" /></b-col>
            <b-col><label>Ex. Computer Science</label></b-col>
        </b-form-row> 
        <b-form-row class="centerButton">
            <b-button variant="success" type="submit" size="sm">Continue</b-button>
        </b-form-row>                   
    </b-container>
</template>

<script>
export default {
    name: "personal",
    data(){
        return {
            fullName:"",
            homeAddress:"",
            homeCity:"",
            homeZipCode: "",
            homeNumber: "",
            homeEmail:"",
            homeDegree:"",
        }
    },
    methods:{
        updateState(){
            this.$emit("add:input-data", this.inputData);
        }
    }
}
</script>

<style>
    .centerButton {
        text-align: center;
    }
</style>