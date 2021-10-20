<template>
  <div class="page-team-list"></div>
</template>

<script lang="ts">
import { Team } from '@/store/types'
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class TeamList extends Vue {
    get Team ():Team | undefined {
    return this.$store.getters.teams.
    sort((a:Team, b:Team) => a.name.localeCompare(b.name))
}
}
</script>
