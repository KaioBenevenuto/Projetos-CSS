# Introdução font-properties
A tipografia transmite uma mensagem, por exemplo, quando queremos dar uma ênfase no texto nós podemos escrever o mesmo em negrito.

Nós podemos transmitir uma mensagem diferente dependendo do estilo que escrevemos o texto.

Algumas das propriedades de fonts do CSS que podem nos ajudar a transmitir uma mensagem através dos textos da página são:

- font-family
- font-weight
- font-style
- font-size
<!------------------------------------------------------------------------------------>
## Font Family
Tipo de fonte de um elemento<br>
Lista de fontes e ordem de prioridade<br>
inclui fallback font<br>
```
p {
  font-family: "Times New Roman", Times, serif;
}
```
Alguns tipos de fonts:

serif (com serifa)<br>
<img src="../Imagens/image-12.png">

sans-serif (sem serifa)<br>
<img src="../Imagens/image-13.png">
<!------------------------------------------------------------------------------------>

## Font Weight
Peso da fonte<br>
Valores: `normal` | `bold` | `bolder` | `lighter` | `100` | `200` | `300` | `400` | `500` | `600` | `700` | `800` | `900`<br>
Dependendo da família da fonte não conseguimos utilizar todos os pesos de fonte
```
p {
	font-weight: bold;
}
```
<b>Referência</b><br>
https://www.w3.org/TR/css-fonts-3/
<!------------------------------------------------------------------------------------>

## Font Style
É o estilo da fonte<br>
Valores: `normal` | `italic` | `oblique`<br>
Os valores que podem ser aplicados dependem da fonte usada<br>
```
span {
	font-style: italic;
} 
```
<!------------------------------------------------------------------------------------>
## Font Size
Tamanho da fonte
```
p {
	font-size: 18px;
}
```
<!------------------------------------------------------------------------------------>
## Web Fonts
### Fontes do sistema x Fontes da web
Fontes do sistema são as fontes que estão instaladas na máquina do usuário e nem sempre o cliente vai ter instalado as fontes usadas no projeto e isso pode fazer com que os estilos dos textos não sejam aplicados corretamente, mas para resolver esses casos podemos preparar nossas fontes para web ou usar as fontes da web.

### Como usar fontes da web?

- @font-face
- @import
- link

<b>Referência</b><br>
https://fonts.google.com/ 

https://css-tricks.com/snippets/css/using-font-face-in-css/
<!------------------------------------------------------------------------------------>

## Font Variant

Faz variações na apresentação da fonte
```
p {
	font-variant: small-caps;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant
<!------------------------------------------------------------------------------------>
## Font Stretch
Alargamento ou encolhimento da fonte<br>
Aceita palavras-chaves como: `expanded` | `condensed` | `normal`<br>
Aceita porcentagens de 50% a 200%<br>
Essa propriedade não vai funcionar em todas as fontes<br>
```
p {
	font-stretch: expanded;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/font-stretch

<b>Referência</b><br>
https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals
<!------------------------------------------------------------------------------------>

## Letter spacing
Define o espaçamento entre os caracteres
```
p {
	letter-spacing: 4px;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing
<!------------------------------------------------------------------------------------>
## Word spacing
Define o espaçamento entre palavras
```
p {
	word-spacing: 1em;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/word-spacing
<!------------------------------------------------------------------------------------>
## Line height
Define os espaços entre linhas<br>
Pode ser com unidades ou sem unidades de medida<br>
Valores comuns: 1.5 ou 2<br>
```
p {
	line-height: 1.5;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/line-height
<!------------------------------------------------------------------------------------>
## Text transform
Transformação do texto<br>
Valores podem ser: `none` | `capitalize` | `uppercase` | `lowercase` | `full-width` | `full-size-kana`<br>
```
p {
	text-transform: uppercase;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform
<!------------------------------------------------------------------------------------>
## Text decoration
Aparência decorativa de um texto<br>
line: `underline` | `overline` | `line-through`<br>
podemos aplicar mais de 1 valor<br>
style: `wavy` | `dotted` | `double` | `dashed` | `solid`<br>
color: `<color>` values<br>
```
h1 {
	text-decoration: underline; 
}

p {
  text-decoration: wavy overline blue; /* shorthand */
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration
<!------------------------------------------------------------------------------------>
## Text align
Alinhamento de um texto<br>
Valores: `start` | `end` | `left` | `right` | `center` | `justify` | `match-parent`<br>
```
p {
	text-align: center;
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/text-align
<!------------------------------------------------------------------------------------>
## Text shadow
Sombra aplicada a um texto<br>
Permite múltiplos valores<br>
```
p {
  text-shadow: 1px 1px 1px red,
	       2px 2px 1px green; /* offset-x(deslocamento-x) | offset-y | blur-radius(raio de desfoque) | color */
}
```
https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow
<!------------------------------------------------------------------------------------>
## Shorthand

Podemos usar o shorthand `font` para determinar os seguintes valores: `font-style`, `font-variant`, `font-weight`, `font-stretch`, `font-size`, `line-height` e `font-family`
```
p {/* -style, -variant, -weight, -stretch, -size, /, -height e -family. */	
  font: italic normal bold normal 3em/1.5 Helvetica, Arial, sans-serif;
}
```