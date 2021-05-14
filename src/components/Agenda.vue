<template>
  <div id="agenda" >  
      <div id="agendaCaixa" v-if="todosContatos != 0">
        
        <BlocoContato
          v-for="contatos in todosContatos"
          v-bind:key="contatos.id"
          :contato="contatos"
        />
      </div>
      <div id="mensagem" v-else>Sem contatos</div>
  </div>
</template>

<script>
import {mapGetters} from 'vuex';
import BlocoContato from './BlocoContato.vue';
export default {
  name: "Agenda",
  data:() =>{
    return {
      
    };
  },
  computed: mapGetters(["todosContatos"]),
  components:{
      BlocoContato
  },
  props:{
    contatos: Object
  }
  
}
</script>

<style scoped>
#agenda{
    font-family: "padrao1";
    font-size: 30px;
    width: 50%;
    margin: 5px;
    padding: 5px;
}
#agendaCaixa{
    padding: 10px 0px;
    color: white;
    font-size: 29px;
    background-color: #c692df;
    border-radius: 20px;
    margin: 0px auto 0px auto;
}

#mensagem {
  float: right;
  font-family: "bold";
}
@media (max-width: 600px){
  #agenda{
    width: 90vw;
  }
}

</style>