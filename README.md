# Curso-D3.js

D3 é uma biblioteca JavaScript para desenvolver representações gráficas. É muito usado para representação visual de dados.

A visualização de dados possui grande relevância nos meios informativos, dentre elas temos gráficos populacionais, mapas com representações sociopolíticas, linhas temporais históricas e muitas outras. O D3 é utilizado no mundo todo para criar as mais diversas representações por sua dinamicidade praticamente infinita. O D3 é de rápido processamento pois se trata de uma lib JS e por isso é interpretado pelos motores de JavaScript já utilizados pelos navegadores. 

Partindo do pressuposto de que a maioria das pessoas interessadas nesse conteúdo possui conhecimentos básicos sobre a linguagem JavaScript, iniciaremos este curso falando um pouco sobre SVG, que é o elemento HTML mais manipulado pelo D3, em seguida partiremos para o conteúdo de D3 propriamente dito.

SVG é uma linguagem XML e pode ser um tipo de elemento HTML, assim como body, p, table e tantos outros conhecidos por todo desenvolvedor web. Para usá-lo devemos abrir nosso documento HTML e inserir a tag <svg> dessa forma:
  
```xml
<svg width="100" height="100"/>
```

Neste exemplos definimos nosso SVG com o tamanho de 100 de largura e 100 de altura. Porém a unidade de medida, neste caso, não foi informada. 
SVG, Scalable Vector Graphics ou seja Gráficos Vetoriais Escaláveis, trazem uma proposta fantástica para o desenvolvimento de páginas responsivas pois suas dimensões são dinamicamente ajustadas ao tamanho do ecrã disponível, parecido com o a unidade ‘%’ de medida de CSS.

Os elementos filhos do SVG que abordaremos aqui são:

* Rectangle <rect>
* Circle <circle>
* Ellipse <ellipse>
* Line <line>
* Polyline <polyline>
* Polygon <polygon>
* Path <path>
  
Estes 7 elementos são os mais usamos ao construir representações gráficas com D3.

### Rect

Abaixo temos um retângulo criado com SVG:

```xml
<svg width="400" height="110">
  <rect width="300" height="100"
style="fill:rgb(0,0,255);stroke-width:3;stroke:rgb(0,0,0)"/>
</svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/rect01.PNG)

Seu resultado é:

* Os atributos height e width correspondem à altura da figura e largura respectivamente.
* O atributo de estilo CSS é o style, dentro dele foi escrito um CSS no grid.
* A propriedade ‘fill’ do CSS preenche o elemento com a cor inscrita nela.
* A propriedade ‘stroke-width’ do CSS define a largura do contorno do elemento.
* O ‘stroke’ define a cor da borda do nosso retângulo.

Vamos verificar outras propriedades:

```xml
<svg width="400" height="180">
  <rect 
        x="50" 
        y="20" 
        width="50" 
        height="50" 
        style="fill:purple;stroke:pink;stroke-width:5;fill-opacity:0.1;stroke-opacity:0.9" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/circle01.PNG)

* O grid tem 100 de largura(width) e 100 de altura(heigth).
* O child para criar um círculo é ‘circle’.
* cx e cy definem o ângulo do ponto central dentro do grid ou seja nesse exemplo o ângulo x e y ficam exatamente no centro do canvas.
* r representa o raio do círculo definido.
* stroke é a cor da borda. Neste caso, será preta.
* strole-width é a largura da borda.
* fill é a cor do preenchimento do círculo.

### Elipse

Abaixo temos uma elipse criada com SVG:

```xml
<svg height="140" width="500">
  <ellipse cx="200" cy="80" rx="100" ry="50"
  style="fill:yellow;stroke:purple;stroke-width:2" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/elipse.PNG)

* Assim como no exemplo do circle temos os atributos cx e cy para alinhar o centro do círculo.
* Neste caso, por se tratar de uma elipse temos dois raios um horizontal e um vertical rx e ry respectivamente.
* No exemplo temos as propriedades de preenchimento e bordeamento da elipse descritos em style como um CSS. Ou seja, já que se comportam como se fizermos uma classe com essas propriedades em um arquivo CSS e importarmos no SVG.

Outro exemplo:

``` xml
<svg height="100" width="500">
  <ellipse cx="240" cy="50" rx="220" ry="30" style="fill:yellow" />
  <ellipse cx="220" cy="50" rx="190" ry="20" style="fill:white" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/elipse02.PNG)

### Line

``` xml
<svg height="210" width="500">
  <line x1="0" y1="0" x2="200" y2="200" style="stroke:darkblue;stroke-width:2" />
</svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/linha01.PNG)

* x1 define o ponto horizontal inicial da linha.
* y1 define o ponto vertical inicial da linha.
* x2 define o ponto vertical final da linha.
* y2, adivinhe...
* dentro de style temos stroke(cor da linha) e stroke-width(espessura da linha).

### Polygon

Poligonos são um pouco complexos de serem manipilados em SVGs.

``` xml
<svg height="210" width="500">
  <polygon points="10,10 150,50 100,170" style="fill:#00ad43;stroke:#52ff95;stroke-width:5" />
</svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/polyline01.PNG)

