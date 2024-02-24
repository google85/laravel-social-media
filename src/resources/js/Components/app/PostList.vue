<script setup>
import {ref} from "vue";
import PostItem from "@/Components/app/PostItem.vue";

const post1 = {
    user: {
        id: 1,
        avatar: 'https://randomuser.me/api/portraits/men/79.jpg',
        name: 'John Smith'
    },
    group: null,
    attachments: [
        {
            id: 1,
            name: 'test.png',
            url: 'https://picsum.photos/1000',
            mime: 'image/png'
        },
        {
            id: 2,
            name: 'test2.png',
            url: 'https://picsum.photos/999',
            mime: 'image/png'
        },
        {
            id: 4,
            name: 'MyDocument.docx',
            url: '#',
            mime: 'application/msword'
        }
    ],
    body: `
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora aut rem sed deleniti impedit a omnis iure in ex quis! Fugiat soluta libero voluptatem eos reprehenderit inventore eius necessitatibus eveniet ipsam quaerat distinctio alias ex illo atque consectetur, dignissimos iure eum, in earum voluptatibus a quae sunt impedit perspiciatis? Illo, voluptatem sapiente.</p>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora aut rem sed deleniti impedit a omnis iure in ex quis! Fugiat soluta libero voluptatem eos reprehenderit inventore eius necessitatibus eveniet ipsam quaerat distinctio alias ex illo atque consectetur, dignissimos iure eum, in earum voluptatibus a quae sunt impedit perspiciatis? Illo, voluptatem sapiente.</p>
`,
    created_at: '2023-11-19 15:12'
}
const post2 = {
    user: {
        id: 2,
        avatar: 'https://randomuser.me/api/portraits/men/78.jpg',
        name: 'James Does'
    },
    group: {
        id: 1,
        name: 'Laravel Developers'
    },
    body: `
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora aut rem sed deleniti impedit a omnis iure in ex quis! Fugiat soluta libero voluptatem eos reprehenderit inventore eius necessitatibus eveniet ipsam quaerat distinctio alias ex illo atque consectetur, dignissimos iure eum, in earum voluptatibus a quae sunt impedit perspiciatis? Illo, voluptatem sapiente.</p>

<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempora aut rem sed deleniti impedit a omnis iure in ex quis! Fugiat soluta libero voluptatem eos reprehenderit inventore eius necessitatibus eveniet ipsam quaerat distinctio alias ex illo atque consectetur, dignissimos iure eum, in earum voluptatibus a quae sunt impedit perspiciatis? Illo, voluptatem sapiente.</p>
`,
    created_at: '2023-11-19 15:12'
}

</script>

<template>
    <div>
        <PostItem :post="post1" />
        <PostItem :post="post2" />
    </div>
</template>

<style scoped>

</style>
