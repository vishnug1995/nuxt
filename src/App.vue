<template>
<div id="app">
    <!-- <div ref="hellow">here</div> -->
    <!-- <div @click="adddata">add data</div> -->
    <input v-model="name"/> <button>add data</button>
    
    dd
    <ul>
        <li>sdfgsdfg   <button>delete</button> <button>edit</button></li>
        <li>dfgsdfg <button>delete</button> <button>edit</button></li>
        <li>dfgsdfgsd <button>delete</button> <button>edit</button></li>
        <li>dfgsdfg <button>delete</button> <button>edit</button></li>
        <li>dgsdfgsdfg <button>delete</button> <button>edit</button></li>
    </ul>


</div>
</template>

<script>
import {
    mapGetters,
    mapActions
} from 'vuex'
export default {
    name: 'App',
    data() {
        return {
            name: '',

        }
    },
    computed: {
        ...mapGetters({
            count: 'get_count',
        }),
    },
    created() {
        console.log('created', this.name, this.$refs.hellow)
    },
    mounted() {
        console.log('mounted', this.name, this.$refs.hellow)
    },
    methods: {
        ...mapActions({
            //adddata: 'increment',
        }),
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
