<template>
  <q-page padding>
    <h1>Liste des clients</h1>
    <q-list v-if="clients.length > 0" bordered separator>
      <client-item
        v-for="cli in clients"
        :key="cli.id.value"
        :personne="cli"
      />
    </q-list>
    <p v-else>Pas de clients ... il faut faire de la pub</p>
  </q-page>
</template>

<script>
import ClientItem from 'components/ClientItem'
export default {
  name: 'ListeClients',
  components: { ClientItem },
  data () {
    return {
      clients: []
    }
  },
  beforeMount () {
    const monComposant = this
    this.$api.get('?results=100&nat=CH')
      .then(function (reponse) {
        monComposant.clients = reponse.data.results
      })
  }
}
</script>

<style scoped>

</style>
