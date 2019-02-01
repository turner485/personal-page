<template>
    <div>
        <app-main></app-main>
        
    </div>
</template>

<script>
// Imports
import Vue from 'vue';
import VueSweetalert2 from 'vue-sweetalert2'
import Main from './components/Main.vue';
Vue.use(VueSweetalert2);

export default {
    components: {
        'app-main': Main
    },
    data () {
    
    },
    methods: {

    }
}
</script>
