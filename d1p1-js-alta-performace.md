[commit misterioso](https://gist.github.com/pbalduino/8817d618)
[slides](https://pbalduino.github.io/jsexperience2017/slides/)

Repaint e Reflow levam muito tempo para serem processados pelo js, se poss√≠vel passar as anima√√es para o css

evitar animacoes css que alterem propriedades do elemento. Dar prefer√ncia para regras como transform, translate e rotate, mas isso nao funciona no firefox :-/

DocumentFragment para usar virtual dom sem react ou vue

```
var frag= document.createDocumentFragment()
var div = document.getElementById('my-div')
frag.appendChild(div)
frag.appendChild(div)
frag.appendChild(div)
div.appendChild(frag) // <-- repaint/reflow s√≥ acontecem uma vez
```

