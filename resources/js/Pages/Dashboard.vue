<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
import PostCard from '@/components/userDashboard/PostCard.vue';
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout class="bg-light main-container">
       <div class="post-holder">
        <PostCard class="post-card"/>
       </div>
    </AuthenticatedLayout>

</template>
<style scoped>
.main-container{
    width: 100%;
    height: 100%;
}
.post-holder{
    position: absolute;
    overflow-y: scroll;
    overflow-x: hidden;
}
.post-card{
    position: relative;
    top: 0;
}
</style>