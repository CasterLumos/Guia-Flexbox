# align-content #

Os sapos estão espalhados por toda a lagoa, mas as vitórias-régias estão agrupadas no topo. Você pode usar align-content para definir como múltiplas linhas devem ser espaçadas uma das outras. Essa propriedade recebe os seguintes valores:

- flex-start: Linhas são agrupadas no topo do container.
- flex-end: Linhas são agrupadas no fundo do container.
- center:Linhas são agrupadas no centro vertical do container.
- space-between: Linhas são posicionadas com espaço igual entre elas.
- space-around: Linhas são posicionadas com espaço igual em torno delas.
- stretch: Linhas se esticam para preencher o container.

Isso pode ser confuso, mas align-content determina o espaçamento entre linhas, enquanto align-items determina como as linhas como um todo são alinhadas dentro do container. Quando há só uma linha, align-content não tem nenhum efeito.

## Soluções ##

### Nível 21 ###

`align-content: flex-start;`

### Nível 22 ###

`align-content: flex-end;`

### Nível 23 ###

`flex-direction:column-reverse;`
`align-content: center`

### Nível 24 ###

`flex-flow: column-reverse wrap-reverse;`
`justify-content: center;`
`align-content: space-between`
