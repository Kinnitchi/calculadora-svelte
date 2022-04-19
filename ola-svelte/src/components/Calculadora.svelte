<script lang="ts">
import CalculadoraModel from "../model/CalculadoraModel";

  import Botao from "./Botao.svelte";
  import Display from "./Display.svelte";
  import Linha from "./Linha.svelte";

  let calc = new CalculadoraModel()
  const numeroDigitado = (num: string) => calc = calc.numeroDigitado(num)
  const operacaoDigitada = (op: string) => calc = calc.operacaoDigitada(op)
  const pontoDigitado = () => calc = calc.pontoDigitado()
  const calcular = () => calc = calc.calcular()
  const limpar = () => calc = calc.limpar()
</script>
<div class="calculadora">
  <Display valor={calc.valor}/>
  <Linha>
    <Botao operacao triple texto="AC" onCLick={limpar}/>
    <Botao operacao  texto="/" onCLick={operacaoDigitada}/>
  </Linha>
  <Linha>
    <Botao texto="7" onCLick={numeroDigitado}/>
    <Botao texto="8" onCLick={numeroDigitado}/>
    <Botao texto="9" onCLick={numeroDigitado}/>
    <Botao operacao texto="*" onCLick={operacaoDigitada}/>
  </Linha>
  <Linha>
    <Botao texto="4" onCLick={numeroDigitado}/>
    <Botao texto="5" onCLick={numeroDigitado}/>
    <Botao texto="6" onCLick={numeroDigitado}/>
    <Botao operacao texto="+" onCLick={operacaoDigitada}/>
  </Linha>
  <Linha>
    <Botao texto="1" onCLick={numeroDigitado}/>
    <Botao texto="2" onCLick={numeroDigitado}/>
    <Botao texto="3" onCLick={numeroDigitado}/>
    <Botao operacao texto="-" onCLick={operacaoDigitada}/>
  </Linha>
  <Linha>
    <Botao duplo texto="0" onCLick={numeroDigitado}/>
    <Botao texto="," onCLick={pontoDigitado}/>
    <Botao destaque texto="=" onCLick={calcular}/>
  </Linha>
</div>

<style>
  .calculadora{
    display: flex;
    flex-direction: column;
    padding: 10px;
    border-radius: 2px;
    height: 80%;
    width: 20%;
    border: 1px solid #ffffff77;
    background-color: var(--bg);
  }
</style>