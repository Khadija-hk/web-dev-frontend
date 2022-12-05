<template>
    <div>
        <h2> {{ phone.name }} </h2>
        <ul>
            <li>Release: {{ phone.release }}</li>
            <li>Operating system: {{ phone.os }}</li>
            <li>Memory: {{ phone.memory }} GB</li>
            <li>Battery: {{ phone.battery }} maH</li>
            <li>Headphone jack: {{ phone.headphone }}</li>
            <li>Price: ${{ phone.price }}</li>
            <li>Status: {{ phone.status }}</li>
        </ul>
    </div>

</template>

<script>

export default {
    name: 'PhoneItem',
    props: {
        phone: Array
    }
}

</script>

<style scoped>
h2 {
    margin: 2px;
    font-size: 2em;
    text-align: center;
}

li {
    font-style: italic;
    font-family: 'Times New Roman', Times, serif;
    font-size: 1.3em;
}

div {
    background-color: #E5CFFB;
    color: black;
    padding: 1.5em;
    border-style: groove;
}
</style>