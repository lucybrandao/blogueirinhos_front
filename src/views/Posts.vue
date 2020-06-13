<template>
  <div class="home">
    <v-flex>
      <v-img
        src="https://cdn.pixabay.com/photo/2016/03/09/09/39/mountain-1245916_960_720.jpg"
        gradient="to top right, rgba(80,125,201,.39), rgba(25,32,72,.1)"
        height="250px"
      >
        <span
          class="display-2 d-flex justify-center white--text"
          style="float:center;margin-top:100px;text-shadow:2px 2px 4px #000;"
        >
          Publications
        </span>
        <span
          class="display-1 d-flex justify-center white--text"
          style="float:center;text-shadow:2px 2px 4px #000;"
        >
          Browse articles, keep up to date, and learn more on our blog!
        </span>
      </v-img>
    </v-flex>

    <!-- <v-divider /> -->

    <div v-for="card in cards" :key="card.id" link  style="margin: 20px 68px">
      <v-hover>
        <template v-slot="{ hover }">
          <v-card :elevation="hover ? 24 : 6" class="mx-auto pa-6"  >
            <v-card-title class="display-1 font-weight-bold">{{ card.title }}</v-card-title>
            <v-card-subtitle class="title font-weight-light">{{ card.subtitle }}</v-card-subtitle>
            <v-card-subtitle class="font-italic">{{ card.date }}</v-card-subtitle>
          </v-card>
        </template>
      </v-hover>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Posts',
  data () {
    return {
      cards: [
        {
          title: 'Man must explore, and this is exploration at its greatest',
          subtitle: 'Problems look mighty small from 150 miles up',
          date: 'Posted by Start Bootstrap on October 31, 2017 · 4 mins read'
        },
        {
          title: 'I believe every human has a finite number of heartbeats. I dont intend to waste any of mine.',
          subtitle: 'Never in all their history have men been able truly to conceive of the world...',
          date: 'Posted by Start Bootstrap on October 31, 2017 · 4 mins read'
        },
        {
          title: 'Science has not yet mastered prophecy',
          subtitle: 'We predict too much for the next year and yet far too little for the next ten.',
          date: 'Posted by Start Bootstrap on October 31, 2017 · 4 mins read'
        },
        {
          title: 'Failure is not an option',
          subtitle: 'Many say exploration is part of our destiny, but it’s actually our duty to future generations.',
          date: 'Posted by Start Bootstrap on October 31, 2017 · 4 mins read'
        },
        {
          title: 'The dreams of yesterday are the hopes of today and the reality of tomorrow.',
          subtitle: 'Never in all their history have men been able truly to conceive of the world...',
          date: 'Posted by Start Bootstrap on October 31, 2017 · 4 mins read'
        }
      ],
      mini: false,
    }
  }
}
</script>
