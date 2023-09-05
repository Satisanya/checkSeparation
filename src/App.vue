<template>
  <v-card>
    <v-layout>
      <v-navigation-drawer
          expand-on-hover
          rail
      >
        <v-list>
          <v-list-item
              v-for="user in users"
              :prepend-avatar="user.profilePicture"
              :title="user.name"
              :subtitle="user.email"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-plus" title="Calculate new check" value="newCheck"></v-list-item>
          <v-list-item prepend-icon="mdi-information" title="How to use" value="howTo"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Credits" value="credits"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main style="height: auto; border: none">
        <Main></Main>
      </v-main>
    </v-layout>
  </v-card>
</template>

<script>
import Main from "@/components/main.vue";
export default {
  components:{
    Main
  },
  data(){
    return{
      users: [
        {id: 1,name: "Alexander", email:"novoseltsev7g21@gmail.com", profilePicture: require('@/profilePictures/minsk.jpg')},
        //{id: 1,name: "Aramarik", email:"sacha.sar@yandex.ru", profilePicture: require('@/profilePictures/moon.jpg')}
      ]
    }
},

}
</script>

<style lang="scss" scoped>

</style>
