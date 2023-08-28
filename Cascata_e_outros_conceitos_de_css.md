# ------------------------- A Cascata -------------------------

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.<br>
Seu estilo é lido de cima para baixo, ou seja, caso haja algum selector com informações 
conflitantes, o mais embaixo é o que será atribuído.<br>
São levados em consideração 3 fatores:

<b>A origem do estilo;</b>
 - inline > tag style > tag link

<b>A especificidade;</b>
 -  É um cálculo matemático, onde cada tipo de seletor e origem do estilo possuem valores 
    a serem considerados.

    0.Universal selector, combinators e negation pseudo-class(:not())<br>
    1.Element type selector e pseudo-elements(::before, ::after)<br>
    10.Classes e attribute selectors([type="radio"])<br>
    100.ID selector<br>
    1000.Inline

<b>A importância;</b>
 -  sintaxe: !important

    São raras as ocasiões nas quais se devem usar um iportant, pois é em geral 
    uma má pratica, visto que quebra o fluxo natural da cascata e pode acabar 
    te atrapalhando caso você a deixe em algum lugar no seu código.

    Portanto evite ao máximo seu uso.

# ------------------------- At-rules 

São regras relacionadas ao comportamento do CSS, começa com um sinal de @ seguido do identificador e do valor.<br>
São as seguintes:

@import serve para incluir um CSS externo.
```
 @import url("url do css que você quer importar");
```

@media são regras condicionais para vários dispositivos.
```
@media(min-width: 500px){
    *regras aqui
}
```
@font-face é para colocar fontes externas.
```
@font-face {
    *regras aqui
}
```
@keyframes serve para as animations do CSS.
```
@keyframes name_of_animation {
    *regras aqui
}
```
# ------------------------- Shorthand 

É basicamente a ideia de junção de propriedades, para que fiquem de forma resumida e legível.<br>
Abaixo um exemplo de propriedades com e sem o shorthand:
```
    - background properties -
    background-color: #000;
    background-image: url(images/bg.gif);
    background-repeat: no-repeat;
    background-position: left top;

    - background shorthand -
    background: #000 url(images/bg.gif) no-repeat left top;
```
```
    - font properties -
    font-style: italic;
    font-weight: bold;
    font-size: .8em;
    line-height: 1.2;
    font-family: Arial, sans-serif;

    - font shorthand - 
    font: bold italic .8em/1.2 Arial, sans-serif;
```

Algumas das características do shorthand:

- Não irá considerar propriedades anteriores, ou seja, caso faça um shorthand, apenas ele será considerado, 
quaisquer propriedades anteriores serão substituídas pelas do shorthand.

- Os valores que não forem especificados irão assumir o valor padrão.

- Por fim, geralmente, a ordem descrita não importa, mas, caso haja muitas propriedades com valores semelhantes, poderemos encontrar problemas.

# ------------------------- Funções 

*Nome seguido de abre e fecha parentesis<br> 
*Recebe argumento

exemplos:
```
@import url("http://urlaqui.com/style.css");
```
```
h1{
    color:rgb(255,0,100);
    width:calc(100% - 10px);
}
```
# ------------------------- Vendor prefixes 

São coisas que permitem que browsers adicionem features(características) a fim de colocar em uso alguma novidade que vemos no CSS.

```
-webkit-background-clip: text; / Chrome, Safari, iOS e Android /
-moz-background-clip: text;   / Mozilla (Firefox)             /
-ms-background-clip: text;   / Internet Explorer ou Edge     /
-o-background-clip: text;   / Opera                         /
```


Você também pode consultar se a feature pode ser utilizada através do site:

https://ireade.github.io/which-vendor-prefix
https://caniuse.com
