<template>
  <q-item
    clickable
    v-ripple
  >
    <!-- Photo du client -->
    <q-item-section avatar>
      <q-avatar>
        <img :src="personne.picture.thumbnail">
      </q-avatar>
    </q-item-section>
    <!-- Nom et prénom -->
    <q-item-section>
      <q-item-label>
        {{ personne.name.first }} <strong>{{ personne.name.last }}</strong>
      </q-item-label>
      <q-item-label caption>
        {{ personne.email }}
      </q-item-label>
    </q-item-section>
    <!-- Icone mail -->
    <q-item-section side>
      <a :href="'mailto:' + personne.email">
        <q-icon name="mail" color="primary" size="sm"/>
      </a>
    </q-item-section>
  </q-item>
</template>

<script>
export default {
  name: 'ClientItem',
  props: {
    personne: {
      type: Object,
      requiered: true
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
}
</style>
