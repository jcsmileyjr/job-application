<template>
    <section>
        <dev id="Work">
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Full Name</label></b-col>
                <b-col><input type="text" v-model="personalData.fullName" /></b-col>
                <b-col><label class="example-label">Ex. John Smith</label></b-col>
            </b-form-row>
            <b-form-row class="input-form">
                <b-col><label class="bold-label">Full Name</label></b-col>
                <b-col><input type="text" v-model="personalData.fullName" /></b-col>
                <b-col><label class="example-label">Ex. John Smith</label></b-col>
            </b-form-row>            
            <b-form-row class="input-form">
                <b-col><label class="bold-label">College Degree</label></b-col>
                <b-col><input type="text" v-model="personalData.homeDegree" /></b-col>
                <b-col><label class="example-label">Ex. Computer Science</label></b-col>
            </b-form-row> 
            <div class="centerButton">
                <b-button variant="success" type="submit" size="sm" @click="updateState">Continue</b-button>
            </div>              
        </dev>
    </section>
</template>

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