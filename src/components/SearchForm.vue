<template>
<div class="container">
    <div class="row">
        <div class="col">
            <div class="form-group mb-2">
                <label class="sr-only">Enter The Name</label>
                <input type="text" placeholder="Enter the name" v-model="search" class="form-control">
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    computed:{
        search:{
            get(){
                return this.$store.state.filter.query;
            },
            set(val){
                this.$store.commit('SET_QUERY', val);
            }
        },
        online:{
            get(){
                return this.$store.state.filter.online;
            },
            set(){
                this.$store.commit('SET_ONLINE');
            }
        }
    }
}
</script>

