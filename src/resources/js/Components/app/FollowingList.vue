<script setup>
import FollowingListItems from '@/Components/app/FollowingListItems.vue';
import ChevronRightIcon from '@/Components/app/icons/ChevronRightIcon.vue';
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';

</script>

<template>
    <div class="px-3 bg-white rounded border h-full py-3 overflow-hidden">
      <div class="block lg:hidden">
         <Disclosure v-slot="{ open }">
               <DisclosureButton class="w-full">
                  <div class="flex justify-between items-center">
                     <h2 class="text-xl font-bold">My Followings</h2>
                     <ChevronRightIcon class="transition-all" :class="open ? 'rotate-90 transform' : ''" />
                  </div>
               </DisclosureButton>
               <DisclosurePanel>
               <FollowingListItems />
               </DisclosurePanel>
         </Disclosure>
      </div>
      <div class="h-full overflow-hidden flex-col hidden lg:flex">
         <h2 class="text-xl font-bold">My Followings</h2>
         <FollowingListItems />
      </div>
    </div>
</template>

<style scoped>

</style>