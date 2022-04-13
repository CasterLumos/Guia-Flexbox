# Guia Flexbox #

O Flexbox é um conjunto de propriedades que tem por objetivo organizar itens dentro de um elemento pai, normalmente chamado de container.

## display ##

O primeiro passo para utilizar o Flexbox é definir a propriedade display do elemento pai com o valor flex.

~~~css
.container {
     display: flex;
}
~~~

## justify-content ##

A propriedade justify-content define o alinhamento dos itens ao longo do eixo principal do container, que por padrão é horizontal.

~~~css
.container {
     display: flex;
     justify-content: [flex-start/flex-end/center/space-between/space-around];
 }
~~~

- flex-start (padrão): Os itens são alinhados a partir do começo do eixo principal;
- flex-end: Os itens são alinhados a partir do final do eixo principal;
- center: Os itens são alinhados ao centro do eixo principal;
- space-between: O primeiro item é deslocado para o início do eixo principal, o último é deslocado para o final do eixo principal e os demais são distribuídos uniformemente entre eles;
- space-around: Os itens são uniformemente distribuídos ao longo do eixo principal. Aqui, porém, são atribuídas margens iguais à esquerda e à direita (ou acima e abaixo, dependendo da direção do eixo principal). Por isso o primeiro e o último item não ficam “colados” nas bordas do container.

## align-items ##

Essa propriedade define como os itens são distribuídos ao longo do eixo transversal do container, que por padrão é vertical.

~~~css
.container {
  display: flex;
  align-items: [stretch/flex-start/flex-end/center/baseline];
 }
~~~

- stretch (padrão): Os itens serão esticados para preencher toda a dimensão do eixo transversal (altura ou largura);
- flex-start: Os itens são deslocadas para o início do eixo transversal;
- flex-end: Os itens são deslocadas para o final do eixo transversal;
- center: Os itens são centralizados no eixo transversal;
- baseline: Os itens são alinhados a partir da base da primeira linha de texto de cada um.

## flex-direction ##

flex-direction define o eixo/fluxo de exibição em que os elementos serão organizados. Veja um exemplo [aqui](https://github.com/CasterLumos/Guia-Flexbox/tree/master/Flexbox%20Froggy/08-13-flex-direction)

~~~css
.container {
     display: flex;
     flex-direction: [row / row-reverse / column / column-reverse];
}
~~~

- row (padrão): Os itens são organizados em forma de linha da esquerda para a direita;
- row-reverse: Os itens são organizados em forma exibição em linha da direita para a esquerda;
- column: Os itens são organizados em forma de colunas iniciando de cima para baixo;
- column-reverse: Os itens são organizados em forma de colunas iniciando de baixo para cima.

## order ##

A propriedade order é uma sub-propriedade do módulo FlexBox. Os itens Flex são exibidos na mesma ordem em que aparecem no documento de origem por padrão. A propriedade order pode ser usada para alterar esta ordenação.

~~~css
.container {
    .item2 {
        order: [número];
    };
}
~~~

## align-self ##

A propriedade align-self é uma sub-propriedade do módulo Flexbox. Ela torna possível a anulação do valor do align-items para  itens flexíveis específicos.

~~~css
.item2 {
     align-self: [auto/stretch/flex-start/flex-end/center/baseline];
}
~~~

- auto (padrão): Respeita o comportamento definido no container por meio do align-items;
- stretch: O item será esticado para preencher toda a dimensão do eixo transversal (altura ou largura);
- flex-start: O item é deslocado para o início do eixo transversal;
- flex-end: O item é deslocado para o final do eixo transversal;
- center: O item é centralizado no eixo transversal;
- baseline: O item é alinhado a partir da base da primeira linha de texto dos demais.

## flex-wrap ##

Ela define se os itens flexíveis são forçados em uma única linha ou se podem ser enviados em várias linhas. Se definido para múltiplas linhas, ele também define o eixo transversal que determina a direção na qual as novas linhas são empilhadas.

Lembrete: o eixo transversal é o eixo perpendicular ao eixo principal. Sua direção depende da direção do eixo principal.

~~~css
.container {
     display: flex;
     flex-wrap: [nowrap / wrap / wrap-reverse];
}
~~~

- nowrap (padrão): Todos os itens serão dispostos em uma linha;
- wrap: Ocorrerá a quebra de linha e os itens mais à direita serão deslocados para a linha de baixo;
- wrap-reverse: Ocorrerá a quebra de linha e os itens mais à direita serão deslocados para a linha de cima;

## flex-flow ##

É uma abreviatura para flex-direction e flex-wrap.

~~~css
.container {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    ou 
    flex-flow: column wrap;
}
~~~

## align-content ##

Ele ajuda a alinhar as linhas de um contêiner quando há espaço extra no eixo transversal, de forma semelhante a como o justify-content alinha os itens individuais dentro do eixo principal.

Note que esta propriedade não tem efeito quando a caixa flexível tem apenas uma única linha. A propriedade flex-wrap:wrap deve estar definida.

~~~css
.container {
     display: flex;
     align-content: [stretch/flex-start/flex-end/center/space-between/space-around];
 }
~~~

- stretch (padrão): As linhas são distribuídas uniformemente ao longo do eixo transversal, ocupando todo o espaço disponível;
- flex-start: As linhas são distribuídas a partir do início do eixo transversal;
- flex-end: As linhas são distribuídas a partir do fim do eixo transversal;
- center: As linhas são mantidas no centro do eixo transversal;
- space-between: A primeira linha é deslocada para o início do eixo transversal, a última é deslocada para o final do eixo transversal e as demais são distribuídas uniformemente entre eles;
- space-around: As linhas são uniformemente distribuídas ao longo do eixo transversal. Aqui, porém, são atribuídas margens iguais à esquerda e à direita (ou acima e abaixo, dependendo da direção do eixo transversal). Por isso a primeira e a última linha não ficam “coladas” nas bordas do container.

## Conclusão ##

Existem outras propriedades porém são para contextos especificos, as aqui aprensentadas são  mais utilizadas e com uma generalização maior. Recomendo fortemente que você jogue o Flexbox froggy pois ele dará uma noção muito aprofundada do que é cada propriedade na prática.
