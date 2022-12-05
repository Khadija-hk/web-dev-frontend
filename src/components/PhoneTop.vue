<template>
    <div class="heading">
        <h1> {{ webpageTitle }} </h1>
    </div>

</template>

<script>
export default {
    name: 'PhoneTop',

    props: {
        webpageTitle: String
    }
}

</script>

<style scoped>
.heading {
    text-align: center;
    text-decoration: underline;
}
</style>