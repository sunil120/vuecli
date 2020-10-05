<template>
  <div>
    <app-header v-bind:title="title" v-on:changeTitle="updateTitle($event)"></app-header>
    <app-users v-bind:users="users"></app-users>
    <app-footer v-bind:title="title"></app-footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Users from './components/Users.vue'
import Footer from './components/Footer.vue'

export default {
  components:{
    'app-header': Header,
    'app-users': Users,
    'app-footer': Footer
  },
  data() {
    return {
      users: [
        {name:"Sunil" , 'speciality': "PHP", show: true},
        {name:"Susil" , 'speciality': "Angular", show: true},
        {name:"Aakash" , 'speciality': "Wordpress", show: true},
        {name:"Mayank" , 'speciality': "Designing", show: true}
      ],
      title: "User List"
    }
  },
  methods: {
    updateTitle: function(title) {
      this.title = title
    }
  }
}
</script>
<style scoped>

</style>
