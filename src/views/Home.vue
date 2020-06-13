<template>
  <div class="home">
    <v-flex>
      <v-img
        src="https://cdn.pixabay.com/photo/2016/03/09/09/39/mountain-1245916_960_720.jpg"
        gradient="to top right, rgba(80,125,201,.39), rgba(25,32,72,.1)"
        height="500px"
        style="box-shadow: 0 8px 6px -3px rgba(0, 0, 0, 0.3), 0 8px 6px -3px rgba(0, 0, 0, 0.2);"
      >
        <span
          class="display-1 d-flex justify-center white--text"
          style="float:center;margin-top:150px;text-shadow:2px 2px 4px #000;"
        >
          Bem vindo ao projeto
        </span>
        <span
          class="display-4 d-flex justify-center white--text"
          style="float:center;text-shadow:2px 2px 4px #000;"
        >
          &lt;Blogueirinhos! /&gt;
        </span>
        <span
          class="headline d-flex justify-center white--text"
          style="float:center;text-shadow:2px 2px 4px #000;"
        >
          by L &amp; L
        </span>
      </v-img>
    </v-flex>

    <div class="d-flex justify-center mt-md" style="margin-top: 24px">
      <v-icon>mdi-chevron-down</v-icon>
    </div>

    <blockquote
      class="blockquote headline font-weight-thin d-flex justify-center"
      style="margin: 0 56px"
    >
      " Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      Harum maiores modi quidem veniam, expedita quis laboriosam,
      ullam facere adipisci, iusto,
      voluptate sapiente corrupti asperiores rem nemo numquam fuga ab at. "
    </blockquote>
    <v-icon class="d-flex ml-auto" style="margin-bottom: 15px">mdi-earth</v-icon>

    <v-divider />

    <div v-for="card in cards" :key="card.id" link style="margin: 20px 68px">
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
  name: 'Home',
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
