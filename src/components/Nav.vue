<template class="container">
    <b-container fluid >
        <b-row id="nav-section" class="nav-bar">
            <b-col class="bold-label">Front-End Job Application</b-col>
            <b-col>Section: {{section.toUpperCase()}}</b-col>
            <b-col class="bold-label">{{completed}} of 3</b-col>
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
        height: 3rem;
        border-bottom: 1px solid black;
        margin-bottom: 1rem;
        background-color: white;
    }

  @media only screen and (max-width: 550px) {
    .nav-bar {
        background-color:lightgrey;
        color: black;
    }
  }    
</style>