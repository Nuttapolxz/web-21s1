<template>
  <div class="page-team-details"> <h1>United States of America</h1>
  </div>
</template>

<script lang="ts">
import { Team } from '@/store/types'
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class TeamDetails extends Vue {
  get Team ():Team | undefined {
    return this.$store.getters.teamsBySlug[this.$route.params.teamsBySlug]
  }
      get suggestions (): TeamDetails[] {
    return this.$store.state.videos.slice(0, 6)
  }

}
</script>
