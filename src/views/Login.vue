        <template>
    <section class="section">
        <div class="container">
            <h1 class="title">
                Hello World
            </h1>
            <p class="subtitle">
                My first website with <strong>Bulma</strong>!
            </p>
            <div class="columns">
                <div class="column">
                    First column
                </div>
                <div class="column">
                    Second column
                </div>
                <div class="column">
                    Third column
                </div>
                <div class="column">
                    Fourth column
                </div>
            </div>
            <md-field>
                <label>Email</label>
                <md-input v-model="initial"></md-input>
                <span class="md-helper-text">Helper text</span>
            </md-field>

            <md-field>
                <label>Password</label>
                <md-input v-model="password" type="password"></md-input>
                <span class="md-helper-text">Helper text</span>
            </md-field>

        </div>
    </section>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
//import { MdField, MdInput } from "vue-material/dist/components";
import VueMaterial from "vue-material";
import "vue-material/dist/vue-material.min.css";

Vue.use(VueMaterial);

@Component({
  data: () => ({
    password: "",
    initial: "",
    type: null,
    withLabel: null,
    inline: null,
    number: null,
    textarea: null,
    autogrow: null,
    disabled: null
  })
})
class Login extends Vue {
  test = "test";

  run() {
    this.test == "test" ? (this.test = "not test") : (this.test = "test");
  }
}
export default Login;
</script>
