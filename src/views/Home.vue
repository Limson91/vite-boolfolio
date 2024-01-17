<script>
export default {
    data() {
        return {
            homeMessage: 'Welcome!',
        };
    },

    computed: {
        formattedMessage() {
            return this.homeMessage.toUpperCase();
        },
    },

    method: {
        newMessage() {
            this.homeMessage = 'New Message!'
        },
    },

    created() {
        console.log('Home component has been successfully created!');
    },
};
</script>

<template>
    <div>
        <h2>{{ homeMessage }}</h2>
        <p>{{ formattedMessage }}</p>

        <button @click="newMessage">New Message</button>
    </div>
</template>

<style scoped lang="scss"></style>