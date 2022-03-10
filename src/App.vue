<template>
  <v-app>
    <v-main class="main__container">
      <v-container>
        <Breadcrumbs :breadcrumbs="breadcrumbs"></Breadcrumbs>
        <TitlePages :title="title"></TitlePages>
        <PostCategories :categories="categories"/>
        <Posts :posts="posts"></Posts>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>

import Posts from "./components/Posts";
import PostCategories from "./components/PostCategories";
import Breadcrumbs from "./components/Breadcrumbs";
import TitlePages from "./components/TitlePages";
import data from './constants/fake-data'

export default {
  name: 'App',
  components: {
    PostCategories,
    Breadcrumbs,
    TitlePages,
    Posts,

  },
  data: () => ({
    breadcrumbs: data.breadcrumbs,
    title: data.title,
    categories: data.categories,
    posts: data.posts,
  }),
};
</script>

<style>
.main__container {
  background: #F5F5FA;
}
</style>
