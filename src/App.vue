<template>
  <v-app style="background-color: #F5F5F5;">
    <v-navigation-drawer
      v-model="drawer"
      app
      light
      :mini-variant.sync="mini"
      permanent
    >
      <v-list-item class="px-2">
        <v-list-item-avatar>
          <v-img src="https://cnet1.cbsistatic.com/img/i-bB6r0b7ltJneOyCYhyoILvXFI=/940x0/2020/01/16/4f1d8cf5-d551-4a96-bc49-5004fa7de941/gettyimages-1012078320.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-title>Visitante</v-list-item-title>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in nditems"
          :key="item.title"
          :href="item.href"
          :to="item.name"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider />

        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-login-variant</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Login</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <v-toolbar
        light=""
        height="56px"
      >
        <v-btn
          icon
          @click.stop="mini = !mini"
        >
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
        <v-toolbar-title>Blogueirinhos</v-toolbar-title>
        <v-spacer></v-spacer>

        <div
          v-for="item in tbitems"
          :key="item.title"
          :href="item.href"
          :to="item.name"
          link
        >
          <v-btn icon :href="item.name">
            <v-icon>{{ item.icon }}</v-icon>
          </v-btn>
        </div>
      </v-toolbar>

      <router-view />
    </v-content>

  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      drawer: true,
      nditems: [
        { title: 'Home', icon: 'mdi-home-city', name: '/' },
        { title: 'Posts', icon: 'mdi-view-dashboard', name: 'posts' },
        { title: 'Sobre', icon: 'mdi-information-outline', name: 'about' },
        { title: 'Descubra!', icon: 'mdi-rocket-launch-outline', name: 'discovery' },
      ],
      tbitems: [
        { id: '1', icon: 'mdi-magnify', name: '/' },
        { id: '2', icon: 'mdi-github', name: 'https://github.com/LucyBrandao/blogueirinhos_api' },
        { id: '3', icon: 'mdi-information-outline', name: 'about' },
        { id: '5', icon: 'mdi-invert-colors', name: '' },
      ],
      mini: false,
    }
  }
}
</script>
