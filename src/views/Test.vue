<template>
    <div>
        <h2>test: {{test}}</h2>
        <button @click="greet">greet</button>
        <p>{{ message }}</p>
        <input v-model="message">
        <p>{{(message=="Message") ? "message == Message":"message != Message" }}</p>
        <p v-if="message">Now you see me</p>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from "vue-property-decorator";
    import * as ws from "ws";
    import {WebsocketService} from "../components/websocket";
    import {Subject} from "rxjs";

    @Component({
        components: {}
    })
    class Test extends Vue {
        test = "";
        message = "";
        res = ["test1", "test2"];

        //ws:Subject<MessageEvent>;

        constructor() {
            super();
            this.test = "constructor";
            this.message = "delete me";
            //this.ws = new WebsocketService();
        }

        bla() {
        }

        greet() {
            this.test = "greet";
        }
    }

    export default Test;
</script>
