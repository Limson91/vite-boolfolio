<script>
export default {
    data() {
        return {
            pageTitle: 'Contact us!',
            email: 'example@info.com',
            phone: '333-987'
        };
    },

    created() {
        console.log('Contact component has been successfully created!')
    },
};
</script>

<template>
    <div>
        <h2>{{ pageTitle }}</h2>
        <p>Email: {{ email }}</p>
        <p>Phone: {{ phoneNumber }}</p>
    </div>
</template>

<style scoped lang="scss"></style>