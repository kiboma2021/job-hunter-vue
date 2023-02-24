<template>
  <h1>Job Hunter List of jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    <router-link :to="{ name: 'JobDetail', params: {id: job.id}}">
      {{ job.title }}
    </router-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: []
    }
  },
  mounted() {
    fetch('http://localhost:3000/jobs')
    .then(res => res.json())
    .then(data => this.jobs = data)
    .catch(err => console.log(err.message))
  },
}
</script>

<style>

</style>