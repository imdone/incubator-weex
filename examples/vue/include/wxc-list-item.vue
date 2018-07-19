<template>
  <div
    class="item" :style="{'background-color': bgColor}"
    v-on:click="click"
    v-on:touchstart="touchstart" v-on:touchend="touchend">
    <text>Hello</text>
    <slot></slot>
  </div>
</template>

<script>
  module.exports = {
    data: function () {
      return {
        bgColor: '#ffffff'
      }
    },
    methods: {
      click: function () {
        this.$emit('click')
      },
      touchstart: function() {
        // FIXME android touch id:114
        // TODO adaptive opposite bgColor id:59
        // this.bgColor = '#e6e6e6';
      },
      touchend: function() {
        // FIXME android touchend not triggered id:58
        // this.bgColor = '#ffffff';
      }
    }
  }
</script>

<style scoped>
  .item {
    padding-top: 25px;
    padding-bottom: 25px;
    padding-left: 35px;
    padding-right: 35px;
    height: 160px;
    justify-content: center;
    /*margin-bottom: 1px; FUTURE */
    border-bottom-width: 1px;
    border-color: #dddddd;
  }
</style>
