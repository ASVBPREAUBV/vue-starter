<template>
    <div>
        <md-datepicker v-model="selectedDate">
            <label>Select date</label>
        </md-datepicker>
    </div>
</template>

<script>
import Vue from "vue";
import { MdDatepicker, MdButton, MdDialog } from "vue-material/dist/components";
import "vue-material/dist/vue-material.min.css";

Vue.use(MdDatepicker);
Vue.use(MdButton);
Vue.use(MdDialog);

export default {
  name: "MyLabeledDatepicker",
  data: () => ({
    selectedDate: null
  })
};
</script>
