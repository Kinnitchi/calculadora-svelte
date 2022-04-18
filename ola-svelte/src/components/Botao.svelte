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
    background-color: #404040;
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
    background-color: #333333;
    color: #fff;
  }
  .destaque{
    background-color: #d43e3e;
    color: #fff;
  }
</style>