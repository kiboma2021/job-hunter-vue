<template>
  <h1>Job Hunter List of jobs</h1>
  <div v-for="job in jobs" :key="job.id">
    {{ job.title }}
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        {title: "Web Developer", description: "Develop websites and maintain existing applications", id: 1},
        {title: "App Developer", description: "Develop websites and maintain existing applications", id: 2},
        {title: "Web Engineer", description: "Develop websites and maintain existing applications", id: 3},
        {title: "Business Analyst", description: "Develop websites and maintain existing applications", id: 4},
      ]
    }
  }

}
</script>

<style>

</style>