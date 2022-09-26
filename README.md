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

Define o alinhamento do eixo vertical de acordo com o tamanho do elemento.

```css:
.container {
  .container {
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
}
}
```

## align-content

Define o espaçamento dos elementos (em bloco) quando existem muitos (é necessario que sempre aja a quebra de linha flex-wrap).
