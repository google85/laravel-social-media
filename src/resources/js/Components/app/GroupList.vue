<script setup>
import TextInput from '@/Components/TextInput.vue';
import GroupItem from '@/Components/app/GroupItem.vue';
import {ref} from "vue";
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';

const searchKeyword = ref('')

</script>

<template>
    <div class="px-3 bg-white rounded border py-3 overflow-hidden flex flex-col">
        <div class="flex-1 block lg:hidden">
            <Disclosure v-slot="{ open }">
                <DisclosureButton>
                    <h2 class="text-xl font-bold">My Groups</h2>
                </DisclosureButton>
                <DisclosurePanel>
                    <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full mt-4" />
                    <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
                        <div v-if="false" class="text-gray-400 text-center p-3">
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
                            <GroupItem image="https://picsum.photos/100"
                                        title="Laravel Developers"
                                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex."
                                        />
                            <GroupItem image="https://picsum.photos/100"
                                        title="Vue.Js Developers"
                                        description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque suscipit tempore alias, culpa."
                                        />
                            <GroupItem image="https://picsum.photos/100"
                                        title="Laravel Developers"
                                        description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex."
                                        />
                            <GroupItem image="https://picsum.photos/100"
                                        title="Vue.Js Developers"
                                        description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque suscipit tempore alias, culpa."
                                        />
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
                </DisclosurePanel>
            </Disclosure>
            </div>

        <div class="hidden lg:block">
            <h2 class="text-xl font-bold mb-4">My Groups</h2>
            <TextInput :model-value="searchKeyword" placeholder="Type to search" class="w-full" />
            <div class="mt-3 h-[200px] lg:flex-1 overflow-auto">
                <div v-if="false" class="text-gray-400 text-center p-3">
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
                    <GroupItem image="https://picsum.photos/100"
                                title="Laravel Developers"
                                description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex."
                                />
                    <GroupItem image="https://picsum.photos/100"
                                title="Vue.Js Developers"
                                description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque suscipit tempore alias, culpa."
                                />
                    <GroupItem image="https://picsum.photos/100"
                                title="Laravel Developers"
                                description="Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis adipisci iure alias, consequuntur nobis ex."
                                />
                    <GroupItem image="https://picsum.photos/100"
                                title="Vue.Js Developers"
                                description="Lorem ipsum, dolor sit amet consectetur adipisicing elit. Atque suscipit tempore alias, culpa."
                                />
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
    </div>
</template>

<style scoped>

</style>
