<template>
    <div class="posts-page">
        <section class='post-lists'>
            <PostPreview
                id='1'
                :isAdmin="isAdmin"
                title='First Post'
                thumbnail='https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
                previewText='Some text here'
            />
            <PostPreview
                id='2'
                :isAdmin="isAdmin"
                title='Second Post'
                thumbnail='https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
                previewText='More text here'
            />
            <PostPreview
                id='3'
                :isAdmin="isAdmin"
                title='Third Post'
                thumbnail='https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg'
                previewText='Again, more text here'
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