<template lang="">
  <section>
    filter
  </section>

  <section>
    <div class="controls">
      <button>Refresh</button>
      <router-link to="/register">Register as coach</router-link>
    </div>
    <ul v-if="hasCoaches">
      <li v-for="coach in filterdCoaches" :key="coach.id">
        {{coach.firstName}}
      </li>
    </ul>
    <h3 v-else>No coaches found.</h3>
  </section>
</template>
<script>
export default {
  computed: {
    filterdCoaches() {
      return this.$store.getters['coaches/coaches']
    },
    hasCoaches() {
      return this.$store.getters['coaches/coaches']
    }
  }
}
</script>
<style lang="">
  
</style>