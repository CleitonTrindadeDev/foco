<template>
  <div>
       <div>
       <ReservaComponent
       v-for="dado in $store.state.dados"
       :key="dado.id"
       :dado="dado"/>
       </div>
  </div>
</template>

<script>
import ReservaComponent from './ReservaComponent.vue'
export default {
  components: {
    ReservaComponent
  }
}
</script>

<style>

</style>
