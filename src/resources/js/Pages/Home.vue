<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({

});
</script>

<template>
    <Head title="Social Media Website" />

    <div class="grid grid-cols-12 gap-3">
        <div class="col-span-3 bg-gray-100 py-6 px-3">
            <h2 class="text-2xl font-bold">My Groups</h2>
            <div class="py-8">
                <div v-if="false" class="text-gray-400 flex text-center">
                    You are not joined to any groups
                </div>
                <div v-else>
                    <div class="flex items-start gap-3">
                        <img src="https://picsum.photos/100" class="w-[48px] rounded-full" />
                        <div>
                            <h3 class="font-black text-xl">Laravel Developers</h3>
                            <div class="text-xs text-gray-500">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex.</div>
                        </div>
                    </div>
                    <div class="flex items-start gap-3">
                        <img src="https://picsum.photos/100" class="w-[48px] rounded-full" />
                        <div>
                            <h3 class="font-black text-xl">Vue.Js Developers</h3>
                            <div class="text-xs text-gray-500">Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex.</div>
                        </div>
                    </div>
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
