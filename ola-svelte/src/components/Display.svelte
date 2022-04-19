<script lang="ts">
  export let valor: string

  $: tamanhoFont =  valor.length >= 20 ? 'small' : `s-${valor.length}`

</script>

<div class={`display ${tamanhoFont}`}>
  <span>{valor}</span>
</div>

<style>
  .display{
    display: flex;
    border: 2px solid #00000048;
    height: 30%;
    justify-content: flex-end;
    align-items: center;
    margin: 2px 1px;
    padding: 0px 5px;
    font-size: 1.5rem;
    overflow: hidden;
    border-top-left-radius:  1px;
    border-top-right-radius:  1px;
    background-color: #464646;
    color: #fff;
  }

  .s-11{font-size: 1.4rem;}
  .s-12{font-size: 1.3rem;}
  .s-13{font-size: 1.2rem;}
  .s-14{font-size: 1.1rem;}
  .s-15{font-size: 1.05rem;}
  .s-16{font-size: 1rem;}
  .s-17{font-size: 0.9rem;}
  .s-18{font-size: 0.8rem;}
  .s-19{font-size: 0.7rem;}
  .small{font-size: 0.6rem;}
</style>