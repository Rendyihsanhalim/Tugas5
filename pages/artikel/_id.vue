<template>
    <div class="container mt-4">
        <div v-for="article in articles" :key="article.id" class="row">
            <!-- Kolom untuk card -->
            <div class="col-md-4"   v-if="task.id == paramId">
                <div class="card">
                    <img :src="article.img" class="card-img-top" alt="Gambar Contoh" style="max-width: 100%;">
                    <div class="card-body">
                        <h5 class="card-title">{{ article.title }}</h5>
                        <p class="card-text">{{ article.content }}</p>
                        <nuxt-link :to="'detail/' + article.id" class="btn btn-primary">Continue Reading</nuxt-link>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>


export default {
    data() {
        return {
            paramId: this.$route.params.id,
            articles: [
        { id:1,
          title: "Judul Artikel 1",
          content: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?",
          img: 'https://images.unsplash.com/photo-1649282806617-c51bb282899c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80'
        },
        { id:2,
          title: "Judul Artikel 2",
          content: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?",
          img: 'https://images.unsplash.com/photo-1635732646038-0a1a2fe3f2d6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80'
        },
        { id:3,
          title: "Judul Artikel 3",
          content: "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?",
          img: 'https://images.unsplash.com/photo-1640006807976-a6127e9d6fa0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80'
        },
      ],
        }
    }
}
</script>
