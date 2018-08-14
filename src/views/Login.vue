<template>
    <div>
        <h2>Login</h2>
        <button @click="run">{{test}}</button>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component({
  components: {}
})
class Login extends Vue {
  test = "test";
  run() {
    this.test == "test" ? (this.test = "not test") : (this.test = "test");
  }
}
export default Login;
</script>
