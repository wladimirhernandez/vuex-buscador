<template>
    <div class="container"  v-if="users.length > 0">       
    <table class="table">
    <thead>
      <tr>
        <th>#</th>
        <th>Name</th>
        <th>Gender</th>
        <th>Email</th>
        <th>Online</th>
      </tr>
    </thead>
    <tbody>
        <user :user="user" v-for="user in users" :key="user.id"></user>
            </tbody>
        </table>
        </div>
    </div>
    <div v-else="" class="alert alert-danger"> User not Found</div>
</template>

<script>
import User from './UserItem';
import {mapGetters} from 'vuex';

export default {
    components: {
        User
    },
    computed: {
        ...mapGetters({
            users: 'filteredUsers'
        })
    }
}
</script>
