<!-- Inspired by bootstrap http://getbootstrap.com/ -->
<template>
  <div
    :class="['panel', 'panel-' + type]"
    :style="{ borderWidth: border }">
    <text
      :class="['panel-header', 'panel-header-' + type]"
      :style="{
        paddingTop: paddingHead,
        paddingBottom: paddingHead,
        paddingLeft: paddingHead*1.5,
        paddingRight: paddingHead*1.5
      }">{{title}}</text>
    <div
      :class="['panel-body', 'panel-body-' + type]"
      :style="{
        paddingTop: paddingBody,
        paddingBottom: paddingBody,
        paddingLeft: paddingBody*1.5,
        paddingRight: paddingBody*1.5
      }">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  module.exports = {
    props: {
      type: { default: 'default' },
      title: { default: '' },
      paddingBody: { default: 20 },
      paddingHead: { default: 20 },
      dataClass: { default: '' }, // FIXME transfer class id:127
      border:{ default: 0 }
    }
  }
</script>

<style scoped>
  .panel {
    margin-bottom: 20px;
    background-color: #fff;
    /*border: 1px solid transparent;*/
    /*border-radius: 10px;*/
    /*-webkit-box-shadow: 0 1px 1px rgba(0,0,0,.05);*/
    /*box-shadow: 0 1px 1px rgba(0,0,0,.05);*/
    border-color: #dddddd;
    border-width: 1px;
  }

  .panel-default {
  }

  .panel-primary {
    border-color: rgb(40, 96, 144);
  }

  .panel-success {
    border-color: rgb(76, 174, 76);

  }

  .panel-info {
    border-color: rgb(70, 184, 218);

  }

  .panel-warning {
    border-color: rgb(238, 162, 54);

  }

  .panel-danger {
    border-color: rgb(212, 63, 58);

  }

  .panel-header {
    background-color: #f5f5f5;
    font-size: 40px;
    /*padding-left: 12px;*/
    /*padding-right: 12px;*/
    /*padding-top: 20px;*/
    /*padding-bottom: 20px;*/
    color: #333;
  }

  .panel-header-default {
  }

  .panel-header-primary {
    background-color: rgb(40, 96, 144);
    color: #ffffff;
  }

  .panel-header-success {
    background-color: rgb(92, 184, 92);
    color: #ffffff;
  }

  .panel-header-info {
    background-color: rgb(91, 192, 222);
    color: #ffffff;
  }

  .panel-header-warning {
    background-color: rgb(240, 173, 78);
    color: #ffffff;
  }

  .panel-header-danger {
    background-color: rgb(217, 83, 79);
    color: #ffffff;
  }

  .panel-body {
    padding-left: 12px;
    padding-right: 12px;
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .panel-body-default {
  }

  .panel-body-primary {
  }

  .panel-body-success {
  }

  .panel-body-info {
  }

  .panel-body-warning {
  }

  .panel-body-danger {
  }
</style>
