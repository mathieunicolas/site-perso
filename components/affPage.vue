<template>
  <div>
    <h1>{{ page.title }}</h1>
    <em>{{
      new Date(page.date).toLocaleDateString("fr-FR", {
        day: "2-digit",
        month: "2-digit",
        year: "numeric"
      })
    }}</em>
    <p>
      <nuxt-link
        v-for="label in page.tags"
        :to="'/tag/' + label"
        class="label"
        :key="label"
        ><span class="labelio">{{ label }}</span></nuxt-link
      >
    </p>
    <!-- <strong>{{ page.description }}</strong> -->
    <nuxt-content :document="page" />
    {{ page.statid }}
    <mastotest v-if="page.statid" :statid="page.statid"></mastotest>
  </div>
</template>

<script>
import galerie from "~/components/galpic.vue";
import important from "~/components/important.vue";
import mastotest from "~/components/mastotest.vue";

export default {
  props: ["page"],
  components: { galerie, important, mastotest },
  /*async fetch() {
    const jsonmasto = await this.$http.get(
      "https://api.npoint.io/fdcad7a7f3c0ab924b51"
    );
    this.mastoid = await jsonmasto.json();
    this.mastoid = this.mastoid[this.page.path];
  },*/
  data() {
    return { mastoid: null };
  }
};
</script>
