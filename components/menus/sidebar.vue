<template>
  <nav>
    <sidebar-header />
    <h3>Catégories</h3>
    <ul class="menu">
      <li v-for="cat in categories" :key="cat.updatedAt.toString()">
        <nuxt-link :to="cat.dir + '/'">{{ cat.title }}</nuxt-link>
      </li>
    </ul>
    <h3>Derniers articles</h3>
    <ul class="menu">
      <li v-for="page in articles" :key="page.slug">
        <nuxt-link :to="page.path">{{ page.title }}</nuxt-link>
      </li>
    </ul>
    <!--
    <hr />
    <h3>Newsletter</h3>
    <p>Recevoir un mail de temps en temps avec le récap' des nouveautés ?</p>
    <p class="news">
      Vous pouvez vous abonner <a href="https://log.mathieunicolas.net">ici</a>.
    </p>
    -->
  </nav>
</template>

<script>
export default {
  async fetch() {
    this.categories = await this.$content("", { deep: true })
      .where({ slug: "index" })
      .fetch();

    this.articles = await this.$content("", { deep: true })
      .where({ slug: { $nin: ["index", "welcome"] } })
      .sortBy("updatedAt", "desc")
      .limit(5)
      .fetch();
  },
  data() {
    return { articles: null, categories: null };
  }
};
</script>

<style scoped>
hr {
  border-top: 1px solid lightgrey;
  margin: 2rem 0 1rem 0;
}
p.news {
  font-size: 0.8rem;
}
input {
  width: 100%;
  font-size: 1rem;
}
button {
  margin: auto;
  display: block;
  font-size: 0.8rem;
}
ul.menu {
  list-style-type: none;
  padding: 0;
}
h3 {
}
ul.menu li {
  margin-bottom: 0.5rem;
}
a {
  text-decoration: none;
  color: #1a8a21;
}
a:hover {
  text-decoration: none;
}
nav {
  margin-top: 5rem;
}
</style>
