<template>
  <div id="header">
        <h1>Minha agenda</h1>
  </div>
</template>

<script>
export default {
    name: "Header"
};
</script>

<style scoped>
#header{
    background-color: var(--cor-destaque);
    color: white;
    padding: 45px;
    display: flex;
    width: 100vw;
    
}

h1{
    font-size: 60px;
    font-family: "padrao1";
    margin: 0px;
    align-items: center;
    padding: 0px;
    margin-block-start: 0;
    margin-block-end: 0;
    display: inline-flex;
}


</style>