<template>
    <div class="row">
        <div class="col">
            <div class="form-group mb-2">
                <label class="sr-only">Escribe Tu Busqueda</label>
                <input type="text" v-model="search" class="form-control">
            </div>

            <div class="form-check form-check-inline">
                <input type="radio" v-model="online" :value="true" class="form-radio-input">
                Online
            </div>
            <div class="form-check form-check-inline">
                <input type="radio" v-model="online" :value="false" class="form-radio-input">
                Offline
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
        },
    }
}
</script>

