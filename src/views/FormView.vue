<template>

<div class="container border p-4 my-5 bg-white">

<form action="" @submit.stop.prevent="addDado">
    <div class="row">

        <h2 class="mb-4">Dados da reserva</h2>

        <div class="col-4">
          <label for="">Acomodação</label>
          <select class="form-control" v-model="acomodacao">
            <option class="invalid selected">Selecione a acomodação</option>
            <option>Quarto simples</option>
            <option>Quarto Duplo</option>
          </select>
        </div>
        <div class="col-2">
          <label for="">Check-in</label>
          <input class="form-control" type="text" placeholder="Default input" v-model="checkin">
        </div>
        <div class="col-2">
          <label for="">Check-out</label>
          <input class="form-control" type="text" placeholder="Default input" v-model="checkout">
        </div>
        <div class="col-2">
          <label for="">Hospedes</label>
          <input class="form-control" type="text" placeholder="Default input" v-model="hospedes">
        </div>
        <div class="col-2">
          <label for="">Crianças</label>
          <input class="form-control" type="text" placeholder="Default input" v-model="criancas">
        </div>

    </div>

    <div class="row">

        <h2 class="mb-4">Dados do responsável</h2>

        <div class="col-4">
         <label for="">Nome</label>
         <input class="form-control" type="text" placeholder="Digite seu nome">
        </div>
        <div class="col-4">
          <label for="">Sobrenome</label>
          <input class="form-control" type="text" placeholder="Digite seu sobrenome">
        </div>
        <div class="col-4">
         <label for="">CPF</label>
         <input class="form-control" type="text" placeholder="Digite seu CPF">
        </div>

        <div class="col-3">
         <label for="">Data de Nascimento</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-3">
          <label for="">Telefone</label>
          <input class="form-control" type="text" placeholder="Digite seu telefone">
        </div>
        <div class="col-3">
         <label for="">Celular</label>
         <input class="form-control" type="text" placeholder="Digite seu celular">
        </div>
        <div class="col-3">
         <label for="">E-mail</label>
         <input class="form-control" type="text" placeholder="Digite seu e-mail">
        </div>

    </div>

     <div class="row">

        <h2 class="mb-4">Endereço</h2>

        <div class="col-4">
         <label for="">CEP</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-4">
          <label for="">Cidade</label>
          <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-4">
         <label for="">Estado</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>

        <div class="col-3">
         <label for="">Rua</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-3">
          <label for="">Número</label>
          <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-3">
         <label for="">Bairro</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>
        <div class="col-3">
         <label for="">Complemento</label>
         <input class="form-control" type="text" placeholder="Default input">
        </div>

        <div class="col d-flex justify-content-end">
         <button type="submit" class="btn btn-primary">Fazer reserva</button>
        </div>

       </div>
      <div>
    </div>
</form>
</div>

</template>

<script>

export default {
  data () {
    return {
      acomodacao: '',
      checkin: '',
      checkout: '',
      hospedes: '',
      criancas: ''
    }
  },
  components: {

  },
  methods: {
    addDado () {
      this.$store.dispatch('addDado', {
        acomodacao: this.acomodacao,
        checkin: this.checkin,
        checkout: this.checkout,
        hospedes: this.hospedes,
        criancas: this.criancas
      }).finally(() => {
        this.acomodacao = ''
        this.checkin = ''
        this.checkout = ''
        this.hospedes = ''
        this.criancas = ''
      })
    }
  }
}
</script>

<style scoped>
.container{
  margin-top: 120px !important;
  border-radius: 1rem;
  box-shadow: 1px 2px 1px rgba(0, 0, 0, 0.26);
}

input{
  margin-bottom: 1.5rem;
}

button{
  background-color: #5582eb !important;
}
</style>
