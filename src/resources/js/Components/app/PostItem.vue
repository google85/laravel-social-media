<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';

    defineProps({
        post: Object
    })

</script>

<template>
    <div>
        <div class="flex items-center gap-2 mb-3">
            <a href="javascript:void(0)">
                <img :src="post.user.avatar" class="w-[40px] rounded-full"/>
            </a>
            <div>
                <h4 class="font-bold">
                    <a href="javascript:void(0)">
                        {{ post.user.name }}
                    </a>
                </h4>
                <small class="text-gray-400">{{ post.created_at }}</small>
            </div>
        </div>
        <div>
            <Disclosure v-slot="{ open }">
                <div v-if="!open" v-html="post.body.substring(0, 200)" />
                <DisclosurePanel>
                    <div v-html="post.body" />
                </DisclosurePanel>
                <div class="flex justify-end">
                    <DisclosureButton class="text-blue-500">
                        {{ open ? 'Read less' : 'Read more' }}
                    </DisclosureButton>
                </div>
            </Disclosure>
        
        </div>
    </div>
</template>

<style scoped>

</style>
