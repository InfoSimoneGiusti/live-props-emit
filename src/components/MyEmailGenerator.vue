<template>
  <button @click="generateRandomEmail">Genera email casuale</button>
</template>

<script>

import axios from 'axios';

export default {
    name: 'MyEmailGenerator',
    methods: {
        generateRandomEmail() {

            axios.get('https://flynn.boolean.careers/exercises/api/random/mail')
            .then(res => {
                this.$emit('generaEmailCasuale', res.data.response);
            });

        }
    }
}
</script>

<style>

</style>