<template>
    <div>
        <h2>test: {{test}}</h2>
        <button @click="greet">greet</button>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import * as ws from "ws";
import {WebsocketService} from '../components/websocket'

@Component({
  components: {}
})
class Test extends Vue {
  test = "";
  res = ["test1", "test2"];

  constructor() {
    super();
    this.test = "constructor";

  }

  bla() {}

  greet() {
    this.test = "greet";
  }
}

export default Test;
</script>
