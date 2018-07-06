---
layout: post
title: Inferencia de variável local no Java 10
date: 2017-02-07 17:00:00
img: java10.jpg
description: Aprenda como funciona a inferencia de tipo em variaveis locais no Java 10
tags: [Java10, novdades]
---

A inferência de tipo em variáveis locais é uma novidade apenas no Java 10, por que em outras linguagens como Scala, Kotlin, C# isso já existia!!

### Definição

Inferência de tipo é a capacidade do compilador de deduzir automaticamente o tipo de uma variável.

### Legal, mas quero ver isso na prática!!!

Calma!! Vamos lembrar um pouco da evolução até o Java 10! 

Antes do  Java 7:

{% highlight java %}
	Map<String, String> fullName = new HashMap<String, String>();
{% endhighlight %} 

No Java 7 e o diamond operator:

{% highlight java %}
        Map<String, String> fullName = new HashMap<>();
{% endhighlight %}

O Diamond Operator já ajudou bastante!

No lambda do Java 8:

{% highlight java %}
	x -> x.toLowerCase(); 
{% endhighlight %}

Repare que embora possível, não declaramos o tipo da variável x !!

Reparou que todas as inferências estão do lado direito da expressão!? Agora o Java 10 veio para inferir o tipo do lado esquerdo também através do nome de tipo reservada **var** !!!

{% highlight java %}
	var i = 0;
	var nome = "rickyTaki";
	for (var i = 0; i < 5; i++) { ... }
	for (var nome : nomes) { ...} 
{% endhighlight %}

### Restrições

Reparem que eu disse **nome de tipo reservado** e não keyword, ou seja, classes e interfaces não podem ser nomeadas como var já que o compilador não faria a menos idéia se a variável é do tipo var ou se a inferência está sendo usada! Isso faz com que não seja retro compatível, mas como um bom dev, você não deve ter nomeando nenhuma classe ou interface como var, não é mesmo!??

O **var** também não pode ser usado como retorno nem parâmetro de funções nem construtores e o catch do try-catch.

### Onde pode ser usada então!?

Em três situações que você já viu lá em cima:

* Variáveis locais inicializadas;
* Dentro de fors;
* Dentro de enhanced for;

### Tome cuidado com a legibilidade

Agora, com o uso do var sendo possível, tome mais cuidado com a legibilidade do seu código! Siga as boas práticas ao nomear variáveis e métodos, considere o seguinte exemplo:

{% highlight java %}
	var x = y.getFoo();
{% endhighlight %}

Consegue decifrar o tipo!? Óbvio que na hora você vai entender e vai achar que pra sempre vai lembrar, mas imagine duas semanas depois... Você va ter que entrar em Y pra entender qual o retorno do método!
Pra resolver isso, capriche na nomenclatura para que o var não se torne um problema no seu código:

{% highlight java %}
	var name = user.getName();
{% endhighlight %}

### Conclusão

Pronto, agora você já sabe usar o **var**, quando usar e quais cuidados tomar!!

Um abraço,

Ricky Taki 
