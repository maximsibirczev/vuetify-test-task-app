<template>
    <v-row>
      <v-col  md="12">
        <v-breadcrumbs class="px-0 py-0" :items="breadcrumbs"></v-breadcrumbs>
      </v-col>
    </v-row>
</template>

<script>
export default {
  name: 'Breadcrumbs',
  props:{
    breadcrumbs: Array,
  },
  data: () => ({
  })
}
</script>
<style>
</style>
