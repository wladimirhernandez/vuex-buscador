<template>
    <div class="row" v-if="users.length > 0">
        <user :user="user" v-for="user in users" :key="user.id"></user>
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
