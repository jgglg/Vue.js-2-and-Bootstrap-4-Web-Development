<template>
  <div class="container">
    <pomodoro-timer></pomodoro-timer>
    <statistics v-if="user && !isAnonymous"></statistics> 
    <settings v-if="user && !isAnonymous"></settings>
  </div>
</template>
<script>
  import {PomodoroTimer, Settings, Statistics} from './sections'
  import {mapState} from 'vuex'

  export default {
    computed: {
      ...mapState(['user', 'isAnonymous'])
    },
    components: {
      PomodoroTimer,
      Settings,
      Statistics
    }
  }
</script>
<style scoped lang="sass">

</style>
