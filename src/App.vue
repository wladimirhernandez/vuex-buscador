<template>
  <div id="app">
    <div class="contai">
      <movies-app></movies-app>
    </div>
  </div>
</template>

<script>
import MoviesApp from './components/UsersApp';

export default {
  name: 'app',
  components: {
    MoviesApp
  }
}
</script>

