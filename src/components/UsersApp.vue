<template>
    <div>
        <h1 class="text-center text-muted">Search</h1>
        <search-form></search-form>
        <hr>
        <user-list></user-list>
    </div>
</template>

<script>
import SearchForm from './SearchForm';
import UserList from './UserList';

export default {
  components: {
    SearchForm,
    UserList
  }
}
</script>

