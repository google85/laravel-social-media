<script setup>
import { Head, Link } from '@inertiajs/vue3';
import GroupItem from '../Components/app/GroupItem.vue'

defineProps({

});
</script>

<template>
    <Head title="Social Media Website" />

    <div class="grid grid-cols-12 gap-3">
        <div class="col-span-3 py-6 px-3">
            <h2 class="text-2xl font-bold">My Groups</h2>
            <div class="py-8">
                <div v-if="false" class="text-gray-400 flex text-center">
                    You are not joined to any groups
                </div>
                <div v-else>
                    <GroupItem image="https://picsum.photos/100"
                                title="Laravel Developers"
                                description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex."
                                />
                    <GroupItem image="https://picsum.photos/100"
                                title="Vue.Js Developers"
                                description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque suscipit tempore alias, culpa."
                                />
                </div>
            </div>
        </div>
        <div class="col-span-6">
            Posts
        </div>
        <div class="col-span-3">
            Followers
        </div>

    </div>

</template>

<style>

</style>
