<style>
#searchBar {
  width: 600px;
  height: 50px;
  padding: 10px;
  background-color: #29a79b;
  color: white;
}
#searchBar::placeholder {
  color: white;
}
#searchBar:focus {
  background-color: #2eb6a8;
}
#searchBtn {
  width: 70px;
  height: 50px;
  padding: 10px;
  background-color: #05887b;
  color: white;
  margin-right: 15px;
}
#searchBtn:hover {
  background-color: #057d71;
}
#p {
  margin-top: 20px;
  margin-right: 20px;
}
#pic {
  width: 40px;
  height: 40px;
  margin-left: 10px;
  border-radius: 50%;
  background-image: url('../assets/photo-1503443207922-dff7d543fd0e.jpg');
  background-size: cover;
}
</style>
<template>
  <v-app style="background-color:azure">
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      style="background-color:#009688;"
    >
      <!--leftpanel-->
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <!--arrow
      <v-btn @click.stop="miniVariant = !miniVariant" icon>
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>

      window
      <v-btn @click.stop="clipped = !clipped" icon>
        <v-icon>mdi-application</v-icon>
      </v-btn>

      Minus sign
      <v-btn @click.stop="fixed = !fixed" icon>
        <v-icon>mdi-minus</v-icon>
      </v-btn>-->

      <!--Title-->
      <font-awesome-icon
        :icon="['fas', 'robot']"
        style="margin-right:50px;"
        size="lg"
      />
      <v-form>
        <span>
          <input
            id="searchBar"
            name="searchKeyword"
            type="text"
            placeholder="Search your apps"
          />
          <button id="searchBtn">Search</button>
        </span>
      </v-form>
      <v-spacer />
      <p id="p">
        <span>
          <font-awesome-icon :icon="['fas', 'users']" size="lg" />
        </span>
        300
      </p>
      <p id="p">
        <span>
          <font-awesome-icon :icon="['fas', 'th']" size="lg" />
        </span>
        653
      </p>
      <p style="margin-top: 20px;">Amr Sobhy</p>
      <div id="pic"></div>
      <!--rightpanel
      <v-btn @click.stop="rightDrawer = !rightDrawer" icon>
        <v-icon>mdi-menu</v-icon>
      </v-btn>-->
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
