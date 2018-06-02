---
layout: post
title: DRY - Don't Repeat Yourself
date: 2017-02-06 17:00:00
img: dry.png
description: Aprenda sobre o princípio DRY que todo dev deveria saber 
tags: [Best-Practices, Essentials]
---

Independente da linguagem de programação que você usa, existem princípios que você deve saber e um deles é o DRY - Don't Repeat Yourself!!!

### Definição

> "Every piece of knowledge must have a single, unambiguous, authoritative representation within a system"
 
Em tradução livre, quer dizer que todo pedaço de conhecimento dentro de um sistema deve ter uma única, inequívoca e autoritária representação.

### Eita, mas oq isso quer dizer!?

Nada mais do que o título diz, **Não se repita !!** Se você está dando copy paste no seu código, você está errado! Para seguir o princípio, abstraia o bloco de código repetitivo para uma unidade reutilizável como uma função, método, macro ou o que for relevante para a linguagem que você estiver utilizando e faça uma chamada onde precisar usar.

### O que eu ganho com isso!?

Vamos lá, vamos supor que você tenha um bloco de código que você utiliza em diversas partes do seu programa e que utiliza um valor X +2. Legal, tudo funciona e todo mundo tá feliz, até o trágico dia que pedem para você mudar de X + 2 para X + 3... Mais um daqueles requisitos fáceis que devem ser rapidinho né... Você consegue lembrar rapidamente em quantas partes do seu código você deu copy paste!?? Duvido que você sequer lembre do código que escreveu semana passada, quanto mais do que escreveu meses ou até anos atrás. E pra melhorar, voc6e achando que era facinho resolveu fazer o deploy na sexta feira a noite e na hora do vamos ver, a parada não roda... Ah, esqueci de alterar em um pedaço só, você vai lá e altera, e nada... Aí você vai desejar com todas as suas forças ter seguido o DRY!!!

Isso falando que nem o deploy rolou, mas pode ser pior, o deploy pode rolar mas por algum "motivo" (DRY) o resultado esperado pela contabilidade não é o mesmo que o sistema dá... Xiii, agora não é mais só o gerente na tua cola, é o CTO, o CFO, o DEO todos te cobrando resultado, tudo por que você não seguiu o DRY... 
