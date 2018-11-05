<template>
  <div id="app">
    <div class="contai">
      <users-app></users-app>
    </div>
  </div>
</template>

<script>
import UsersApp from './components/UsersApp';

export default {
  name: 'app',
  components: {
    UsersApp
  }
}
</script>

