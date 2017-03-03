---
layout: page
title: Moc mluvim o práci
---


Moje práce mě baví a furt o ní mluvim. Mým povoláním je převážně backend developer jedné REST API. Je to větší projekt než já, začínal vznikat v půlce roku 2013 a od té doby na něm spolupracovalo ~20 lidí. Je psanej v jazyce Python, kterej je strašně skvělej! Něco ti ukážu..

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

Jednou jsem takhle řešil, jakou cenu má ta API zobrazovat na detailu produktu, ke kterému se vztahují dodací podmínky s různou cenou a na detailu produktu se tak měla zobrazovat ta nejnižší. Potřeboval jsem minimum z array listu, kterej ovšem mohl bejt prázdnej..

{% highlight python %}
>>> print min([])
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: min() arg is an empty sequence

{% endhighlight %}

..a tak jsem ho chtěl rozšířit o maloobchodní cenu produktu. Sečtení to v pořádku vyřešilo. :-\|
