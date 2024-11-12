<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout class="bg-light main-container">

        <div class="">
            <div class="left"></div>
        </div>
    </AuthenticatedLayout>
</template>
<style scoped>
.main-container{
    width: 100vw;
    height: 100vh;
}
</style>