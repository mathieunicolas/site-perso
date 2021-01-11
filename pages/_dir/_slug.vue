<template>
  <aff-page :page="data"></aff-page>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const data = await $content(params.dir, params.slug).fetch();

    return { data };
  },
  head() {
    return {
      title: this.data.title,
      meta: [
        {
          hid: "description",
          name: "description",
          content: this.data.description
        },
        // Open Graph
        { hid: "og:title", property: "og:title", content: this.data.title },
        {
          hid: "og:description",
          property: "og:description",
          content: this.data.description
        },
        // Twitter Card
        {
          hid: "twitter:title",
          name: "twitter:title",
          content: this.data.title
        },
        {
          hid: "twitter:description",
          name: "twitter:description",
          content: this.data.description
        }
      ]
    };
  }
};
</script>

<style>
.labelio:hover {
  background-color: orangered;
}
a.label {
  margin-right: 1rem;
  /*background-color: ;*/
}
a.label:hover {
  border: 0;
}
</style>
