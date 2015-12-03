Dev Book
==========


Introdução a programação Web
==========

O objetivo deste capítulo é apresentar os conceitos básicos sobre programação Web. Introduzir algumas tecnologias, vantagens e desvantagens.

Um desenvolvedor web é capaz de desenvolver web sites e/ou web apps para a Internet (World Wide Web) e/ou Intranet (rede privada).

Algumas das disciplinas que um desenvolvedor web deve conhecer são: web design, desenvolvedor de conteudo web, programação do lado do cliente/servidor, servidor web, configuração e segurança de redes, desenvolvimento de e-commerce.





Arquitetura Web
----------

Antes de colocarmos a mão no código é importante conhecer alguns conceitos que irão ajudar entender como as coisas funcionam.



### Cliente e Servidor

A arquitetura mais simples que existe na Web é a cliente/servidor.

Basicamente o Internet é formada por uma rede de computadores interligados. Um computador (cliente) pode enviar uma mensagem para outro computador (servidor) através de protocolos.

O protocolo mais usado na Web é HTTP (Hyper Text Transfer Protocol).




Navegador -> URL -> DNS/IP -> Servidor

HTTP Request e Response



### Navegadores (Browser)

Aqui vou falar sobre navegadores. Firefox. Chrome. Internet Explorer (EDGE). Safari.



### Servidor

Aqui vou falar sobre servidores.

- Conteúdo estático x dinâmico.
- Ciclo de vida de informações entre servidor e cliente (escopo)
- Linguagens
- Servidores Web
- Servidores de Aplicação





Configurando o Ambiente (Ferramentas)
----------

Boas ferramentas são importante para ajudar você a solucionar os problemas.

Para desenvolver para Web precisamos de duas ferramentas básicas:

- Navegador para debugar HTML, CSS e JavaScript
- Um bom Editor de texto


### Navegadores

Aqui vamos configurar os navegadores.


#### Debugando uma página Web

- View source
- Inspect Element
- Atualizando valores
- JavaScript Console



### Editores de Texto

Um editor de texto é onde você vai passar a maior parte do tempo. Depois do seu conhecimento e experiência para mim é a ferramenta mais importante. Ter dominio das *features* que um editor de texto tem é fundamental para melhorar a produtividade de qualquer desenvolvedor.

Para desenvolvermos nossas aplicações precisamos de um bom editor de texto. Aqui não vale usar um editor de texto rico como o **Word** da Microsoft ou o **Pages** da Apple, pois eles adicionam `meta tags` para formatar o texto e elas atrapalham nosso código.

No mercado temos muitas opções de editores de texto.



#### Sobre os WYSIWYG

Existem alguns editores do tipo <abbr title="What You See Is What You Get">WYSIWYG</abbr>, mas vamos evitar eles.



#### Sobre IDE

Por enquanto vamos evitar o uso de IDEs também.


#### Vim e Emacs

Aqui vou falar sobre editores de linha de commando.


#### Sublime Text

- Sintaxe highlight
- Match Parenthesis
- Replace All



### Linha de Comando (CLI -> Command-line Interface)

`pwd`, `ls`, `ls -a`, `mkdir [dir]`, `cd [dir]`, `touch [file]`, `cp`, `mv`, `rmdir`, `cat`, `less`.



### Controle de Versão

#### Git

Aqui vou falar sobre Git.

`git init`, `git status`, `git add [file(s)]`, `git commit -m [msg]`, `git log`.



#### GitHub

Aqui vou falar sobre o GitHub.





HTTP
----------

Aqui vou falar sobre HTTP.

- Status Code

100s are informational
200s are successes
300s are redirection (something moved)
400s are client errors
500s are server errors





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





CSS
----------

### O que é CSS?

CSS é a abreviação para Cascading Style Sheet. Ela é uma linguagem de folhas de estilo utilizada para estilizar documento HTML.





JavaScript
----------

JavaScript é uma linguagem de programação.





jQuery
----------

Aqui vou falar sobre jQuery.





Introdução ao desenvolvimento Front-End
==========

Atualmente o desenvolvimento Front-End para Web é baseado em três tecnologias, o HTML, o CSS e o JavaScript. Junto os três é possivel criar desde Web Sites até aplicações Web.

Aqui vemos o primeiro conceito de separação de responsabilidades, o HTML é o responsável pela estrutura do conteudo. Já o CSS é o responsável pelo estilo do conteúdo, e o JavaScript é o responsável pelos comportamentos.





JavaScript
----------

JavaScript é uma linguagem de programação.

### Test-Driven Development

### Jasmine

Aqui vou falar de Jasmine





DOM
----------

O Modelo de Objetos do Documento.

Aqui vou falar sobre DOM.





jQuery
----------

Aqui vou falar de jQuery.





AJAX
----------

Aqui vou falar sobre AJAX.

- Asynchronous Javascript And XML





Introdução ao desenvolvimento UI/UX
==========





Introdução ao desenvolvimento JavaScript
==========


AngularJS
----------

Aqui vou falar de AngularJS.





Introdução ao desenvolvimento JavaScript BackEnd
==========

NodeJS
----------

Aqui vou falar de NodeJS.

### Test-Driven Development





SQL
----------

Aqui vou falar de SQL.





Introdução ao desenvolvimento FullStack com MEAN
==========


Express
----------

Aqui vou falar de express.





MongoDB
----------

Aqui vou falar de MongoDB.





Introdução ao desenvolvimento Mobile Hídrido
==========

Aqui vou falar sobre desenvolvimento mobile hibrido.





Cordova
----------

Aqui vou falar sobre o cordova.









# TODO: Tópicos para organizar

## Padrões de projetos (Design Patterns)

