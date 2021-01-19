<template>
    <div class="admin-post-page">
        <section class="update-form">
            <AdminPostForm :post="loadedPost" />
        </section>
    </div>
</template>

<script>
    import AdminPostForm from '@/components/Admin/AdminPostForm'
    export default {
        layout: 'admin',
        components: {
            AdminPostForm
        },
        data() {
            return {
                loadedPost: {
                    author: "Seth Brady",
                    title: "An Amazing Post",
                    thumbnaiink:'https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg',
                    content: "The best content ever, here"
                }
            }
        }
    }
</script>

<style scoped>
    .update-form {
    width: 90%;
    margin: 20px auto;
    }
    @media (min-width: 768px) {
    .update-form {
        width: 500px;
    }
    }
</style>