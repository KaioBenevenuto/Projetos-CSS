# Page Layout
Alguns dos métodos usados para posicionar os elementos na tela.

- Tables
- Floats e clear
- Frameworks e Grid Systems
- Flexbox
- Grid

## Posicionamentos
Controla onde, na página, o elemento irá ficar, alterando o fluxo normal dos elementos.

Name: <code>position</code><br>
Value: <code>static</code> | <code>relative</code> | <code>absolute</code> | <code>fixed</code><br>

Lembrando que o fluxo normal dos elementos é ficar um abaixo do outro, a não ser no caso de elementos inline, que ficam um ao lado do outro.

### Static
Por padrão os elementos são <code>static</code>. Isso significa que os elementos irão seguir o fluxo normal do HTML.

### Relative
O <code>position</code> indica onde o elemento vai ser posicionado na página. Ao usar o <code>position</code> podemos adicionar outras propriedades como <code>top</code>, <code>right</code>, <code>bottom</code>, <code>left</code> e <code>z-index</code>, que vão determinar o posicionamento final do elemento.

Quando o <code>position</code> é <code>relative</code> os elementos são deslocados do seu posicionamento normal, mas sem afetar o posicionamento de outros elementos da página.

### Absolute
Quando o <code>position</code> é <code>absolute</code> o elemento é deslocado saindo do fluxo normal. O elemento de <code>position absolute</code> é posicionado em relação ao seu parent element mais próximo. Se esse elemento "pai" não existir, ele será posicionado em relação ao bloco contendo a raiz do elemento.

### Fixed
Quando aplicado o <code>position fixed</code> é como se criasse um elemento flutuante que fica fixo na página, independente do scrolling feito.

### Element Stacking
É o empilhamento de elementos. Podemos usar o <code>z-index</code> para determinar a ordem da posição do elemento. Quanto maior o <code>z-index</code>, mais "acima" vai aparecer o elemento.

## Flexbox
- Nos permite posicionar os elementos dentro da caixa<br>
- Controle em uma dimensão (horizontal ou vertical)<br>
- Alinhamento, direcionamento, ordenar e tamanhos<br>

```
    div.parent {
        display: flex;
    }
```

### Flex-direction
Qual a direção do <code>flex</code>: horizontal ou vertical<br>
<code>row</code> | <code>column</code>

### Alinhamento

<code>justify-content</code><br>
<code>align-items</code>

## Grid
- Posicionamento dos elementos dentro da caixa
- Posicionamento vertical e horizontal ao mesmo tempo
- Pode ser flexível ou fixo
- Cria espaços para os elementos filhos habitarem