[//]: # (Escrever sobre padrões de projeto)

Padrões de projetos são soluções elegantes (reutilizáveis) para problemas comunsm (que ocorrem com frequência). Um padrão de projeto não é uma solução pronta para escrever software, mas sim um template (modelo) para se usar de base para resolver o problema, cada implementação de um *design pattern* pode variar de projeto para projeto.

Os primeiros passos para os padrões de projetos foram cunhados por Chirstofer Alexandrer, onde um padrão deve ter as seguintes características: encapsulamento, generalidade, equílibrio, abstração, abertura, combinatoriedade. Além disso sevem seguir o formato: nome, exemplo, contexto, problema, solução. Depois o movimento ganhou notoriedade com a *Gang of Four* (**GoF**), Erich Gamma, Richard Helm, Ralph Johnson e John Vlissides, autores do livro: Design Patterns: Elements of Reusable Object-Oriented Software.



### Padrões GoF ('Gang of Four')

Os padrões **GoF** são organizados da seguinte forma:

| Creational | Baseados no conceito de criação de objetos. |
| ---------- | ------------------------------- |
| Factory Method | This makes an instance of several derived classes based on interfaced data or events. |
| Abstract Factory | Creates an instance of several families of classes without detailing concrete classes. |
| Builder | Separates object construction from its representation, always creates the same type of object. |
| Prototype | A fully initialized instance used for copying or cloning. |
| Singleton | A class with only a single instance with global access points. |


| Structural | Baseados na ideia de construir blocos de objetos. |
| ---------- | ---------------- |
| Adapter | Match interfaces of different classes therefore classes can work together despite incompatible interfaces. |
| Bridge | Separates an object's interface from its implementation so the two can vary independently. |
| Composite | A structure of simple and composite objects which makes the total object more than just the sum of its parts. |
| Decorator | Dynamically add alternate processing to objects. |
| Facade | A single class that hides the complexity of an entire subsystem. |
| Flyweight | A fine-grained instance used for efficient sharing of information that is contained elsewhere. |
| Proxy | A place holder object representing the true object. |

| Behavioral | Baseados nas interações e divisões de responsabilidades entre os objetos |
| ---------- | --------- |
| Interpreter | A way to include language elements in an application to match the grammar of the intended language. |
| Template Method | Creates the shell of an algorithm in a method, then defer the exact steps to a subclass. |
| Chain of Responsibility | A way of passing a request between a chain of objects to find the object that can handle the request. |
| Command | Encapsulate a command request as an object to enable, logging and/or queuing of requests, and provides error-handling for unhandled requests. |
| Iterator | Sequentially access the elements of a collection without knowing the inner workings of the collection. |
| Mediator | Defines simplified communication between classes to prevent a group of classes from referring explicitly to each other. |
| Memento | Capture an object's internal state to be able to restore it later. |
| Observer | A way of notifying change to a number of classes to ensure consistency between the classes. |
| State | Alter an object's behavior when its state changes. |
| Strategy | Encapsulates an algorithm inside a class separating the selection from the implementation. |
| Visitor | Adds a new operation to a class without changing the class. |

Os padrões **GoF** podem ser classificados segundo o seu escopo:

| Escopo | Definição |
| ------ | --------- |
| Classe | Definido por relacionamentos de herança e em tempo de compilação. |
| Objeto | Encontrados no relacionamento entre os objetos definidos em tempo de execução. |



## Referências

- [Wikipédia](https://pt.wikipedia.org/wiki/Padr%C3%A3o_de_projeto_de_software)
- [Learning JavaScript Design Patterns](http://addyosmani.com/resources/essentialjsdesignpatterns/book/#summarytabledesignpatterns), Addy Osmani

[//]: # (https://en.wikipedia.org/wiki/Software_design_pattern)
[//]: # (http://www.tutorialspoint.com/design_pattern/design_pattern_overview.htm)
[//]: # (http://www.princiweb.com.br/blog/programacao/design-patterns/o-que-sao-design-patterns.html)
[//]: # (http://www.casadocodigo.com.br/products/livro-design-patterns)
[//]: # (https://sourcemaking.com/design_patterns)
[//]: # (http://www.oodesign.com/)

[//]: # (https://www.pluralsight.com/courses/patterns-library)
[//]: # (http://br.phptherightway.com/pages/Design-Patterns.html)
[//]: # (http://www.devmedia.com.br/curso/introducao-a-design-patterns/188)
[//]: # (http://www.vincehuston.org/dp/)

[//]: # (https://nandovieira.com.br/design-patterns-no-javascript-module)
[//]: # (https://nandovieira.com.br/design-patterns-no-javascript-singleton)
[//]: # (https://nandovieira.com.br/design-patterns-no-javascript-factory)
[//]: # (https://nandovieira.com.br/design-patterns-no-javascript-decorator)

[//]: # (http://code.tutsplus.com/tutorials/design-patterns-the-decorator-pattern--cms-22641)

[//]: # (http://www.dofactory.com/javascript/design-patterns)





### Outros

[//]: # (Tópicos que podem entrar no livro)

- clean software craftsmanship
- Test-driven development (TDD)
- Engineering best practice, such as pairing and regular code reviews, is second nature
- Linux (both as a production and development environment)
- Version control systems e.g. Git
- Continuous integration e.g. Jenkins
- Build tooling e.g. Grunt
- Browser-testing techniques e.g. CasperJS or cucumber.js
- RESTful APIs and Service Oriented Architecture (SOA)
- Cloud-based deployments e.g. Azure / AWS
- Server-side languages - Clojure preferably but experience of others such as Perl, Ruby, PHP, Python is also beneficial
- Collaboration and use of Open Source software.
- communication skills









