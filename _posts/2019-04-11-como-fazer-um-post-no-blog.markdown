---
layout: post
title:  "Como fazer um post no blog?"
date:   2019-04-11 14:50:00 -0300
categories: post
author: Denis Manfroi
---

Antes de começar, farei um overview do projeto. O blog **{{ site.title }}** foi desenvolvido em [Jekyll](https://jekyllrb.com/). O Jekyll nada mais é do que um gerador de site estático, onde o mesmo pode ser hospedado de forma gratuita no **[GitHub Pages](https://pages.github.com/)**. Com ele você pode criar suas páginas de forma simples, utilizando HTML puro, ou mesmo a linguagem de marcação **[Markdown](https://www.markdownguide.org/)**. Caso queira utilizar o **Markdown**, não esqueça de mudar a extensão do arquivo para **.markdown** ou **.md**.

### Vamos lá...

Para criar um post aqui no blog é simples. Antes de tudo você deverá **clonar** o projeto `https://github.com/blogfstech/blogfstech.github.io.git`.

Feito o clone, basta acessar a pasta `_posts`, e nela vai conter os posts atuais. Recomendo que você copie um dos arquivos mudando a data e o nome. Fiquei atento para seguir o esquema de data correto, caso contrário pode dar problema.

Assim que abrir o arquivo, logo no início vai encontrar alguns parâmetros como:

{% highlight markdown %}
    ---
    layout: post
    title:  "Como fazer um post no blog?"
    date:   2019-04-11 14:50:00 -0300
    categories: post
    author: Denis Manfroi
    ---
{% endhighlight %}

Nessa etapa a única coisa que você não poderá mudar é o layout, que deverá continuar o default `layout:post`.

O conteúdo do post fica logo abaixo, sem muito segredo. Vai depender mesmo só da sua imaginação.

Post finalizado é hora de subir para o git. Basta fazer um pull request, e aguardar um tempo para que possamos aprovar o mesmo.

Basicamente é isso, caso precise de ajudar com alguma coisa, basta comentar.

Abraços!