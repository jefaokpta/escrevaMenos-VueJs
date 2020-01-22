<template>
  <ul>
    <li v-for="fruta of frutas" :class="{highlighted: fruta.status}" v-on:click="fruta.status=!fruta.status" >
      {{fruta.tipo}}
    </li>
  </ul>
</template>

<script>
export default {
  data () {
    return {
      frutas: [
        {tipo: 'banana',status: false},
        {tipo: 'maca',status: false},
        {tipo: 'framboesa',status: false}
      ]
    }
  }
}
</script>

<style>
.highlighted{
  background-color: orange;
}
</style>
