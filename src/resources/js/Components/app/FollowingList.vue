<script setup>
import TextInput from '@/Components/TextInput.vue';
import FollowingItem from '@/Components/app/FollowingItem.vue';
import {ref} from "vue";

const searchKeyword = ref('')

</script>

<template>
    <div class="px-3">
        <h2 class="text-2xl font-bold mb-4">My Friends</h2>
        <TextInput :model-value="searchKeyword" placeholder="Type to search"></TextInput>
        <div class="py-8">
            <div v-if="false" class="text-gray-400 flex text-center">
                You don't have friends yet.
            </div>
            <div v-else>
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
