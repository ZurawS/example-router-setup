<template>
  <h1>Available jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'jobDetails', params: { id: job.id } }">
      <h3>
        {{ job.title }}
      </h3>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {
          title: "UX designer",
          id: 1,
          details:
            "In enim ipsum ex anim qui. Ullamco ullamco reprehenderit incididunt velit id voluptate adipisicing consectetur ut commodo veniam. Fugiat enim Lorem pariatur aliquip tempor. Fugiat duis consectetur incididunt sunt eiusmod voluptate consequat. Eiusmod ex laborum pariatur ut magna ex eu incididunt. Eiusmod reprehenderit eu et sunt laboris dolor ad. Nostrud adipisicing id do consequat duis aliqua ullamco anim aute.",
        },
        {
          title: "Backend developer",
          id: 2,
          details:
            "In enim ipsum ex anim qui. Ullamco ullamco reprehenderit incididunt velit id voluptate adipisicing consectetur ut commodo veniam. Fugiat enim Lorem pariatur aliquip tempor. Fugiat duis consectetur incididunt sunt eiusmod voluptate consequat. Eiusmod ex laborum pariatur ut magna ex eu incididunt. Eiusmod reprehenderit eu et sunt laboris dolor ad. Nostrud adipisicing id do consequat duis aliqua ullamco anim aute.",
        },
        {
          title: "Frontend developer",
          id: 3,
          details:
            "In enim ipsum ex anim qui. Ullamco ullamco reprehenderit incididunt velit id voluptate adipisicing consectetur ut commodo veniam. Fugiat enim Lorem pariatur aliquip tempor. Fugiat duis consectetur incididunt sunt eiusmod voluptate consequat. Eiusmod ex laborum pariatur ut magna ex eu incididunt. Eiusmod reprehenderit eu et sunt laboris dolor ad. Nostrud adipisicing id do consequat duis aliqua ullamco anim aute.",
        },
      ],
    };
  },
};
</script>

<style>
.job h3 {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h3:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
