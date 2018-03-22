<template>
  <section id="post">
    <PostPreview v-for="post in posts" :key="post.id" 
    :title="post.title"
    :excerpt="post.previewText"
    :thumbnailImage="post.thumbnailUrl"
    :id="post.id"
    />
  </section>
</template>

<script>
import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: "A New Beginning",
          previewText: "This will be awesome don't miss it!",
          thumbnailUrl:
            "https://images.unsplash.com/photo-1505308509987-f7f783ebabfc?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=0e3bdbb41717970d8c1017225644c957&auto=format&fit=crop&w=400&q=60",
          id: "a-new-beginning"
        },
        {
          title: "A Second Beginning",
          previewText: "This will be awesome blog",
          thumbnailUrl:
            "https://images.unsplash.com/photo-1504214208698-ea1916a2195a?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=c9fc7ec2cbf1e7f00746ea9f4810613a&auto=format&fit=crop&w=400&q=60",
          id: "a-second-beginning"
        },
        {
          title: "A Third Beginning",
          previewText: "This will be awesome Travel",
          thumbnailUrl:
            "https://images.unsplash.com/photo-1516354095361-ae3c8810963a?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=8f75174e058dc4acbeb54c41a7812631&auto=format&fit=crop&w=500&q=60",
          id: "a-third-beginning"
        }
      ]
    };
  }
};
</script>

<style>
#post {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}

@media (min-width: 35rem) {
  #post {
    flex-direction: row;
  }
}
</style>
