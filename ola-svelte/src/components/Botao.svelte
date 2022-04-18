<script lang="ts">
  export let texto: string
  export let triple: boolean = false;
  export let duplo: boolean = false; 
  export let operacao: boolean = false; 
  export let destaque: boolean = false; 
</script>

<button class="botao" 
  class:triple class:duplo class:operacao class:destaque>
  {texto}
</button>

<style>
  .botao{
    margin: 0;
    border: 1px solid var(--bg);
    flex-basis: 25%;
    background-color: #303030;
    color: #fff;
    cursor: pointer;
  }

  .triple{
    flex-basis: 75%;
  }
  .duplo{
    flex-basis: 50%;
  }
  .operacao{
    background-color: #212121;
    color: #fff;
  }
  .destaque{
    background-color: #d43e3e;
    color: #fff;
  }
  .botao:hover{
    background-color: #212121;
  }
  .operacao:hover{
  background-color: #404040;
  }
  .destaque:hover{
    background-color: #e02a2a;;
  }
</style>