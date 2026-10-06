# Simulador de padrão de vida

Ferramenta web de uma página que mostra quanto a pessoa precisa acumular para manter o padrão de vida depois que parar de trabalhar, e leva o visitante ao diagnóstico gratuito.

**Demo:** https://gustavo4157.github.io/simulador-vertex/

## O que faz

- Pergunta idade, idade para parar de trabalhar, renda mensal desejada, patrimônio atual, aporte mensal e retorno real ao ano.
- Calcula o patrimônio necessário, a projeção com o aporte atual e o aporte mensal necessário.
- Mostra se o plano fecha e quanto falta, com barra de progresso.
- Gera um card em imagem (1080x1350) para o visitante postar nos stories.
- O botão "Agendar diagnóstico gratuito" leva ao formulário do site.

## Como usar

Não precisa instalar nada. Abra o `index.html` no navegador (ou use a extensão Live Server do VS Code).

## Como personalizar

No começo do `<script>` do `index.html` há um bloco `CONFIG`:

```js
const CONFIG = {
  marca: "VERTEX CAPITAL",
  diagnosticoUrl: "https://www.vertexcapitalbr.com.br/",
  idadeFinal: 90
};
```

- `marca`: nome exibido no topo e no card.
- `diagnosticoUrl`: link do botão de diagnóstico.
- `idadeFinal`: até que idade a renda deve durar.

As cores ficam no bloco `:root` no começo do CSS.

## Como colocar no Instagram e no site

- **Instagram:** use o link da página na bio ou na figurinha de link dos stories.
- **Site:** publique como página própria ou incorpore com:

```html
<iframe src="LINK-DO-SIMULADOR" style="width:100%;height:900px;border:0" title="Simulador"></iframe>
```

- **Medir resultados:** acrescente um marcador ao link, por exemplo `?origem=insta`, e compare com os diagnósticos agendados.

## Como o cálculo funciona

Tudo em valores de hoje (já descontada a inflação). O patrimônio necessário é o valor presente da renda desejada, paga mensalmente da idade escolhida até `idadeFinal`, com o retorno real informado. A projeção soma o patrimônio atual e os aportes mensais capitalizados até a idade escolhida. Não considera INSS, impostos, taxas nem renda variável.

## Aviso

Simulação educativa. Não é recomendação de investimento.

## Tecnologias

HTML, CSS e JavaScript puro, sem dependências nem servidor.

## Autor

[Gustavo Santos]
