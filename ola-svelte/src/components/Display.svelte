<script lang="ts">
  export let valor: string

</script>

<div class="display">
  <span>{valor}</span>
</div>

<style>
  .display{
    display: flex;
    flex: 1;
    justify-content: flex-end;
    align-items: center;
    padding: 0px 5px;
    font-size: 1.5rem;
    background-color: aliceblue;
    overflow: hidden;
  }
</style>