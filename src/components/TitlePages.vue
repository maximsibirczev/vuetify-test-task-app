<template>
  <v-row class="pb-0">
    <v-col md="12" class="pb-0">
      <h2 class="font-size-40 font-weight-black">Наш блог</h2>
<!--      text-h3-->
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'TitlePages',
  props:{
    title: String,
  },
  data: () => ({
  })
}
</script>
<style>
.font-size-40{
  font-size: 40px;
}
</style>
