<template>
  <header class="flex flex-wrap md:flex-no-wrap items-center justify-between mb-6 -mx-3 -mt-3">
    <ul class="flex items-center">
      <li>
        <router-link :to="{name:'home'}" class="text-sm inline-block p-3 text-gray-800" href="">Home</router-link>
      </li>
      <li><a class="text-sm inline-block p-3 text-gray-800" href="#">Your files</a></li>
    </ul>
    <ul class="flex items-center">
      <li><router-link :to="{name:'login'}" class="text-sm inline-block p-3 text-gray-800" href="#">Sign in</router-link></li>
      <li><a class="text-sm inline-block p-3 text-gray-800" href="">Create account</a></li>
    </ul>
  </header>
</template>

<script>
import  {mapGetters} from 'vuex'
export default {
  computed:{
    ...mapGetters({
      authenticated:'auth/authenticated',
      user:'auth/user',
    })
  }
}
</script>