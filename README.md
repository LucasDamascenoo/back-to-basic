# back-to-basic
Repositório para anotações e pratica de conceitos front-end.

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





