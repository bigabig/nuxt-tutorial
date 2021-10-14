<template>
    <div class="container">
        <article>
            <h1 class="title">The Title :/</h1>
            <p>Hello I am the article! :)</p>
        </article>
    </div>
</template>

<script lang="ts">
    export default {
        data() {
            return {
                id: this.$route.params.id,
                posts: [
                    {
                        id: 'tim',
                        title: 'tim is great',
                        content: 'tim is the best :)',
                    },
                ]
            }
        },
        computed: {
            post() {
                return this.posts.find(post => post.id === this.id)
            }
        }
    }
</script>

<style scoped>
p {
    color: green;
}
</style>