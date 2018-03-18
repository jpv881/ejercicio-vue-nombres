<template>
  <div>
    <div class="circle" v-bind:style="{ backgroundColor: color }">{{char}}</div>
  </div>
</template>

<script>

export default {
  props: ["name"],
  data() {
    return {
      char: "",
      color: this.getRandomColor(),
    }
  },
  methods: {
    gimmeName(){
      this.char = this.name.charAt(0);
    },
    getRandomColor() {
      var letters = '0123456789ABCDEF';
      var color = '#';
      for (var i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    },
  },
  created(){
    this.gimmeName();
  }
}

</script>

<style>
  #app div div {
    padding: 13px;
    border-radius: 100%;
    display: block;
    height: 20px;
    width: 20px;
  }

  #app div {
    text-align: center;
  }

  .circle {
    margin-left:auto;
    margin-right: auto;
    margin-bottom: 15px;
  }
</style>
