<template>
  <div class="mastotest">
    <h3>Commentaires à cet article :</h3>
    <p>
      <em
        ><a :href="`https://diaspodon.fr/web/statuses/${statid}`"
          >(Commenter sur mastodon)</a
        ></em
      >
    </p>
    <div v-if="data !== null">
      <mastocom v-for="com in data.descendants"
                :key="com.id.toString()"
                :com="com"
                class="comms"
      ></mastocom>
    </div>
  </div>
</template>

<script>
export default {
  props: ["statid"],
  data() {
    return { data: null };
  },
  async fetch() {
    console.log("yo le mounted diou");
    this.data = await this.$http.$get(
      `https://diaspodon.fr/api/v1/statuses/${this.statid}/context`
    )
    console.log('coucou')
  },
  mounted() {
    this.$fetch();
  },
  fetchOnServer: false
};
</script>

<style>
.mastotest {
  margin-top: 2rem;
}
.comms {
  width: 75%;
  margin: auto;
  margin-top: 1rem;
}
</style>
