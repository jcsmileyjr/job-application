<template>
    <div id="results">        
        <section>     
            <h3>Personal Information</h3>       
            <b-row><label><span>Full Name:</span> {{personal.fullName}}</label></b-row>
            <b-row><label><span>Address:</span> {{personal.homeAddress}}</label></b-row>
            <b-row><label><span>City: </span> {{personal.homeCity}}</label></b-row>
            <b-row><label><span>Zip Code:</span> {{personal.homeZipCode}}</label></b-row>
            <b-row><label><span>Phone Number:</span> {{personal.homeNumber}}</label></b-row>
            <b-row><label><span>Email:</span> {{personal.homeEmail}}</label></b-row>
            <b-row><label><span>College Degree:</span> {{personal.homeDegree}}</label></b-row>                                    
        </section>
        <section>     
            <h3>Work History</h3>       
            <b-row><label><span>Current Job:</span> {{work.jobName}}</label></b-row>
            <b-row><label><span>Address:</span> {{work.jobAddress}}</label></b-row>
            <b-row><label><span>City:</span> {{work.jobCity}}</label></b-row>
            <b-row><label><span>Zip Code:</span> {{work.jobZipCode}}</label></b-row>
            <b-row><label><span>Job Title:</span> {{work.jobTitle}}</label></b-row>
            <b-row><label><span>Description:</span> {{work.jobDescr}}</label></b-row>
            <b-row><label><span>Pay:</span> {{work.jobPay}}</label></b-row>                                    
        </section>
        <section>     
            <h3>Professional Skills</h3>       
            <b-row><label><span>Skill #1:</span> {{skills.feSkills}}</label></b-row>
            <b-row><label><span>Skill #2:</span> {{skills.beSkills}}</label></b-row>
            <b-row><label><span>Skill #3:</span> {{skills.dbSkills}}</label></b-row>
            <b-row><label><span>Skill #4:</span> {{skills.doSkills}}}</label></b-row>                                    
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

    h3 {
        text-decoration-line: underline;
    }

    span {
        font-weight: 500;
    }
</style>