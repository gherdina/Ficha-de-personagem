[fonte](https://github.com/drachehavoc/ia26-webdesign)

# webdesign

essa diciplina foca em geral na lingugem de marcação relacionada ao design de sites, explicando a lógica da linguagem html e suas ferramentas de uso ex: nomes de tags e suas atribuições, focando nos principios basicos de desenvolvimento de interface web e sua compreenção.

## pré requisitos

é necessario ter em seus dispositivos um editor de codigo para poder acompanhar as aulas> nessa diciplina usaremos visual studio code como editor de código.


# *HTML* (HyperText Markup Language (Linguagem de Marcação de Hipertexto))

*html* não é uma linguagem de programação e sim e marcação, pois ultiliza apenas marcações que dão atribuições á textos, imagens ou estilos, sendo responsavel pelo conteúdo de uma página web, para pessoas tanto comuns quanto com deficiencias com recursos de acessibilidade. 
html é compoto por uma série de elementos,cada um representado por uma tag (etiqueta) que define o tipo de conteúdo e sua função na página. Por exemplo, `<h1>` é usado para títulos principais, `<p>` para parágrafos, `<a>` para links, entre outros. O HTML também permite a inclusão de atributos nas tags para fornecer informações adicionais sobre os elementos, como `class`, `id` , `src` , etc.

Antes de seguirmos, imagine um editor de texto como o Microsoft Word ou o Google Docs. Em editores como estes, você costuma selecionar um trecho de texto e aplicar uma formatação, como negrito, itálico ou sublinhado. O HTML é a linguagem que permite marcar o trecho selecionado com uma tag (etiqueta) que indica a formatação desejada, sendo que a sintaxe do HTML é composta por tags (etiquetas) de abertura e fechamento, onde a etiqueta de abertura é escrita entre colchetes angulares `< >` e a etiqueta de fechamento é escrita da mesma forma, mas com uma barra `/` antes do nome da tag. Por exemplo, para criar um parágrafo em HTML, você usaria a tag `<p>` para abrir o parágrafo e `</p>` para fechá-lo. O conteúdo do parágrafo seria colocado entre essas duas tags.

![Animação de seleção](https://github.com/drachehavoc/ia26-webdesign/raw/main/docs/select.gif)

Na animação acima, o usuário escreve em um editor a frase `lorem ipsum dolor sit amet potentia` e, então, executa algumas seleções de definição de formatação. A seguir, veremos, passo a passo, o equivalente em HTML para cada uma dessas seleções/formatações.

passo a passo:

1.
- o usuario ultiliza a tag `<strong>` e para fechar a tag `</strong>` para tornar "lorem ipsum" megrito, pois todo o texto dentr dessa tag se torna negrito.

2.
- o usuario ultiliza a tag `<em>` e para fechar a tag `</em>` em "sit amet", pois o texto incluido nessa tag se torna itálico.

3.
- o usuario seleciona "ipsum dolor sit" e o coloca na cor vermelha ultilizando a tag `<spam style="color: red;">` e para fechar a tag `</spam>` 

código final:

<strong>  `<strong>lorem <span style="color: red;">ipsum dolor sit</span></strong> amet <em>sit amet</em> potentia` </strong>


>**⚠️Nota**:
>
>O html, para fins de acessibilidade( como por exemplo, paginas com audiodescrição ) ultiliza algumas tags que substituindo outras que funcionam do mesmo modo porem não tem semantica.
>
>*exemplos*:
>
>- `<strong>` substitue `<b>`
>
>- `<em>` substitue `<i>`

# Estrutura básica do html

- **Declaração do tipo de documento:**

 *ex:* `<!DOCTYPE html>`, declara o tipo do código

- Dentro do html temos duas partes principais:

  **`<head>`**: *Inclue as informações sobre a página*, links para arquivos css, título etc. Não é visivel no front da página.


  **`<body>`**: *Conteúdo visível na página*, títulos, parágrafos, imagens, links e etc... É o que o usuário ve ao acessar a página.

  **Estrutura na prática:**

 ```
 <!DOCTYPE html>
<html lang="pt-BR">
<head>
   <meta charset="UTF-8">
   <title>Título da Página</title>
   <!-- Links para arquivos CSS e scripts JavaScript podem ser adicionados aqui -->
</head>
<body>
   <!-- Conteúdo visível da página é adicionado aqui -->
</body>
</html>
```
>**⚠️Nota:**
>
>- Todo o código deve estar dentro da tag `<html>`
>
>- o atributo `lang=¨pt-BR¨` *serve para indicar que o idioma da página está em portugues BR*, importante para mecanismos de busca e acessibilidade.
>
>- o elemento `<meta charset=¨UTF=8¨>` define os caracteres do documento como UTF-8, o que garante que caracteres ascentuados e outros simbulos sejam exibidos de forma correta.
>
>- o elemento `<title>` define o titulo da página na aba do navegador.

# Atributos html

Dão informações adicionais as tags, e as controlam, consistem em um nome e um valor, separados por um sinal de igual `=`.

**exemplos de atributos:**

- `href` é usado em uma tag `<a>` para indicar o URL de um link.

- `src` é usado em uma tag ``<img>` para especificar a fonte da imagem.

## Prática:

se quisermos criar um link para o google em nossa página, usamos a tag `<a>` e o atributo `href` para especificar o link do google:

`<a href="https://www.google.com">Visite o Google</a>`

na página isso resulta em um texto que se pressionado leva o usuário ao site desejado:

<a href="https://www.google.com">Visite o Google</a>

# CSS - Cascading Style Sheets (Folhas de Estilo em Cascata)

É uma linguagem de estilo que controla a aparencia e o layout de uma página. Permite estilizar os elementos do html, atribuindo cores, fontes, margens, espaçamento e etc. Usamos o **CSS** em um arquivo separado do **HTML**, o que permite mexer em ambos os codigos separadamente otimizando a organização e facilitando a manutenção do site. Ultiliza *seletores* e *declarações*.

**Seletores:** Selecionam os elementos do html que serão customizados

**Declarações:** Definem as propriedades de estilo e seus valores.

## Demonstração:
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
   <meta charset="UTF-8">
   <title>Exemplo de CSS</title>
   <link rel="stylesheet" href="styles.css">
</head>
<body>
   <h1>Olá, Mundo!</h1>
   <p>Este é um exemplo de CSS.</p>
</body>
</html>
```

para alterar o codigo html acima, usamos o css, que esta como um arquivo externo dentro do html, usando a tag `<link>` no `<head>`. podemos alteralo da seguinte forma:
```
/* styles.css */
body {
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
}

h1 {
  color: #333333;
  text-align: center;
}

p {
  color: #666666;
  font-size: 18px;
  margin: 20px;
}
```

as alterações no exemplo acima resultam em um fundo cinza claro, um titulo escuro e centralizado e um parágrafo de uma cor mais clara que o texto, tamanho maior e com margem:

![CSS Aplicado](https://github.com/drachehavoc/ia26-webdesign/raw/main/docs/image-css.png)

O css personaliza nosso codigo, o tornando o site mais bonito e proficional, sem o css o site seguiria o estilo padrão do navegador, dando uma aparencia mais amadora e sem detalhes. 👇

![CSS Aplicado](https://github.com/drachehavoc/ia26-webdesign/raw/main/docs/image-css-none.png)

# Sintaxe do CSS

É composta por regras de estilo, cada regra é formada por um *seletor* e um *bloco de declarações*:

**Seletor:** Seleciona o elemento html a ser modificado.

**Bloco de declarações:** Define as propriedades, estilos e valores do elemento.
```
seletor {
  propriedade: valor;
  propriedade: valor;
  /* ... */
}
```

>**⚠️Nota:**
>
>O seletor pode ser um **nome** de elemento HTML, uma **classe**, um **ID** ou uma combinação desses.
>
> As propriedades são palavras chave que definem o visual de um elemento.
>
>ex: `color`, `font-size` ou `background-color`.
>
>Valores são atribuidos as propriedades para especificar o estilo desejado.
>
>ex: `red`, `16px`, `#f0f0f0`.
>
>**Cada declaração deve ser separada por `;`**

# Seletores CSS

Selecionam os elementos HTML aos quais serão aplicadas regras de estilo. Sua logica se baseia na **estrutura do documento**(hierarquia dos elementos, chamamos de ¨cascading¨-em cascata). Permitem **aplicar estilos a um elemento especifico ou a grupos de elementos** com base em suas caracteristicas, como tipo, classe, ID, atributos e etc.

## Tipos de seletores:

- **Seletor de tipo:** Seleciona elementos de certo tipo  (ex: `<h1>`, `<p>`, `<a>`), para estilizalos. Ex: `h1 { color; blue;}` (da a cor azul a todos os `<h1>`).

- **Seletor de classe:** Seleciona elementos de certa classe (para isso ultilizamos ¨.¨ e depois o nome da classe) ex: `.texto {font-size; 40px; }` (aumenta a letra na classe texto).

- **Seletor de ID:** Seleciona um ID especifico. ex: `#paragrafo1 { color: red; } ` (torna vermelho apenas o ID paragrafo1).

- **Seletor de atributo:** Seleciona um atributo ou valor especifico do mesmo. ex: `a[href="#"] { text-decoration: none; } ` (remove a linha abaixo de um href de valor ¨#¨).

- **Pseudo-Classes:** Seleciona com base na hierarquia do documento. ex: `p:first-child { font-weight: bold; } ` (aplica negrito ao 1 filho dentro de um elemento pai).

## Hierarquia:
```
<main>
  <section>
   <p>Este é um parágrafo dentro de uma seção...</p>
  </section>
</main>
```

`<p>` está dentro de `<section>` que está dentro de `<main>`

**Se usarmos `main section p  { color: green; } ` tornaremos verde todos os `<p>` dentro do `<main>`.**
```
<main>
  <section>
   <p>Este é um parágrafo dentro de uma seção...</p>
  </section>
  <p>Este é um parágrafo fora da seção...</p>
</main>
```

Com base no exemplo acima, podemos tornar verde apenas os `p` que estão dentro de section usando ` section p { color: green; }`.

**Ficará assim:**

![Hierarquia seletores](https://github.com/drachehavoc/ia26-webdesign/raw/main/docs/image-css-selectors.png)


# Tipos de seletores CSS

**na tabela abaixo veremos os tipos de seletores no css e qual suas funções👇**

| Tipo de Seletor               | Exemplo&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Descrição |
|------------------------------ | -------------------------------- | --------- |
| Seletor de Tipo               | `nome_elemento { }`              | Seleciona todos os elementos de um determinado tipo. Exemplo: `p { color: blue; }` seleciona todos os parágrafos e aplica a cor azul. |
| Seletor de Classe             | `.nome_classe { }`               | Seleciona elementos com uma classe específica. Exemplo: `.titulo { font-size: 24px; }` seleciona todos os elementos com a classe "titulo" e aplica um tamanho de fonte de 24 pixels. |
| Seletor de ID                 | `#nome_id { }`                   | Seleciona um elemento com um ID específico. Exemplo: `#paragrafo1 { color: red; }` seleciona o elemento com o ID "paragrafo1" e aplica a cor vermelha. |
| Seletor de Atributo           | `elemento[atributo="valor"] { }` | Seleciona elementos com um atributo específico ou um valor de atributo específico. Exemplo: `a[href="#"] { text-decoration: none; }` seleciona todos os links que têm um atributo `href` com o valor "#" e remove o sublinhado. |
| Pseudo-classes                | `elemento:pseudo-classe { }`     | Seleciona elementos com base em seu estado ou posição na hierarquia do documento. Exemplo: `p:first-child { font-weight: bold; }` seleciona o primeiro parágrafo dentro de seu elemento pai e aplica negrito. |

## Seletores de descendentes, filhos e irmãos:


| Tipo de Seletor               | Exemplo&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; | Descrição |
|------------------------------ | -------------------------------- | --------- |
| Seletor de Descendente        | `elemento1 elemento2 { }`        | Seleciona elementos que são descendentes de um elemento específico. Exemplo: `main section p { color: green; }` seleciona todos os parágrafos que estão dentro de uma seção, que por sua vez está dentro do elemento principal `<main>`, e aplica a cor verde. |
| Seletor de Filho              | `elemento1 > elemento2 { }`      | Seleciona elementos que são filhos diretos de um elemento específico. Exemplo: `main > section { background-color: lightgray; }` seleciona todas as seções que são filhos diretos do elemento principal `<main>` e aplica um fundo cinza claro. |
| Seletor de Irmão Adjacente    | `elemento1 + elemento2 { }`      | Seleciona um elemento que é imediatamente precedido por outro elemento específico. Exemplo: `h1 + p { margin-top: 0; }` seleciona o parágrafo que vem imediatamente após um título `<h1>` e remove a margem superior. |
| Seletor de Irmão Generalizado | `elemento1 ~ elemento2 { }`      | Seleciona elementos que são irmãos de um elemento específico, independentemente de sua posição. Exemplo: `h1 ~ p { color: gray; }` seleciona todos os parágrafos que são irmãos de um título `<h1>` e aplica a cor cinza. |

**Por hoje é só pessoal 😉**
