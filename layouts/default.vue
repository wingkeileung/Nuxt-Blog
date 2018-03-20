<template>
  <div>
    <NavBar />
    <main class="main-content">
    <nuxt/>
    </main>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar/NavBar'

export default {
  components: {
    NavBar
  }
}
</script>


<style>
* {
  box-sizing: border-box;
}

body {
  font-family: "Arvo", sans-serif;
}

.main-content {
  margin-top: 4.5rem;
}

</style>
