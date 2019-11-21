<template>
    <section>
        <div id="work">
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Company Name</label></b-col>
                <b-col><input type="text" v-model="workData.jobName" /></b-col>
                <b-col><label class="example-label">Coders Delight</label></b-col>
            </b-form-row>    
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Company Address</label></b-col>
                <b-col><input type="text" v-model="workData.jobAddress" /></b-col>
                <b-col><label class="example-label">Coders Bay</label></b-col>
            </b-form-row>
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Company City</label></b-col>
                <b-col><input type="text" v-model="workData.jobCity" /></b-col>
                <b-col><label class="example-label">Coders</label></b-col>
            </b-form-row>    
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Company Zip Code</label></b-col>
                <b-col><input type="text" v-model="workData.jobZipCode" /></b-col>
                <b-col><label class="example-label">01010</label></b-col>
            </b-form-row>              
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Job Title</label></b-col>
                <b-col><input type="text" v-model="workData.jobTitle" /></b-col>
                <b-col><label class="example-label">Developer</label></b-col>
            </b-form-row> 
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Job Description</label></b-col>
                <b-col><input type="text" v-model="workData.jobDescr" /></b-col>
                <b-col><label class="example-label">Build the Front End</label></b-col>
            </b-form-row>    
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Job Pay</label></b-col>
                <b-col><input type="text" v-model="workData.jobPay" /></b-col>
                <b-col><label class="example-label">$75,000 yr</label></b-col>
            </b-form-row>                          
            <div class="centerButton">
                <b-button variant="success" type="submit" size="sm" @click="updateState">Continue</b-button>
            </div>              
        </div>
    </section>
</template>

<script>
export default {
    data(){
        return{
            workData:{
                jobName:"",
                jobAddress:"",
                jobCity:"",
                jobZipCode:"",
                jobTitle:"",
                jobDescr:"",
                jobPay:"",
            }
        }
    },
    name: "work",
    methods:{
        updateState(){
            this.$emit("update:work-info", this.workData);
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

    #work {
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