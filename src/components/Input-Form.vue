<template>
    <section id="input-form">
        <div>
            <label>{{title}}</label>
            <input type="text" />
            <label>{{example}}</label>
        </div>
    </section>
</template>

<script>
export default {
    name: "input-form",
    props:{
        title: String,
        input: String,
        example: String,
    }
}
</script>