* poits é o elemento mais importante de polygon.
* points são eixos e suas coordenadas funcionam semelhantemente à lines mas podem ser multiplas por isso são separadas por espaços.
* como nos exemplos anteriores, o primeiro eixo será x(horizontal) e o segundo será y(vertical) e definem o ponto inicial de uma linha.
* o próximo seguinte terá seus dois eixos definidos da mesma forma do que o ponto anterior.
* para que haja preenchimento e formação de um triângulo é necessário haver um novo ponto com seu eixos x e y. Sendo assim, 3 pontos sendo ligados por linha reta formam um triângulo.

Outro exemplo:

``` xml
<svg height="210" width="500">
  <polygon points="10,10 100,150 150,10 200,150 250,10 300,150 350,10 400,150" 
           style="fill:#00ad43;stroke:#52ff95;stroke-width:5" />
</svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/polyline02.PNG)

### Polyline

Polilinha funciona como um polígono porém sem preenchimento.

``` xml
<svg height="200" width="500">
  <polyline points="20,20 40,25 60,40 80,120 120,140 200,180 250,100 270,97" 
            style="fill:none;stroke:black;stroke-width:3" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/polilinha01.PNG)

Mais um exemplo de polilinha:

``` xml
<svg height="180" width="500">
  <polyline points="5,150 5,100 50,100 50,50 100,50 100,0" 
            style="fill:white;stroke:#ec2131;stroke-width:5" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/polilinha02.PNG)

## O TEMÍVEL PATH

Path não é só o elemento de uso mais complexo de SVG como também é o mais customizável. Com ele podemos criar linhas, curva, arcos o que já nos permite fazer muita coisa. O atributo que define as formas de um elemento path é 'd'. Os atributos que compõem 'd' são:

* M = moveto
* L = lineto
* H = horizontal lineto
* V = vertical lineto
* C = curveto
* S = smooth curveto
* Q = quadratic Bézier curve
* T = smooth quadratic Bézier curveto
* A = elliptical Arc
* Z = closepath

Vamos dar uma olhada num code pra assustar:

```xml
<svg width="200" height="200" xmlns="http://www.w3.org/2000/svg">
  <path d="M150 0 L75 200 L225 200 Z" />
</svg>
```
![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/path01.PNG)

Formas complexas podem ser feitas com o elemento polyline porém seu uso para tal exigiria muitas pequenas polilinhas além disso não escalaria tão bem.
O uso de editores de SVG para criação dinâmica de paths complexos é muito comum porém para corrigir erros em modelos SVG é importante ter um bom entendimento de path.

Cada um dos comandos é instanciado em 'd' pelo nome de sua classe e sua localização com as coordenadas xey, por exemplo M10 10, criará um elemento M nas posições x=10 e y=10.
O comando M significa Move To. Após instanciá-lo dessa forma M10 10 o parser aguarda pelo próximo comando.

Todos os comandos possuem duas variantes, um instanciado com a letra maiúscula(M) e outro com letra minúscula(m) sendo que a maiúscula especifica valores de coordenadas absolutas na página enquanto que minúscula específica coordenadas relativas(por exemplo, mover 10 px para cima e 7 para a esquerda do último ponto).
As coordenadas são sempre escritas sem unidade de medida.

Ao total são 5 os comandos de path para gerar linhas. O primeiro é o M(Move To) que recebe os parâmetros x e y. O preenchimento de apenas um M não renderiza nenhuma linha mas será ponto de partida para os próximos comandos que virão.

No exemplo a seguir foram inseridas as coordenadas xey(10 10) mas para que possamos ter uma ideia de onde estão os pontos colocaremos um pequeno ponto com circle em cada coordenada definida.

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/path02.PNG)

Existem 3 comandos para desenhar linhas. O mais genérico é L(Line To) que possuem duas coordenadas xey e desenha uma linha da posição atual para a coordenada inserida. Neste caso definirá o ponto de encerramento da figura.

```xml
    <svg width="400" height="400" xmlns="http://www.w3.org/2000/svg">
        <path d="M10 10 L10 10" />
        <circle cx="10" cy="10" r="2" fill="red"></circle>
    </svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/path02.PNG)

Agora colocaremos os parâmetros H e V. H para linha horizontal e V para linha vertical.

```xml
    <svg width="400" height="400" xmlns="http://www.w3.org/2000/svg">
        <path d="M 10 10 H 90 V 90 H 10 L10 10" />

        <circle cx="10" cy="10" r="2" fill="red"></circle>
        <circle cx="90" cy="10" r="2" fill="red"></circle>
        <circle cx="90" cy="90" r="2" fill="red"></circle>
        <circle cx="10" cy="90" r="2" fill="red"></circle>

    </svg>
```

![Test Image 2](https://github.com/RafaeloDuarte/Curso-D3.js/blob/master/assets/path03.PNG)

O comando Z sinaliza o fechamento da instrução.

```xml
    <svg width="400" height="400" xmlns="http://www.w3.org/2000/svg">
        <path d="M 10 10 H 90 V 90 H 10 L10 10 Z" />

        <circle cx="10" cy="10" r="2" fill="red"></circle>
        <circle cx="90" cy="10" r="2" fill="red"></circle>
        <circle cx="90" cy="90" r="2" fill="red"></circle>
        <circle cx="10" cy="90" r="2" fill="red"></circle>

    </svg>
```

Podemos abreviar o código dessa forma:

```xml
    <svg width="400" height="400" xmlns="http://www.w3.org/2000/svg">
        <path d="M 10 10 H 90 V 90 H 10 L10 10 Z" fill="transparent" stroke="black" />
    </svg>
```
