<template>
<div class="container mt-4">
    <div class="row">
        <!-- Kolom untuk card -->
        <div class="col-md-4">
            <div class="card">
                <img :src="article.img" class="card-img-top" alt="Gambar Contoh" style="max-width: 100%;">
                <div class="card-body">
                    <h5 class="card-title">{{article.title}}</h5>
                    <p class="card-text">{{article.content}}</p>
                    <nuxt-link :to="'artikel/' + article.id" class="btn btn-primary">Continue Reading</nuxt-link>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    props: {
        article: {
            type: Object,
            default() {
                return {}
            }
        },
    },
    computed: {
        localTask: {
            get() {
                return this.article
            },
            set(newValue) {
                this.$emit('update:task', newValue)
            },
        },
    }
}
</script>

<style scoped>
.article-img {
    width: 100%;
    max-height: 250px;
}
</style>
