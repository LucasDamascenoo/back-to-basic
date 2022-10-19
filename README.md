# back-to-basic

Repositório para anotações e pratica de conceitos front-end.

## Seletores

Seletores é como "selecionamos" o que queremos modificar em nosso HTML. Cada tipo de seletor tem uma especifidade diferente.

- Tags (H1,Image,Ul,a)

- classes e Ids (.name - #name)

Os seletores acima são os mais basicos que podemos usar.

Avançando um pouco mais.

- Seletores multiplos (h1,h2,p)
- Seletores aninhado (.name p)
- Seletores de classe (.classe)
- Seletores de Ids (#id)
- Pseudo-classes (a:hover, a:clicked)

## Fontes

Podemos fazer alterações no tamanho da fonte, estilizar a fonte, mudar o tema , o espaçamento de cada letra entre outras.

- color
- font-size
- font-famaly
- text-tranform
- font-style
- line-height
- letter-spacing

```css:
p {
font-family: arial;
font-size: 1rem;
}
```

## Cores

Tambem podemos alterar as cores dos nossos elementos.

- name color (blue,red)
- hexa-decimal (#fff)
- rgb (256,234,20)
- rgba(256,242,21,0.7)

os 3 primeiros tipo de atributos,alteramos apenas a cor dos nosso elementos, já a ultima rgba altera alem das cores como a transparencia dessa cor.

## Background

A propriedade background altera o fundo do nosso site seja com cor ou com imagens.

- color

```css:
body {
  background:  #fff;
  }
```

- Imagem

```css:
div {
  background: url(./destino_da_foto) no-repeat
  center center/cover;
  }
```

Na imagem podemos usar alguns atributos para mudar a forma que a imagem aparecem.

- <b>Url</b>: é o caminho da onde vamos incluir a imagem.
- <b>no-repeat</b>: estamos configurando para que a imagem não quebre em varias imagens.
- <b>center center</b>: é a forma de alinha a imagem no eixo horizontal e vertical.
- <b>cover</b>: é para que a imagem "cubra" toda o espaço diponivel na tela.

## Unidades de Medidas

No css temos unidades de medidas absolutas e relativas.

<b>Absolutas</b>:

- px

Unidade de medida mais usada, porem ela é uma unidade que quando definida ela não se adapta ao layout da tela ou seja, sempre vai ter a largura ou a altura fixa em determinado valor.

<b>Relativas</b>:

São unidades que se adaptam ao navegador (viewport).

As mais usadas são.

- em e rem
- vh e vw
- %
- max and min

<b>Em e Rem</b>:

Em é uma medidas relativa referente ao pai.

```css:
 body  {
  font-size:10px;
  }

  h1 {
    font-size: 2em;
  }
```

No exemplo acima, defimos uma font-size padrão para nosso body de 10 px, já no H1, aplicamos um valor de 2em, ou seja 2x o valor do meu pai, que nesse caso será de 20px.

<b> Caso tenha um outro elemento que seja filho da propriedade de 20px e aplicamos 2em,agora esse filho terá 40px, pois herdou os 20px e não os 10px que definimos no primeiro pai</b>

Rem tambem é uma unidade de medida relativa mas ligada ao root, por padrão dos navegadores temos uma fonte de 16px.

Podemos alterar esse valor no root do nosso html, que é a tag html.

```css:
 html  {
  font-size:10px ou 62.5%;
  }

  h1 {
    font-size: 2rem;
  }
```

nesse caso nosso rem agora vale 2x 10px.

<b> Onde usar rem e onde usar em?</b>

Não tem uma regra 100% especifica, mas podemos usar rem para font-sizes e em para margin e padding.

- rem : font-size
- em : padding and margin

## Responsividade

Viewport : é uma meta tag com finalidade na tela útil dos navegadores, sem essa tag os elementos não se adequam corretamente no tamanho da tela.

definir widght em %
evitar hight por padding

min-width(600px) == 600px ou maior
max-width(500px) == 500px ou menor

se formos criar um layout mobile first, podemos usar min-widgt,
pois nosso layout sera feito primeiramente para telas menores,
apos isso, criamos para telas maiores.

a ordem que incluimos nossos breakpoint tambem importa,
então precisamos incluir sempre o breakpoint menor para o maior.

Breakpoints:

a ideia é evitar usar um monte de breakpoints, entao
precisamos "brincar" com nosso site e ver os tamanhos
que estão apresentando problema e arrumar o media query
atraves dessa resolucão.

Dicas :

Todo site é resposivo logo de inicio, se não é mais, fizemos algo errado.
Evitar tamanhos fixos

## Box-model

É o modelo "caixa" que todo nossos elementos possuem.

![box-model](/src/img/box-model.png)

- <b>Content</b>: é conteudo que foi atribuido dentro daquela caixa.
- <b>Padding</b>: é o espaçamento interno entre o conteudo e a borda.
- <b>Border</b>: é a borda que por padrão não aparece.
- <b>Margin</b>: é o espaçamento interno entre uma "caixa" e outra.

Ao adicionamos Borda e Padding , nossa caixa aumenta o tamanho.Para manter o tamanho definido usamos a propriedade: <b>box-sizing</b>.

Por padrão os navegadores já vem setado algumas medidas de margin e padding, para tirarmos esses valores podemos usar o reset css;

```css:
* //seletor universal {
  margin:0;
  padding:0;
  }
```

## Tipos de caixas

No HTML trabalhamos com 3 tipos de caixas:

- block
- inline
- inline-block.

Os elementos <b>block</b>(h1,div e etc) ocupam toda a largura da pagina, podemos atribuir largura e altura e quebram linha, ou seja o proxima elemento começa em baixo.

Os elementos <b>inline</b>(span,img,a) ocupam apenas a largura do conteudo, não é possivel atribuir altura e largura e os elementos ficam um ao lado do outro.

Já os elementos <b>inline-block</b> tem o mesmo comportamento do inline,mas "herda" as possiveis alterações do elementos em block, definir altura,largura,margem.

## Layouts

Quando falamos de Layouts temos 2 conceitos.

- Layout de pagina
- Layout de componentes

Onde o Layout é a pagina como um todo, o posicionamento dos elementos

e o compomentes são os "micros" designer que tambem precisam ser posionados dentro de suas caixas.

![layout-componentes](/src/img/Layout.PNG)

Temos 3 maneiras de manipular Layouts no css.

- Floats
- Flex-box
- Grids

## Floats

Float é uma maneira de manipular elementos (caindo em desuso) atraves de suas propriedades.

## Positions

Com a propriedades positions conseguimos mudar os elementos de acordo com as propriedades aplicadas.

- Static

é a propriedade padrão dos navegadores, ou seja renderiza na ordem que aparece no documento.

Não é possivel aplicar top e left.

- Relative

Muda o posicionamento relativamente a sua posição original(elemento sai do fluxo), ao mudarmos um elemento relativamente, o espaço "original" vai continuar reservado como se o elemento ainda estivesse ali.

![relative](../back-to-basic/src/img/Screenshot-1.png)

Podemos aplicar top e left

- Absolute

Muda o posicionamento de acordo com o pai (que não seja static) mais proximo, caso não exista ele movimenta o elemento de acordo com o body. elementos que estejam como absolute, sobrepoem outros elementos.

Podemos aplicar top e left

- Fixed

fixa a posição do elemento de acordo com a posição do navegador.

Podemos aplicar top e left

- Sticked

Movimenta o elemento de acordo com o scroll do mouse.

Podemos aplicar top e left

## Flex-box

Flex-box é usado para manipular os elementos de forma mais facil para criação de Layouts (de uma dimensão).

## Cheatsheet

![flex-box-cheatseat](./src/img/css%20tricks.jpg)

## o que acontece quando utilizamos a propriedades display-flex?

ao utilizarmos a propriedade display-flex, "criamos" dois conceitos:

- Container (Pai)
- Items (Filho direto)

Onde o container é a "caixa geral" dos conteudo e o conteudo interno é são os Items.

![Content:Container](/src/img/container.png)

![Content:Items](/src/img/flex-content.png)

# Propriedades que alteram o container

## flex-direction

Flex direction define em qual eixo vamos trabalhar os elementos, horizontal(row) ou vertical (columuns).

- Row/Linha (Padrão:Horizontal)
- Columns/Colunas (Vertical)

![Row-Columns](/src/img/row-columns.png)

```css:
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

## Flex-wrap

Flex-wrap difine se os items(flexiveis) vão quebrar de linha caso o conteudo ultrapasse o limite determinado.

![flex-wrap](/src/img/flex-wrap.png)

```css:
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

## Flex-flow

é uma propriedade abreviada para : Flex-direction + flex-wrap.

```css:
.container {
  flex-flow: column wrap;
}
```

## Justify-content

Define o alinha o espaçamento mento do eixo horinzontal (principal) de acordo com o tamanho do elemento.

![justify-content](/src/img/justify-content.png)

```css:
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;
}
```

## align-items

Define o alinhamento do eixo vertical (cross axis) de acordo com o tamanho do elemento.

![align-items](/src/img/align-items.png)

```css:
.container {
  .container {
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
}
}
```

## align-content

Define o espaçamento dos elementos (em bloco) quando existem muitos (é necessario que sempre aja a quebra de linha flex-wrap).

![align-content](/src/img/align-content.png)

# Propriedades que Alteram os Items

# order

Determina a ordem em que os elementos aparecerão.

![order](/src/img/order.svg)

Por padrão os flex items são dispostos na tela na ordem do código. Mas a propriedade order controla a ordem em que aparecerão no container.

```css:
.item {
  order: 5; /* default is 0 */
}
```

# align-self

Permite que o alinhamento padrão (ou o que estiver definido por align-items) seja sobrescrito para ítens individuais.

![align-self](/src/img/align-self.svg)

```css:
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

# flex-grow

Divide o espaço disponivel do container para os filho de forma igual

Se todos os ítens tiverem flex-grow definido em 1, o espaço remanescente no container será distribuído de forma igual entre todos. Se um dos ítens tem o valor de 2, vai ocupar o dobro de espaço no container com relação aos outros (ou pelo menos vai tentar fazer isso).

```css:
.item {
   flex-grow: <numero>; /* o valor default(padrão) é 0 */
```

Valores negativos não são aceitos pela propriedade.

# flex-shrink

Define a habilidade de um flex item de encolher, caso necessário.

Caso eu tenha um container com larura de 500px e 4 items de 250, ativando o shrink (1) faz com que os 4 items se ajustem(diminuam) para que caibam naquele container.

```css:
.item {
    flex-shrink: <número>; /* o valor padrão é 0 */
```

Valores negativos não são aceitos pela propriedade.

# flex basics

Define o tamanho padrão para um elemento antes que o espaço remanescente do container seja distribuído. Pode ser um comprimento (por exemplo, 20%, 5rem, etc) ou uma palavra-chave. A palavra-chave auto significa "observe minhas propriedades de altura ou largura" (o que era feito pela palavra-chave main-size, que foi depreciada). A palavra-chave content significa "estabeleça o tamanho com base no conteúdo interno do ítem" - essa palavra-chave ainda não tem muito suporte, então não é fácil de ser testada, assim como suas relacionadas: max-content, min-content e fit-content.

```css:
.item {
    flex-basis: flex-basis:  | auto; /* o valor padrão é auto */
```

# flex

Esta é a propriedade shorthand para flex-grow, flex-shrink e flex-basis, combinadas. O segundo e terceiro parâmetros (flex-shrink e flex-basis) são opcionais. O padrão é 0 1 auto, mas se você definir com apenas um número, é equivalente a 0 1.

```css:
.item {
    flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
```

<b>Flex: 0</b>; usamos para quando que nossos itens não ocupem todo os espaço do container(somente do seu proprio conteudo).

<b>Flex: 1</b>; é quando queremos que os items tenha a mesma distribuição dentro do container mesmo que seus conteudos sejam diferentes.
