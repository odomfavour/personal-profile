<template>
  <div class="about">
    <!-- <h1>{{ $route.params.id }}</h1> -->
    <MyWork/>
  </div>
</template>

<script>
// import MyWork from '@/components/MyWork.vue'
import MyWork from "@/components/MyWork.vue";
export default {
  name: 'Work',
  components: {
    MyWork
  }
}
</script>
