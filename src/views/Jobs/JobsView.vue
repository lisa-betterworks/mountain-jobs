<template>
  <h1>Jobs</h1>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobDetails', params: { id: job.id } }">
      <h4>{{ job.title }}</h4>
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: "web designer", id: 1, details: "lorem" },
        { title: "web developer", id: 2, details: "lorem" },
        { title: "graphic designer", id: 3, details: "lorem" },
      ],
    };
  },
};
</script>

<style>
.job h4 {
  background: #f4f4f4;
  padding: 20px;
  border-radius: 10px;
  margin: 10px auto;
  max-width: 600px;
  cursor: pointer;
  color: #444;
}
.job h4:hover {
  background: #ddd;
}
.job a {
  text-decoration: none;
}
</style>
