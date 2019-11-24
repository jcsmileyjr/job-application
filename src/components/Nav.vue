<template class="container">
    <b-container fluid >
        <b-row id="nav-section" class="nav-bar">
            <b-col class="bold-label">Front-End Job Application</b-col>
            <b-col v-if="section=='personal'">PERSONAL INFORMATION</b-col>
            <b-col v-if="section=='work'">WORK HISTORY</b-col>
            <b-col v-if="section=='skills'">PROFESSIONAL SKILLS</b-col>
            <b-col class="bold-label">{{completed}} of 4</b-col>
        </b-row>        
    </b-container>
</template>

<script>
export default {
    name:"nav-section",
    props:['section', 'completed'],
}
</script>

<style scoped>
    .horizontal-navbar {
        display: inline-block;

    }
    ul {
        list-style-type: none;
    }

    li {
        float: left;
    }

    .bold-label {
        font-weight:bold;
    }

    .nav-bar {
        padding-bottom: 2%;
        padding-top: 2%;
        border-bottom: 1px solid black;
        margin-bottom: 1rem;
        background-color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

  @media only screen and (max-width: 550px) {
    .nav-bar {
        background-color:lightgrey;
        color: black;
    }
  }    
</style>