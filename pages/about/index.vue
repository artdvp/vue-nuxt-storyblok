<template>
  <section id="about-page">
      <h1>Hi, I'm Artdvp</h1>
      <div class="about-profile folded-img">
          <img class="" src="https://avatars0.githubusercontent.com/u/12493732?v=4" alt="Avatar Profile">
      </div>
      
      <pre class="about-content">I'm a bunch of highly motivated and learning new things, 
Blogging about tech stuff.</pre>
  </section>
</template>

<style scope>
#about-page {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-top: 1rem;
  text-align: center;
  font-family: "Lato", sans-serif;
  flex-direction: column;
}

.about-profile {
  width: 200px;
}

.about-profile img {
  width: 200px;
  border-radius: 3%;
  box-shadow: 1px 1px 5px 1px rgb(0, 0, 0, 0.5);
}

.about-content {
  font-size: 23px;
}

.folded-img {
  position: relative;
  color: #fff;
  overflow: hidden;
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
}
</style>
