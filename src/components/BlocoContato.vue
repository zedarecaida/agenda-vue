<template>
  <div id="blocoContato">
     
      <div id="dadosContatos">
          <span >{{contato.nome}}</span>
          <span >{{contato.telefone}}</span>
          <span >{{contato.email}}</span>
      </div>
       <button @click="excluirContato(contato.id)" id="botaoExcluir" >
          <img src="../assets/lixeira.png" alt="Lixeira">
      </button>
  </div>
</template>

<script>
import {mapActions} from "vuex";

export default {
    name: "BlocoContato",
    methods: mapActions(["excluirContato"]),
    props:{
        contato: Object
    }
}
</script>

<style scoped>
#blocoContato{
    display: flex;
    width: 80%;
    margin: 5px auto 30px auto;
    background-color: white;
    border-radius: 15px;
    font-family: "padrao";
    padding: 15px;
    justify-content: center;
    color: black;
}
button{
    border: none;
    outline: none;
    float: right;
    background-color: white;
    vertical-align: middle;
    align-items: flex-end;
}
button:hover {
  cursor: pointer;
}
button img {
    float: flex;
  width: 50px;
}

#dadosContatos{
    width: 80%;
    font-size: 70%;
    text-align: right;
}
span{
    display: block;
}
span:first-child{
    font-size: 150%;
    font-family: "bold";
}

</style>