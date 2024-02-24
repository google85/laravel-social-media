<script setup>
import { Head, Link } from '@inertiajs/vue3';
import GroupList from "@/Components/app/GroupList.vue";
import FollowingList from "@/Components/app/FollowingList.vue";

defineProps({

});
</script>

<template>
    <Head title="Social Media Website" />

    <div class="grid grid-cols-12 gap-3">
        <div class="col-span-3 py-6 px-3">
            <GroupList />
        </div>
        <div class="col-span-6">
            Posts
        </div>
        <div class="col-span-3">
            <FollowingList />
        </div>

    </div>

</template>

<style>

</style>
