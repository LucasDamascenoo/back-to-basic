# back-to-basic
Repositório para anotações e pratica de conceitos front-end.


## Seletores
Seletores é como "selecionamos" o que queremos modificar em nosso HTML. Cada tipo de seletor tem uma especifidade diferente.

- Tags (H1,Image,Ul,a)

- classes e Ids (.name - #name)

Os seletores acima são os mais basicos que podemos usar.

Avançando um pouco mais.

- Seletores multiplos  (h1,h2,p)
- Seletores aninhado (.name p)


## Fontes
Podemos fazer alterações no tamanho da fonte, estilizar a fonte, mudar o tema , o espaçamento de cada letra entre outras.

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

* color

```css:
body {
  background:  #fff;
  }
```
* Imagem

```css:
div {
  background: url(./destino_da_foto) no-repeat 
  center center/cover;
  }
```
Na imagem podemos usar alguns atributos para mudar a forma que a imagem aparecem.

* <b>Url</b>: é o caminho da onde vamos incluir a imagem.
* <b>no-repeat</b>: estamos configurando para que a imagem não quebre em varias imagens.
* <b>center center</b>: é a forma de alinha a imagem no eixo horizontal e vertical.
* <b>cover</b>: é para que a imagem "cubra" toda o espaço diponivel na tela.


## Box-model

É o modelo "caixa" que todo nossos elementos possuem.



![box-model](/src/img/box-model.png)

* <b>Content</b>: é conteudo que foi atribuido dentro daquela caixa.
* <b>Padding</b>: é o espaçamento interno entre o conteudo e a borda.
* <b>Border</b>: é a borda que por padrão não apare.
* <b>Margin</b>: é o espaçamento interno entre uma "caixa" e outra.

Ao adicionamos Borda e Padding , nossa baixa aumenta o tamanho.Para manter o tamanho definido usamos a propriedade: <b>box-sizing</b>.

## Flex-box
Flex-box é usado para manipular os elementos de forma mais facil para criação de Layouts.

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

é uma propriedade abreviada para  : Flex-direction +  flex-wrap.

```css:
.container {
  flex-flow: column wrap;
}
```

## Justify-content

Define o alinha  o espaçamento mento do eixo horinzontal (principal) de acordo com o tamanho do elemento.

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





