<script setup>
import TextInput from '@/Components/TextInput.vue';
import FollowingItem from '@/Components/app/FollowingItem.vue';
import {ref} from "vue";

const searchKeyword = ref('')

</script>

<template>
    <div class="px-3 bg-white rounded border py-3 h-full overflow-hidden flex flex-col">
        <h2 class="text-xl font-bold mb-4">My Followings</h2>
        <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full" />
        <div class="mt-3 flex-1 overflow-auto">
            <div v-if="false" class="text-gray-400 text-center p-3">
                You don't have friends yet.
            </div>
            <div v-else>
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="John Doe"
                            />
                <FollowingItem image="https://picsum.photos/100"
                               title="Elon Musk"
                            />
            </div>
        </div>
    </div>
</template>

<style scoped>

</style>
