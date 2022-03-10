<template>
  <v-row class="mb-4">
    <v-col md="12">
      <div class="categories d-flex flex-wrap align-center">
        <div
            v-for="category in categories"
            :key="category.id"
            :class="[category.id === activeId ? 'categories__item__active py-1 px-2 my-2 mr-10': 'categories__item py-1 my-2 mr-10'] "
            @click="selectCategory(category.id)"
        >
          {{ category.name }}
        </div>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'Filters',
  props: {
    categories: {
      type: Array,
    }
  },
  data: () => {
    return {
      activeId: null,
    }
  },
  methods: {
    selectCategory(id) {
      this.activeId = id
    },
  }
}
</script>

<style lang="scss" scoped>
.categories__item {
  color: black;
  transition: .3s;
  cursor: pointer;
  border-bottom: 1px dashed #252C38;
}
.categories__item__active {
  cursor: pointer;
  transition: .3s;
  background: #fff;
  box-shadow: 0px 1px 1px rgba(0, 0, 0, 0.14), 0px 1px 3px rgba(0, 0, 0, 0.12);
}
</style>