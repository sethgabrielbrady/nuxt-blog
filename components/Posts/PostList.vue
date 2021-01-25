<template>
    <div class="posts-page">
        <section class='post-lists'>
            <PostPreview
                v-for="post in posts"
                :key="post.id"
                :id="post.id"
                :isAdmin="isAdmin"
                :title="post.title"
                :thumbnail="post.thumbnail"
                :previewText="post.previewText"
            />
        </section>
    </div>
</template>

<script>
    import PostPreview from '@/components/Posts/PostPreview'
    export default {
        components: {
            PostPreview,
        },
        props: {
            isAdmin: {
                type: Boolean,
                default: false
            },
            posts: {
                type: Array,
                required: true
            }
        }
    }
</script>

<style scoped>
    .post-lists {
        display: flex;
        padding: 20px;
        box-sizing: border-box;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
    }
</style>