<template>
  <v-app-bar class="main__navigation" color="black" fixed app elevate-on-scroll>
    <v-container fluid class="pa-0">
      <div class="d-flex justify-space-between">
        <nuxt-link to="/">
          <v-img
            src="/logo.png"
            max-height="40"
            max-width="80"
          />
        </nuxt-link>
        <v-spacer />
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn v-scroll-to="item.link" class="toolbar__items" v-for="(item, index) in items" :key="index" text>
            {{ item.title }}
          </v-btn>
        </v-toolbar-items>
        <v-menu offset-y transition="fab-transition">
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              dark
              class="hidden-md-and-up"
              v-bind="attrs"
              v-on="on"
            >
              Меню
            </v-btn>
          </template>
          <v-list>
            <v-list-item
              v-for="(item, index) in items"
              :key="index"
              v-scroll-to="item.link"
            >
              <v-list-item-title class="menu__link">
                {{ item.title }}
              </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
      </div>
    </v-container>
  </v-app-bar>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      items: [
        { link:'#main', title: 'Главная' },
        { link:'#about-us', title: 'Про нас' },
        { link:'#services', title: 'Услуги' },
        { link:'#cases', title: 'Кейсы' },
        { link:'#footer', title: 'Контакты' }
      ]
    }
  },
  mounted() {
  }
}
</script>

<style scoped>
  .container {
    max-width: 1400px !important;
  }
  .toolbar__items {
    letter-spacing: 2px;
  }
  .menu__link {
    cursor: pointer;
  }
  .menu__link:hover {
    border-bottom: 1px solid #fff;
    margin-bottom: -1px;
  }
</style>
