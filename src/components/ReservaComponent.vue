<template>
<div class="container">
    <table class="table">
     <!-- <thead>
            <tr>
            <th scope="col">#</th>
            <th scope="col">First</th>
            <th scope="col">Last</th>
            <th scope="col">Handle</th>
            </tr>
        </thead> -->
        <tbody>
            <tr>
            <th scope="row">1</th>
            <td><input :value="dado.acomodacao"></td>
            <td><input :value="dado.checkin"></td>
            <td><input :value="dado.checkout"></td>
            <td> <input :value="dado.hospedes"></td>
            <td> <input :value="dado.criancas"></td>
            <td>
            <button type="button" class="btn btn-dark">editar</button>
            <button type="button" class="btn btn-dark" @click="excluirReserva">excluir</button>
            </td>
            </tr>
        </tbody>
    </table>
</div>
</template>

<script>
export default {
  props: {
    dado: {
      type: Object,
      default: () => ({})
    }
  },
  methods: {
    excluirReserva () {
      this.$store.dispatch('deleteDado', this.dado.id)
    }
  }

}
</script>

<style>

</style>
