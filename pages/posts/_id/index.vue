<template>
    <div class="single-post-page">
        <section class="post">
            <h1 class="post-title">{{ loadedPost.title }}</h1>
            <div class="post-details">
                <div>Updated on: {{ loadedPost.updatedDate }}</div>
                <div>Authored by:{{ loadedPost.author}}</div>
            </div>
            <p class="post-content">{{ loadedPost.content }}</p>
        </section>
        <section class="post-feedback">
            <p>
                Send feedback to <a href="mailto:awesomefeedback@awesomedomain.com"> my email</a>
            </p>
        </section>
    </div>
</template>

<script>
    export default {
     asyncData(context, callback) {
        setTimeout(() => {
             callback(null, {
                loadedPost: {
                    id: "1",
                    title: "Post (ID: " + context.params.id+ ")",
                    previewText:"This is a post",
                    author: "Seth Brady",
                    updatedDate: new Date(),
                    content: "Some dummy text",
                    thumbnail:"https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg"
                 }
             });
        }, 1000);
     }
    }
</script>

<style scoped>
    .single-post-page {
        padding: 30px;
        text-align: center;
        box-sizing: border-box;
    }

    .post {
     width: 100%;
    }

    @media (min-width: 768px) {
        .post {
            width: 600px;
            margin: auto;
        }
    }

    .post-content {
        font-weight:bold;
    }

    .post-title {
     margin: 0;
    }

    .post-details {
        padding: 10px;
        box-sizing: border-box;
        border-bottom: 3px solid #ccc;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }

    @media (min-width: 768px) {
        .post-details {
            flex-direction: row;
        }
    }

    .post-detail {
        color: rgb(88, 88, 88);
        margin: 0 10px;
    }

    .post-feedback a {
        color: red;
        text-decoration: none;
    }

    .post-feedback a:hover,
    .post-feedback a:active {
        color: salmon;
    }
</style>