HTML
==========

O que é o HTML?
----------

HTML é a abreviação para HyperText Markup Language (Linguagem de Marcação e HiperTexto). Como o próprio nome diz ela serve para marcar conteudo (adicionando semântica ao conteudo) e adicionar ligações (*links*) entre documentos.


Criando nossa primeira página
----------

Vamos criar a nossa primeira página HTML. Para isso crie um documento com o nome e extensão `index.html` e nele insira o conteúdo:

```html
Meu primeiro HTML.
```

Abra o arquivo no seu navegador favorito (recomendo usar o [Firefox](https://www.mozilla.org/firefox/)) e veja o que acontece. O navegador exibiu o texto que escrevemos.


Estrutura básica
----------

Altere o arquivo `index.html` com a seguinte estrutura. Aqui o importante é digitar todas as linhas para ir praticando a sintaxe do HTML.

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Minha página</title>
    </head>
    <body>
        <!-- Conteúdo da página vai aqui -->
        Meu primeiro HTML.
    </body>
</html>
```

A estrutura acima é a estrutura mais básica de um documento HTML. Vamos entender o que significa cada elemento.


O `<!doctype html>` é uma declaração, não é uma tag HTML, mas sim uma instrução onde falamos para o navegador qual a versão do HTML estamos usando. No caso a última versão do HTML, o HTML5.

Todo documento HTML deve começar com a tag `<html>` é nele onde vamos inserir todas as outras tags.

Na tag `<head>` é onde vamos inserir todas as nossas meta informações. Esses informações não farão parte do nosso conteúdo em si.

É na tag `<body>` onde a magia acontece. É lá onde vamos inserir todos os nossos elementos que serão interpretados pelo navegador e mostrados para o usuário.
