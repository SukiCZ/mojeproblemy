---
layout: page
title: Moc mluvim o práci
---


Moje práce mě baví a furt o ní mluvim! Jsem backend developer jedné REST API. Je to vcelku velký projekt. Začínal vznikat v půlce roku 2013 a od té doby na něm spolupracovalo ~20 lidí. Je to e-shop, který běží na dvou produkčních serverech v sedmi regionech a deseti jazykových mutací. Je to náhrada našeho staršího katalogu, který používal stejně staré technologie, nebyl tak jednoduše rozšiřitelnej a vůbec - code base vlastnila externí firma. Je psanej v jazyce Python, kterej je strašně skvělej! Něco ti ukážu..

{% highlight python %}
>>> x = [1, 2, 3]  # array 3 čísel
>>> x.extend([4, 5])  # která se dá rozšířit o další array
>>> print x
[1, 2, 3, 4, 5]
>>> print [i for i in x]  # iterace array listu
[1, 2, 3, 4, 5]
>>> y = [i for i in x].extend([6, 7])  # iterace array listu se dá rozšířit
>>> print y  # ale nevznikne z toho nic
None
>>> z = [i for i in x] + [6, 7]  # iterace se dá sčítat
>>> print z
[1, 2, 3, 4, 5, 6, 7]

{% endhighlight%}

Jednou jsem takhle řešil, jakou cenu má ta API zobrazovat na detailu produktu, ke kterému se vztahují dodací podmínky s různou cenou (array `x`, dodací podmínky můžou být prázdné) a na detailu produktu se tak měla zobrazovat ta nejnižší. Minimum z prázdného listu vrací chybu..

{% highlight python %}
>>> print min([])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: min() arg is an empty sequence

{% endhighlight %}

..a tak jsem ho musel rozšířit o maloobchodní cenu produktu. Extend to neřešil. Poznámka pro přístě:

* Iterace listu se sčítají - nerozšiřují
