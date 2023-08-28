# ------------- Anatomia do CSS -------------
```
h1 {
	color: blue;
	font-size: 60px;
	background: gray;
}
```
Os elementos do CSS são:

- Selectors: Nesse caso o h1, que vai buscar no HTML a tag h1 e aplicar as mudanças.
- Declaration: As chaves e tudo dentro delas.
- Properties: As coisas a serem alteradas.
- Property values: Os novos valores que estamos atribuindo a tais propriedades.


# -------------------- Selectors 

Os seletores são o que conectam um elemento HTML com o CSS, existem vários tipos, 
sendo eles Element/Type selector(h1, p, div...), o seletor global, que é um * (asterisco), 
ID selector, que é # (cerquilha, cardinal) e o ID do elemento HTML, class selector, 
que é um . (ponto) e o nome da classe, e mais alguns que podemos entender mais tarde no curso.

Os seletores que mais usaremos serão realmente apenas os anteriormente citados, e vamos 
entrar em exemplos de como usá-los:

HTML
```
	<div id="container" class="m-40">
		<h1>Título</h1>
		<h2>Subtitulo</h2>
	</div>
```

CSS<br>
ID selector:
```
	#container {
		width: 200px;
	}
```

Class selector:
```
	.m-40 {
		margin: 40px;
	}
```

Element/Type selector + Agrupamento de seletores:
```
	h1, h2 {
		color: blue;
		font-size: 60px;
		background: gray;
	}
```

# -------------------- Box model

O CSS trabalha com a ideia de caixas, ou seja, o box model. Mas o quê exatamente 
é esse box model? É uma caixa retangular. Essa caixa possui as mesmas propriedades 
de uma caixa 2D, e tem como propriedades:

- Tamanho (largura x altura): width e height, respectivamente
- Conteúdo: o content
- Bordas: o border
- Preenchimento interno: o padding
- Espaços fora da caixa: a margin

Quase todo elemento de uma página é considerado uma caixa: Posicionamentos, tamanhos, 
espaçamentos, bordas, cores, então, em suma, elementos HTML são caixas, assim como quase tudo no CSS.
