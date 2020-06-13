<template>
  <div class="about">
    <v-flex>
      <v-img
        src="https://cdn.pixabay.com/photo/2016/03/09/09/39/mountain-1245916_960_720.jpg"
        gradient="to top right, rgba(80,125,201,.39), rgba(25,32,72,.1)"
        height="250px"
      >
        <span
          class="display-2 d-flex justify-center white--text"
          style="float:center;margin-top:70px;text-shadow:2px 2px 4px #000;"
        >
          Sobre
        </span>
        <span
          class="display-1 d-flex justify-center white--text"
          style="float:center;text-shadow:2px 2px 4px #000;"
        >
          o projeto Blogueirinhos
        </span>
      </v-img>
    </v-flex>

    <blockquote
      class="blockquote headline font-weight-thin d-flex justify-center"
      style="margin: 0 56px"
    >
      " Lorem ipsum dolor sit amet, consectetur adipisicing elit.
      Harum maiores modi quidem veniam, expedita quis laboriosam,
      ullam facere adipisci, iusto,
      voluptate sapiente corrupti asperiores rem nemo numquam fuga ab at. "
    </blockquote>

    <v-divider />

    <div
      class="display-1 d-flex ml-12 mt-8 white--grey"
      style="text-shadow:2px 2px 4px #00000007;"
    >
      Tecnologias:
    </div>

    <div style="margin: 15px 25px">
      <v-container fluid>
        <v-row dense>
          <v-col
            v-for="card in cards"
            :key="card.title"
            :cols="card.flex"
          >
            <v-hover>
              <template v-slot="{ hover }">
                <v-card :elevation="hover ? 24 : 6" style="margin: 10px"  >
                  <v-img
                    :src="card.src"
                    class="white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                    height="200px"
                  >
                    <v-card-title v-text="card.title"></v-card-title>
                  </v-img>
                </v-card>
              </template>
            </v-hover>
          </v-col>
        </v-row>
      </v-container>
    </div>

  </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      cards: [
        // { title: 'Vuetify', src: 'https://i.morioh.com/2019/11/01/47e709b4198f.jpg', flex: 4 },
        { title: 'Vuejs', src: 'https://www.mundojs.com.br/wp-content/uploads/2019/12/vue-1232x603.jpeg', flex: 4 },
        { title: 'Vuetify', src: 'https://res.cloudinary.com/practicaldev/image/fetch/s--_VSTqAUX--/c_imagga_scale,f_auto,fl_progressive,h_500,q_auto,w_1000/https://thepracticaldev.s3.amazonaws.com/i/9qypxdkcnrvkzqhxeo59.png', flex: 4 },
        { title: 'Django', src: 'https://i0.wp.com/unaaldia.hispasec.com/wp-content/uploads/2019/06/django.png?resize=1024%2C683&ssl=1', flex: 4 },
        { title: 'Python', src: 'https://miro.medium.com/max/1024/1*e4bHx4q36OYZ58NNlN8nWQ.png', flex: 4 },
        { title: 'Github', src: 'https://i.pinimg.com/600x315/2c/b6/70/2cb670b6ddd8922a1c1b2fee4f6f758c.jpg', flex: 4 },
        { title: 'VSC', src: 'https://www.elegantthemes.com/blog/wp-content/uploads/2019/01/000-VS-Code.png', flex: 4 },

      ],
      mini: false,
    }
  }
}
</script>
