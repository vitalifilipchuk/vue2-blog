<template>
  <div class="home">
    <addBlog></addBlog>  
  </div>
</template>

<script>
// @ is an alias to /src
import addBlog from '@/components/addBlog.vue'
import AddBlog from '../components/addBlog.vue'

export default {
  name: 'Home',
  components: {
    addBlog,
  }
}
</script>
