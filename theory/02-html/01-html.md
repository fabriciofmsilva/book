HTML
----------

### O que é o HTML?

HTML é a abreviação para HyperText Markup Language (Linguagem de Marcação e HiperTexto). Como o próprio nome diz ela serve para marcar conteudo (adicionar semântica) e adicionar ligações (*links*) entre documentos.

Atualmente HTML é a linguagem mais utilizada na Web para desenvolver páginas e applicações Web. O HTML foi criado por volta de 1991 pelo Sir Tim Berners-Lee no CERN. O HTML foi baseado em SGML (Standard Generalized Markup Language).

Se você quer se aventurar no mundo de desenvolvimento Web HTML é o ponto de partida. Como disse Diego Eis <q cite="http://www.casadocodigo.com.br/products/livro-guia-frontend">tudo começa e termina no HTML</q>.



### Criando nossa primeira página

Vamos criar a nossa primeira página HTML. Para isso crie um documento com o nome e extensão `index.html` e nele insira o conteúdo:

```html
Meu primeiro HTML.
```

Abra o arquivo no seu navegador favorito (recomendo usar o [Firefox](https://www.mozilla.org/firefox/)) e veja o que acontece. O navegador exibiu o texto que escrevemos.



### Estrutura básica

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

Na tag `<head>` é onde vamos inserir todas as nossas meta informações. Esses informações não farão parte do nosso conteúdo em si, mas servirão para o navegador.

Dentro da tag `<head>` temos a tag `<meta>`, no nosso caso com o atributo `charset="utf-8"`, as tags `<meta>` são tags onde vamos inserir metainformações. Dependendo do atributo podemos ter vários tipos de metainformações. No caso do atributo `charset` estamos dizendo o tipo de codificação que queremos que o navegador renderize nossos textos.

Ainda temos a tag `<title>`, nela é onde vamos dizer ao navegador o título da nossa página. Esse título é exibido na aba do navegador.

É na tag `<body>` onde a magia acontece. É lá onde vamos inserir todos os nossos elementos que serão interpretados pelo navegador e mostrados para o usuário.



### Elementos HTML

Um elemento HTML é formado por uma *tag* de abertura, seu conteúdo e uma *tag* de fechamento. Porém existem algumas exceções onde não existe a *tag* de fechamento, esses elementos são chamados de vazios. Segue um exemplo de um elemento:

```html
<tag>Conteúdo do elemento</tag>
<tag-vazia atributo="conteudo do atributo" />
```



### Tags HTML

Uma *tag* HTML é formada por `<`, seu nome, atributos e `>`, é a partir das *tags* que damos semântica ao conteúdo do HTML.

Abra novamento o arquivo `index.html` e vamos inserir algumas *tags* nele:

```html
<!doctype html>
<html>
    <head>
        <meta charset="utf-8">
        <title>Minha página</title>
    </head>
    <body>
        <header>
            <h1>Olá mundo.</h1>
        </header>

        <main>
            <h1>Meu primeiro HTML.</h1>
            <p>Seja bem-vindo ao meu primeiro HTML.</p>
        </main>

        <footer>
            <small>&copy; Fabrício Silva</small>
        </footer>
    </body>
</html>
```

Nesse exemplo começamos a estruturar o nosso HTML. Mais para a frente vamos entender as principais *tags* HTML. Por enquanto basta saber que adicionamos um cabeçalho (`<header>`), um conteúdo principal (`<main>`) e um rodapé (`<footer>`) a nossa página.
