<template>
  <v-row>
    <v-col
        cols="12"
        md="6" lg="4"
        v-for="post in posts"
        :key="post.id"
    >
      <v-card height="488">
        <v-img
            height="254"
            :src="post.img"
        >
          <v-chip
              class="white py-1 px-2 mt-6"
              label
              link
          >
            Советы
          </v-chip>
        </v-img>
        <div class="d-flex flex-column justify-space-around">
          <v-card-title class="pb-0">
            <h4>{{ post.title }}</h4>
          </v-card-title>
          <v-card-text class="black--text mt-0">
            <p>{{ post.description }}</p>
          </v-card-text>
          <v-card-subtitle class="grey--text d-flex align-center">
            <b>{{ post.date }}</b>
            <b class="pl-3 gray--text">Время чтения: {{ post.timeToRead }} минуты</b>
          </v-card-subtitle>
        </div>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'Posts',
  props:{
    posts: Array,
  },
  data: () => ({
  }),
}
</script>
