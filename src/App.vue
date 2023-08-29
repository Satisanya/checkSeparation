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
          <v-list-item prepend-icon="mdi-folder" title="My Files" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main style="height: 250px"></v-main>
    </v-layout>
  </v-card>
</template>

<script>
export default {
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
