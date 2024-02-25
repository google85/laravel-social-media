<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';
import LikeIcon from '@/Components/app/icons/LikeIcon.vue';
import CommentIcon from '@/Components/app/icons/CommentIcon.vue';
import DocumenIcon from '@/Components/app/icons/DocumentIcon.vue';

    defineProps({
        post: Object
    })

    function isImage(attachment) {
        const mime = attachment.mime.split('/')
        return mime[0].toLowerCase() === 'image'
    }

</script>

<template>
    <div class="bg-white border rounded p-4 mb-3">
        <div class="flex items-center gap-2 mb-3">
            <a href="javascript:void(0)">
                <img :src="post.user.avatar" class="w-[40px] rounded-full border border-2 transition-all hover:border-blue-500"/>
            </a>
            <div>
                <h4 class="font-bold">
                    <a href="javascript:void(0)" class="hover:underline">{{ post.user.name }}</a>
                    <template v-if="post.group">
                        >
                        <a href="javascript:void(0)" class="hover:underline">{{ post.group.name }}</a>
                    </template>
                </h4>
                <small class="text-gray-400">{{ post.created_at }}</small>
            </div>
        </div>
        <div class="mb-3">
            <Disclosure v-slot="{ open }">
                <div v-if="!open" v-html="post.body.substring(0, 200)"/>
                <DisclosurePanel>
                    <div v-html="post.body" />
                </DisclosurePanel>
                <div class="flex justify-end">
                    <DisclosureButton class="text-blue-500 hover:underline">
                        {{ open ? 'Read less' : 'Read more' }}
                    </DisclosureButton>
                </div>
            </Disclosure>
        </div>
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-3 mb-3">
            <template v-for="attachment of post.attachments" class="h-[160px]">
                <div class="group aspect-square bg-blue-100 flex flex-col items-center justify-center text-gray-500 relative">
                    <!-- Download -->
                    <button class="opacity-0 group-hover:opacity-100 transition-all w-8 h-8 flex items-center justify-center text-gray-100 bg-gray-600 rounded absolute right-2 top-2 cursor-pointer hover:bg-gray-800">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-4 h-4">
                            <path fill-rule="evenodd" d="M12 2.25a.75.75 0 0 1 .75.75v11.69l3.22-3.22a.75.75 0 1 1 1.06 1.06l-4.5 4.5a.75.75 0 0 1-1.06 0l-4.5-4.5a.75.75 0 1 1 1.06-1.06l3.22 3.22V3a.75.75 0 0 1 .75-.75Zm-9 13.5a.75.75 0 0 1 .75.75v2.25a1.5 1.5 0 0 0 1.5 1.5h13.5a1.5 1.5 0 0 0 1.5-1.5V16.5a.75.75 0 0 1 1.5 0v2.25a3 3 0 0 1-3 3H5.25a3 3 0 0 1-3-3V16.5a.75.75 0 0 1 .75-.75Z" clip-rule="evenodd" />
                        </svg>
                    </button>

                    <img v-if="isImage(attachment)" :src="attachment.url"
                        class="object-cover aspect-square"/>
                        
                    <template v-else>
                         <!-- Document -->
                        <DocumenIcon/>

                        <small>{{ attachment.name }}</small>
                    </template>
                </div>
            </template>
        </div>
        <div class="flex gap-2">
            <button class="text-gray-800 flex gap-1 items-center justify-center bg-gray-100 rounded-lg hover:bg-gray-200 py-2 px-4 flex-1">
                <LikeIcon/>
                Like
            </button>
            <button class="text-gray-800 flex gap-1 items-center justify-center bg-gray-100 rounded-lg hover:bg-gray-200 py-2 px-4 flex-1">
                <CommentIcon/>
                Comment
            </button>
        </div>
    </div>
</template>

<style scoped>

</style>
