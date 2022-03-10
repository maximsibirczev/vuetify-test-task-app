<template>
  <v-row>
    <v-col
        cols="12"
        md="6" lg="4"
        v-for="post in posts"
        :key="post.id"
    >
      <v-card height="508">
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
  name: 'PostItem',
  props:{
    posts: Array,
  },
  data: () => ({
  //   posts: [
  //     {
  //       id: 0,
  //       title: 'Что нужно знать в ОАЭ',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/1.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //     {
  //       id: 1,
  //       title: 'Россия. Новые направления',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/2.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //     {
  //       id: 2,
  //       title: 'Албания',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/3.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //     {
  //       id: 3,
  //       title: 'Что нужно знать в ОАЭ',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/1.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //     {
  //       id: 4,
  //       title: 'Россия. Новые направления',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/2.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //     {
  //       id: 5,
  //       title: 'Албания',
  //       description: 'Современная Турция образовалась в 1923 году в результате распада Османской империи после её поражения в Первой мировой войне и последовавшей национально-освободительной войны.',
  //       img: '/images/3.jpg',
  //       date: '5 мая 2021',
  //       timeToRead: '3 мин',
  //     },
  //   ],
  }),
}
</script>
<style>
.post-item__chip {
  background: red !important;
}

</style>
