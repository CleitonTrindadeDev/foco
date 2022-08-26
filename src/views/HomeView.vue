<template>
<div class="d-flex container">
  <form action="">
    <div class="row px-4">
      <div class="col-6">
        One of three columns
      </div>
      <div class="col-6">
        <input class="form-control " type="search" placeholder="Pesquisar" aria-label="Search">
      </div>
    </div>
  </form>
  <button type="button" class="btn btn-primary h-25 btn-lg"> + Fazer reserva</button>
</div>
<ReservasComponent/>
</template>

<script>
import ReservasComponent from '@/components/ReservasComponent.vue'
export default {
  name: 'HomeView',
  components: {
    ReservasComponent
  },
  created () {
    this.$store.dispatch('getDados')
  }
}
</script>

<style scoped>
.container{
    margin-top: 120px !important;
}
form{
  border-radius: 1rem;
  box-shadow: 1px 2px 1px rgba(0, 0, 0, 0.26);
}
button{
  background-color: #5582eb !important;
}
</style>
