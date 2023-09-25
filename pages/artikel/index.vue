<template>
  <div>
    <HeaderPage />
    <div class="py-4">
      <div class="container">
        <div></div>
        <div class="list-task row">
          <CardItem v-for="(article, index) in articles" :key="index" :article="article" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardItem from "@/components/Card/CardItem.vue"
import HeaderPage from "@/components/HeaderPage.vue"

export default {
  layout(context) {
    return 'custom'
  },
  components: {
    CardItem,
    HeaderPage
  },
  data() {
    return {
      searchQuery: '',
      // Tipe layout daftar task
      isGrid: true,
      // Status saat menambahkan task
      isCreating: false,
      // Daftar task
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
  },
}
</script>
