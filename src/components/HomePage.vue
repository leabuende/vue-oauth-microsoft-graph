<template>
  <div class="home">
    <h1>This page is empty and errorless</h1>
    <basebutton
      class="button"
      text="This is a new primary button"
      :color="colors[0]"
    ></basebutton>
    <basebutton
      class="button"
      text="This is a new warn button"
      :color="colors[1]"
    ></basebutton>
    <basebutton
      class="button"
      text="This is a new danger button"
      :color="colors[2]"
    ></basebutton>
    <basebutton class="button" text="This is a new default button"></basebutton>
    <basebutton
      class="button"
      text="This is an async button"
      :disabled="isPending"
      @click.native="handleClick()"
    />
    <p v-if="isPending">
      Wait before clicking again...
    </p>

    <basebutton
      class="button"
      text="This is a modified async button"
      :disabled="isPendingModified"
      @click.native="handleClickMod()"
    />
    <p>Waiting time : {{time/1000}} seconds</p>
    <p v-if="isPendingModified">
      Wait before clicking again...
    </p>
   
  </div>
</template>

<script>
import basebutton from "./basebutton.vue";
export default {
  name: "Homepage",
  components: {
    basebutton,
  },
  data() {
    return {
      colors: ["primary", "warn", "danger"],
      isPending: false,
      isPendingModified : false,
      time : 2000
    };
  },
  methods: {
    async handleClick() {
      this.isPending = true;
      await this.wait(2000);
      this.isPending = false;
    },
    async handleClickMod() {
      this.isPending = true;
      await this.wait(this.time);
      this.isPending = false;
      this.time +=1000;
    },
    wait(ms) {
      return new Promise((resolve) => setTimeout(resolve, ms));
    },
  },
};
</script>

<style scoped>
.home {
  min-height: 100vh;
}
.button {
  margin-bottom: 10px;
}
</style>
