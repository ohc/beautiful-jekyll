---
layout: post
title: Como eu crio posts pro OHC?
tags: [ohc, posts]
bigimg: /img/codeimage.jpg
---

Agora que mudamos nossa plataforma para o Jekyll, esperamos que fique mais fácil a colaboração com artigos, afinal agora podemos usar git/markdown e isso dá mais tesão e incentiva mais o pessoal a escrever.

Este post é pra justamente dar o básico para aquele que não esta familiarizado com Jekyll/Github/Markdown.

Bom, agora como o site é um repositório dentro do github, o git será um grande amigo seu :P. Para aqueles que estão como colaboradores, basta clonar o repositório diretamente, já para quem não esta como colaborador é necessário que se faça um *fork* primeiramente:

```
# Como colaborador
git clone https://github.com/ohc/ohc.github.io.git
```

Se você ainda não é um colaborador, é necessário que *fork* o projeto inicialmente:

![](/img/fork.jpg)

E então, clonar a partir do seu repositório:

![](/img/clone.jpg)

```
# Como não colaborador
git clone https://github.com/<username>/ohc.github.io.git
```

Troque username pelo qual você usa no github.

Deste ponto em diante é o mesmo para colaborador ou não. Primeiro entre no repositório e crie uma branch com o nome que preferir:

```
cd ohc.github.io
git checkout -b meupost
```

Os posts devem estar na pasta *_posts* e devem ser escritos em Markdown.

Até mesmo este post pode servir como exemplo para saber como escrever em Markdown.

Outro ponto é que o nome do arquivo deve seguir a seguinte estrutura:

```
YYYY-MM-DD-título.md
```

No caso deste post:

```
2016-10-10-como-crio-posts-pro-ohc.md
```

Criado seu post, você precisa dar um *add* para monitorar suas alterações, um *commit* (de preferência com uma mensagem sobre do que se trata seu post) e um *push* para subir suas alterações para o repositório:

```
git add .
git commit -m "Meu post sobre como criar posts no site do OHC :)"
git push origin meupost <=== nome do branch criado anteriormente
```

Para aquele que é colaborador, deve agora ir até repositório no github e criar um PR (pull request) clicando em 'Compare & pull request'

![](/img/pullr.jpg)

Selecionar o repositório:

*NOTE:*> Preste bastante atenção para não criar um PR no repositório errado. Selecione *ohc/ohc.github.io*

![](/img/selectrepo.jpg)

Em seguida, 'Create pull request':

![](/img/createpr.jpg)

Pronto! Seu PR foi enviado e assim que for avaliado será aceito ou negado, mas com a explicação e com instruções de como nós estamos esperando.

Espero que tenha sido útil para aqueles que querem escrever um post na plataforma Jekyll. Para mais informações: [Jekyll](https://jekyllrb.com/)
