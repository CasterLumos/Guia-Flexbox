# flex-direction #

Os sapos precisam ficar na mesma ordem das vitórias-régias usando <u>flex-direction</u>. Esta propriedade CSS define a **DIREÇÃO DO POSICIONAMENTO** no container e aceita os seguintes valores:

- row: Itens são posicionados na **MESMA DIREÇÃO** do texto.
- row-reverse: Itens são posicionados na **DIREÇÃO OPOSTA** à do texto.
- column: Itens são posicionados de **CIMA PARA BAIXO**.
- column-reverse: Itens são posicionados de **BAIXO PARA CIMA**.

Note que quando **flex-direction: column;** o justify-content altera a vertical e align-items altera a horizontal.

## Soluções ##

### Nível 8 ###

`flex-direction: row-reverse;`

### Nível 9 ###

`flex-direction:column;`

### Nível 10 ###

`flex-direction: row-reverse;`

`justify-content: flex-end;`

### Nível 11 ###

`flex-direction: column;`

`justify-content: flex-end;`

### Nível 12 ###

`flex-direction: column-reverse;`

`justify-content: space-between;`

### Nível 13 ###

`flex-direction: row-reverse;`

`justify-content: center;`

`align-items: flex-end`
