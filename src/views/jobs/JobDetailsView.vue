<template>
  <div v-if="job" class="page-content">
    <h1>{{ job.title }}</h1>
    <p>The job id is: {{ job.id }}</p>
    <p>{{ job.details }}</p>
  </div>
  <p v-else>Loading job details...</p>
</template>

<script>
export default {
  props: ["id"],
  data() {
    return {
      // alternative way to get id from url
      // id: this.$route.params.id,
      job: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs/" + this.id)
      .then((resp) => resp.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style></style>
