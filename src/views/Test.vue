<template>
    <div>
        <input v-model="test"></input>
        <h2>test: {{test}}</h2>
        <button @click="greet">greet</button>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from "vue-property-decorator";
    import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src

    @Component({
        components: {
            HelloWorld
        }
    })
    class Test extends Vue {
        test = '';

        constructor() {
            super()
            this.test = "constructor"
        }

        greet() {
            this.test = 'greet'
        }
    }

    export default Test
</script>
