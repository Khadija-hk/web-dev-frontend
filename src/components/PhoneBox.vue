<template>
    <div class="bookbox">
        <div v-for="phone in phones" :key="phone.name">
            <PhoneItem :phone="phone" />
        </div>
    </div>
</template>

<script>

import PhoneItem from './PhoneItem.vue'

export default {
    name: 'PhoneBox',

    components: {
        PhoneItem
    },

    props: {
        phones: Array
    }

}

</script>

<style scoped>
.bookbox {
    padding: 1em;
    color: gray;
}
</style>