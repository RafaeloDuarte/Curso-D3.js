# Curso-D3.js

D3 é uma biblioteca JavaScript para desenvolver representações gráficas. É muito usado para representação visual de dados.

A visualização de dados possui grande relevância nos meios informativos, dentre elas temos gráficos populacionais, mapas com representações sociopolíticas, linhas temporais históricas e muitas outras. O D3 é utilizado no mundo todo para criar as mais diversas representações por sua dinamicidade praticamente infinita. O D3 é de rápido processamento pois se trata de uma lib JS e por isso é interpretado pelos motores de JavaScript já utilizados pelos navegadores. 

Partindo do pressuposto de que a maioria das pessoas interessadas nesse conteúdo possui conhecimentos básicos sobre a linguagem JavaScript, iniciaremos este curso falando um pouco sobre SVG, que é o elemento HTML mais manipulado pelo D3, em seguida partiremos para o conteúdo de D3 propriamente dito.

SVG é uma linguagem XML e pode ser um tipo de elemento HTML, assim como body, p, table e tantos outros conhecidos por todo desenvolvedor web. Para usá-lo devemos abrir nosso documento HTML e inserir a tag <svg> dessa forma:
  
```xml
<svg width="100" height="100">
</svg> 
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
