<template>
  <div class="home">
    <ul>
      <li v-for="attendee in attendees">{{ attendee.profile.first_name }} {{ attendee.profile.last_name }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex'

export default {
  created () {
    this.init()
  },

  computed: {
    ...mapState(['attendees']),
  },

  methods: {
    ...mapActions(['init'])
  }
}
</script>
