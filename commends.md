#comentarios


/* No CSS podemos fazer comentário sem que ele afete nosso códio.

* Esses comentários ajudam a lembrar o que é o bloco de códigos  e o que estamos fazendo.

* Nos comentários também podemos deixar dicas para leitura e também ajudar os outros a entenderem o que você está fazendo.

* Nunca esqueça de fechar um comentário

comentários começam com '/*' e terminam com '*/'. 

os comentário também pode ser usado para desasbilitar partes do meu codigo.

# Anatomia

````css

h1 {color: blue;
Font-size: 60px;
background: gray}

````

* Selector - função que vai selecionar a tag que eu quero configurar ex: <h1>

Ele serve para conectar um HTML com o CSS.

## Tipos

* Global Selector: `*`
* Element/Type selector `h1, h2, p, div`
* ID Selecto `#box, #container`
* Class Selector `.red, .m-a`
* Atribute selector, Pseudo-class, Pseudo-element, e outros.

* Declaration - é TODO conteudo a ser configurado como color, font-size e background.

*Propeties - é CADA itém a ser declarado como color, fron-size etc.

Property Value - é o valor aplicado a propriedade como red, blue, 60px etc.


O Css trabalha com ideias de modelos de caixas (Box model) ou seja caixa retangular e e essascaixas possuem as mesmas propriedades que uma caixa 2D elas São:

    *Tamanho (largura x altura [width x heiht])
    * Conteúdo (content)
    * Bordas (border)
    * Preenchimento interno (padding)
    * Espaços fora da caixa (margin)

Quase todo elemento de uma pagina é considerado uma caixa: Posicionamento, tamanho, espaçamento, bordas, cores, enfim todos os elementos HTML são caixas, assim como quase tudo no CSS.


# a cascata (cascading)

é a escolha do browser de qual regra ele vai aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima pra baixo: Ou seja sempre a ultima regra é a que vai ser aplicada á pagina.

* Também é levado em considerção três fatores:

1. A origem do estilo
2. Especificidade
3. Importancia.

Se houver duas tag color iguais com cores diferentes ele va usar sempre a ultima tag colocada.

Se houver uma tag inline como: <h1 style: color> e outra tag apenas <h1 color:> ele vai usar a opção que tem stye independente da ordem dos fatores pois essa tag dentro do h1 é a mais forte.

Se houver <style:color> e <h1:color>
Também a tag Style é a que tem mais força.

Se houver <h1 style:color> e <style:color> a que tem h1 pois a tag inline é sempre a mais forte. 

ou seja a origem de estilo é sempre

inline> tag style > tag link

Se não houver essa diferença e todas as tags forem iguais, a ultima a ser configurada será a sempre a que irá sair na pagina.

### Epecificidade


É um calculo matemático, onde, cada tipo de seletor e origem do estilo possuem valores a serem considerados.

0. Iniversal selector, combinators e negation pseudo-class (:not()) Significa força zero e que qualque outro elementos pode passar por cima dessa configuração no CSS.

1. Element type selector e pseudo-elements (::before, ::after) possui força 1 então quando houver duas configurações pelo mesmo elemento entre uma universal por exmplo e e elemnt type, pelos calculos 1 é maior que zero entõa a configuração regente é a do element type selector.

10. Classes e atribute selectors {[type="radio"]} (geralmente usase a tag class)

100. ID selector

1000. Inline a mais forte de todas.


### A regra important

* cuidado, evite o uso
* Não é considerado uma boa prática
* Quebra o fluxo natural da cascata.
* Ela sobreescreve todas as forças das tag.
*deve ser usado em ultimo caso.

# At-rules

* Está relacionado ao comporamento do CSS
* começa com o sinal de `@` seguido do identificador e valor.


## exemplos comuns

-@import       /*incluir um CSS externo*/

``` @import ("http://local.com/style.css) ``` 

ou

``` @import url("http://local.com/style.css)```


- @media      /* regras adicionais para dispositivos*/

@media (min-with: 500px) {colocar o link da midia}

- font - face  /* fontes externas */

@font-face {/*colocar as regras aqui */}

- key frames  /* animações*/

@keyframes nameofanimation {/*colocar as regras das aniações aqui*/}


# shorthand

*horthand são junção de propriedades do css

* Através do shorthand você consegue por diversas propriedades de maneira resumida e bem mais legivel.

Exemplos

``` CSS {
    /* background properties */

    background-colo: #000;
    background-image: url(imaged/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

/* background shorthand*/

background: #000 url (images/bg.gif) no-repeat left top

/*font properties*/
 
font-style: italic;
font-weight: bold;
font-size: 8em;
line-height: 1.2;
font-family: Arial, sans-serif;

/* font shothand */

font: italic bold . 8em/1.2 Arial, sans-serif;
  /*shorthand sobrepo~es a todas propriedades anteriores*/
}```


## Detalhes

* Não irá considerar propriedades anteriores.
* Valores não especificados irão assumir o valor padrão.
* geralmente, a ordem descrita não importa, mas se houver muitas propriedades com valores semelhantes, podemos encontrar problemas.


## propriedades que aceitam short-hand

Animation, -background, border, border-bottom, border-color, border-left, border-radius, border-right, border-style, border-top, boder width, column-rule, colums, flex, flex-flow, font, grid, grid-area, grid-column, grid-row, grid-template, list-style, margin, offset, outline, overflow, padding, place-content, place-items, place-self, text-decoration, transition.


Quando for usar o shothand deve entrar no site.

**https://developer.mozila.or/en-US/docs/web/css/shorthand_properties**


e pesquisar quaid propriedades aceitam o shorthand.

# Funções

* Nome seguido de abre e fecha parenteses
*recebe um argumento

## exemplos

``` css

@import url("http:://urlaqui.com/style.css");

{
    color: rgb (255, 0 , 100)
    width: calc (100% - 10%)

}
```

Devtools - ferremanta muito utilizada para desenvolvedores. 


# Margin

*margim, é o espaço (margem) entre os elementos.

*podemos dividir o margin em 4 valores:

/* margin-top / margin-right / margin-botton / margin-left*/

* Os valores utlizados são:

    - Values: <length> / <percentage> / auto.

    *geralmente usamos uma forma abreviada (shorthand) para escrever o margin. Esse formato segue o sentido horário iniciando pelo TOP, seguindo para RIGHT, BOTTOM e LEFT.


margim: 12px 16px 10px 4px; /* top right bottom e left respectivamente*/


margim: 12px 16px 0 /* top , right and left, bottom respectvamente */

Margim: 8px 16px /* top and bottom , right and left respectivamente */

Margim: 8px; /* a mesma margem para todos os lados*/

* O margim é aplicado em elementos com display block

* Cuidado com o margim collapsing que é quando o top se junta ao bottom.


## padding

O paddinf tem as mesmas propriedades que o margim a diferença entre um e outro é que o margim configura a posição externa da caixa (onde a caixa vai ficar na pagina) e o padding configura a posição interna da caixa (onde o texto dentro da caixa vai ficar em relação a caixa)


## border

São as bordas da caixa:

        - Value: <border-style> / <boder-width> / <border-color>
        - style: solid / dotted / dashed / double / groove / ridge / inset / outset.
        -width: <length>
        - color: <color>

```css

div{ /*shorthand*/} border-top: solid 2px; /* top / right/ /bottom/ left*/

/*style*/
border: solid;

/*width <length> / style */
border : 2px dotted;

/* style /color */
border: outser #f33

/*width / style / color*/

border: medium dashed green;

