<template>
    <div>
        <h2>Login</h2>
        <button @click="test">greet</button>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from "vue-property-decorator";

    @Component({
        components: {}
    })

    class Login extends Vue {

        test=()=>{
            console.log('test')
        }
    }


    export default Login;
</script>
