<template>
    <div id="results">        
        <section>     
            <h3>Personal Information</h3>       
            <b-row><label>{{personal.fullName}}</label></b-row>
            <b-row><label>{{personal.homeAddress}}</label></b-row>
            <b-row><label>{{personal.homeCity}}</label></b-row>
            <b-row><label>{{personal.homeZipCode}}</label></b-row>
            <b-row><label>{{personal.homeNumber}}</label></b-row>
            <b-row><label>{{personal.homeEmail}}</label></b-row>
            <b-row><label>{{personal.homeDegree}}</label></b-row>                                    
        </section>
        <section>     
            <h3>Work History</h3>       
            <b-row><label>{{work.jobName}}</label></b-row>
            <b-row><label>{{work.jobAddress}}</label></b-row>
            <b-row><label>{{work.jobCity}}</label></b-row>
            <b-row><label>{{work.jobZipCode}}</label></b-row>
            <b-row><label>{{work.jobTitle}}</label></b-row>
            <b-row><label>{{work.jobDescr}}</label></b-row>
            <b-row><label>{{work.jobPay}}</label></b-row>                                    
        </section>
        <section>     
            <h3>Professional Skills</h3>       
            <b-row><label>{{skills.feSkills}}</label></b-row>
            <b-row><label>{{skills.beSkills}}</label></b-row>
            <b-row><label>{{skills.dbSkills}}</label></b-row>
            <b-row><label>{{skills.doSkills}}}</label></b-row>                                    
        </section>                  
    </div>
</template>

<script>
export default {
    name:"results",
    props:{
        personal:{},
        work: {},
        skills:{},
    }
}
</script>

<style>

    #results {
        background-color: white;
        padding: 2rem;
        margin-bottom: 1rem;
    }
</style>