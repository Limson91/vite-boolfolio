<script>
export default {
    created() {
        console.log('NotFound component has been successfully created!');
    },
};
</script>

<template>
    <div>
        <h1>404 - Page Not Found</h1>
        <p>The page does not exist. Go back to <router-link :to="{ name: 'home' }"> page</router-link></p>
    </div>
</template>

<style scoped>
h1 {
    color: red;
}
</style>