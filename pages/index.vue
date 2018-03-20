<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id" 
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id"/>
  </section>
</template>

<script>
import PostPreview from "@/components/Blog/PostPreview";

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: 'First post!',
          previewText: 'This is the first post, hopefully I can share tips and techniques here',
          thumbnailUrl: 'https://instagram.fsea1-1.fna.fbcdn.net/vp/6c08b6b951973255d5b23a08ee58eba6/5B48CF72/t51.2885-15/s640x640/sh0.08/e35/25026363_1089505464519863_1881255410053152768_n.jpg',
          id: 'first-post'
        },
        {
          title: 'Second post!',
          previewText: 'This is the second post, hopefully I can share tips and techniques here',
          thumbnailUrl: 'https://instagram.fsea1-1.fna.fbcdn.net/vp/6c08b6b951973255d5b23a08ee58eba6/5B48CF72/t51.2885-15/s640x640/sh0.08/e35/25026363_1089505464519863_1881255410053152768_n.jpg',
          id: 'second-post'
        }
      ]
    }
  }
}
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
