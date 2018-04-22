<template>
  <section id="about-page">
      <h1>{{ title }}</h1>
      <div class="about-profile folded-img">
          <img class="" :src="profileImg" alt="Avatar Profile">
      </div>
      
      <pre class="about-content">{{ content }}</pre>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return context.app.$storyapi
      .get("cdn/stories/about", {
        version: context.isDev ? "draft" : "published",
      })
      .then(res => {
        console.log(res.data);
        return {
          title: res.data.story.content.title,
          content: res.data.story.content.content,
          profileImg: res.data.story.content.profile_img.url
        };
      });
  }
};
</script>

<style>
#about-page {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 1rem;
  font-family: "Lato", sans-serif;
  flex-direction: column;
  margin: auto;
  width: 80%;
  max-width: 500px;
}

#about-page p {
  white-space: pre-wrap;
}

.about-content {
  font-size: 23px;
}

.about-profile img {
  width: 200px;
  border-radius: 3%;
  box-shadow: 1px 1px 5px 1px rgb(0, 0, 0, 0.5);
}
/*
.folded-img {
  position: relative;
  color: #fff;
  overflow: hidden;
}



.about-profile {
  width: 200px;
}

.folded-img:before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  border-radius: 0;
  border-width: 0 30px 30px 0;
  border-style: solid;
  border-color: #ffffff #ffffff #308277 #308277;
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.3),
    -1px 1px 1px rgba(0, 0, 0, 0.2);
  -moz-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.3), -1px 1px 1px rgba(0, 0, 0, 0.2);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.3), -1px 1px 1px rgba(0, 0, 0, 0.2);
  display: block;
  width: 0;
}*/
</style>
