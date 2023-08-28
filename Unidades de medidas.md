# ------------------------- Introdução 

Veremos agora sobre valores e unidades de medidas no CSS e como podemos usar a documentação do MDN para aprender mais.

## Valores e unidades de medidas

Cada propriedade possui valores `property: value`<br>
Como conhecer e estudar os valores na documentação?<br>

`<color> <length>`<br>

Os termos podem variar values ou data types
Documentação MDN: https://developer.mozilla.org/en-US/

# ------------------------- Tipos numéricos e unidades comuns 

Veremos Agora algumas unidades de medida do css.

## Tipos numéricos:

`<integer>` - número inteiro como -10 ou 223<br>
`<number>` - número decimal como -2.4, 64 ou 0.234<br>
`<dimension>` - é um ```<number>``` com uma unidade junto: 90deg, 2s, 8px<br>
`<percentage>` - representa uma fração de outro número: 50%


## Unidades comuns:

`<length>` - é um dos mais usados no CSS e representa um valor de distância: px(pixels), em, vw<br>
`<angle>` - representa um ângulo: deg(graus), rad(radiano), turn(360° graus)<br>
`<time>` - representa um tempo: s(segundos), ms(milissegundos)<br>
`<resolution>` - representa resoluções para dispositivos: dpi

# ------------------------- Distâncias absolutas e relativas 

## Distâncias absolutas <length>

São fixas e não alteram seu valor.

| Unidade  | Nome                | Equivalência                     |
|----------|---------------------|----------------------------------|
| cm       | Centímetros         | 1cm = 96px/2.54                  | 
| in       | Inches (polegadas)  | 1in = 2.54cm = 96px              | 
| px       | Pixels              | 1px = 1/96 avos de uma polegada  |

*o mais comum e mais utilizado é o px<br>
*não é recomendado usar cm

## Distâncias relativas

São relativas a um outro valor, pode ser o elemento pai, ou root, ou o tamanho da tela.<br>
Benefício: Maior adaptação aos diferentes tipos de tela.

| Unidade  | Relativo a                                    |
|----------|-----------------------------------------------|
| em       | Tamanho da font do elemento pai               |
| rem      | Tamanho da font do elemento raiz (root/html)  | 
| vw       | 1% da viewport wid (largura)                  |  
| vh       | 1% da viewport height (altura)                |

Normalmente o tamanho da font padrão do navegador é de 16px e para mudar esse valor temos que fazer a alteração no root ou no elemento html.
```
:root {
	font-size: 18px;
}
```
/* OU */
```
html {
	font-size: 18px;
}
```
O viewport é a parte da tela que está sendo exibida.<br> 
No caso dos navegadores web, é o que é exibido na janela/tela do documento.<br> 
Conteúdos que estão fora do viewport só serão exibidos quando feito um scroll da área de visualização.

# ------------------------- Porcentagens 

As porcentagens são valores bem flexíveis.<br>
Em muitos casos é tratado da mesma maneira que as distâncias `<length>`.<br>
Sempre será relativo a algum valor.

💻 Exemplo
Relativo ao elemento pai

HTML
```
<ul>
	<li>One</li>
	<li>Two</li>
	<li>Three
		<ul>
			<li>Three A</li>
			<li>Three B</li>
				<ul>
					<li>Three B 2</li>
				</ul>
		</ul>
	</li>
</ul>
```

CSS
```	
li {
	font-size: 80%;
}
```
# ------------------------- Position 

`<position>`

Representa um conjunto de coordenadas 2D:<br>
top(canto superior), right(direita), bottom(canto inferior), left(esquerda) e center(centro).<br>
Usado para alguns tipos de propriedades como o background-position.<br>
Não confundir com a propriedade `position`.

# ------------------------- Funções 

Em programação, funções são reconhecidas por causar um reaproveitamento de código.
Exemplos de funções do CSS:

rgb()<br>
hsl()<br>
url()<br>
calc()

Dentro dos parêntesis são passados argumentos.<br>
Link da documentação do MDN: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Functions

# ------------------------- Strings e Identificadores 

Strings: texto envolto em aspas
```
.box::after {
	content: "Isso é uma string"
}
```
Identificadores: podemos ter nomes de cores como red, black, gold, dentre outros.