# Estrutura das CSS
CSS, ou Cascading Style Sheets (Folhas de Estilo em Cascata, em tradução livre), é uma linguagem usada para descrever a apresentação de um documento escrito em HTML ou XML. Com CSS, você pode controlar a aparência visual dos elementos em uma página web, incluindo layout, cores, fontes e espaçamento. CSS permite separar o conteúdo da apresentação, facilitando a manutenção e atualização do design de um site. As regras CSS podem ser aplicadas diretamente no HTML, em um arquivo CSS externo, ou dentro de tags &lt;style&gt; no cabeçalho do documento HTML.

``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu site</title>
</head>
<body>
    <h1>Era uma vez...</h1>
    <h2>Capítulo 1</h2>
    <h3>Capítulo 1.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique beatae...</p>
    <h3>Capítulo 1.2</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus, dolores!...</p>
    <h2>Capítulo 2</h2>
    <h3>Capítulo 2.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta, quam...</p>
</body>
</html>
```

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/5e0ac22c-19f4-4f84-93fb-8d0b10d1c78a) 

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/093570c2-5967-45ea-b4c7-41a79194513d)
(Site com CSS - cores apenas)


## CSS aplicado no próprio código: inline style
A forma mais simples de aplicar CSS é diretamente na própria tag HTML, utilizando o atributo style. No entanto, essa abordagem tem a desvantagem de ser difícil de manter. Por exemplo, se você precisar alterar a cor de fundo de vários textos no site, terá que modificar cada tag individualmente, o que pode ser muito trabalhoso. Apesar disso, essa forma de aplicação possui a maior prioridade na hierarquia de estilos CSS e pode ser muito útil para realizar ajustes específicos e pontuais.

``` html
<body>
    <h1 style="color: blue">Era uma vez...</h1>
    <h2 style="color: red">Capítulo 1</h2>
    <h3>Capítulo 1.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique beatae...</p>
    <h3>Capítulo 1.2</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus, dolores!...</p>
    <h2 style="color: red">Capítulo 2</h2>
    <h3>Capítulo 2.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta, quam...</p>
</body>
```

## CSS aplicado ao cabeçalho: internal style
Para aplicar estilos de forma mais dinâmica e prática, podemos adicionar uma tag &lt;style&gt; dentro da área &lt;head&gt; do nosso documento HTML local. A desvantagem desse método é que ele não aplicará os estilos a outras páginas do site. Se você tiver muitas páginas, precisará duplicar o estilo em cada uma delas, o que pode tornar o código muito extenso e difícil de gerenciar. Além disso, as regras CSS geralmente ocupam mais espaço que o próprio HTML, contribuindo para o aumento do tamanho total do documento.

``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu site</title>
    <style>
      h1 {
         color: blue;
      }
      h2 {
         color: red;
      }
    </style>
</head>
<body>
    <h1>Era uma vez...</h1>
    <h2>Capítulo 1</h2>
    <h3>Capítulo 1.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique beatae...</p>
    <h3>Capítulo 1.2</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus, dolores!...</p>
    <h2>Capítulo 2</h2>
    <h3>Capítulo 2.1</h3>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta, quam...</p>
</body>
</html>
```

## CSS mais versátil: external style
Manter as folhas de estilo fora do código HTML proporciona uma maior organização e permite que os estilos sejam reutilizados de maneira mais eficiente em outras páginas do site. Para isso, utilizamos a tag &lt;link&gt;, especialmente configurada para trabalhar com arquivos de estilo externos. De preferência, coloque essa tag logo abaixo da tag &lt;title&gt; dentro da área <head> do documento.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/0221755d-9ec0-424d-a716-7b70ad926803)

``` html
<link rel="stylesheet" href="style.css">
```

``` css
/* Regra @charset caso haja problemas com acentuação ou línguas com outros alfabetos */
@charset "UTF-8";

h1 {
   color: blue;
}
h2 {
   color: red;
}
```

>[!TIP]
> Nesses exemplos, você aprendeu apenas a trocar a cor da fonte, mas existem muitas outras funções que você pode aplicar na folha de estilo. Elas estão disponíveis nos sites da [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/CSS) e da [W3Schools](https://www.w3schools.com/cssref/index.php).

>[!NOTE]
> Para aplicar estilos globais a todas as tags, basta usar o seletor universal * no CSS. Dê sempre preferência deixá-lo no topo, ou seja, acima do h1 no exemplo acima.

# Planejando um projeto
Tudo começa com a criação do que chamamos de _wireframe_, onde planejamos a estrutura e o comportamento do site. Este wireframe serve como base para o planejamento dos elementos que comporão a página.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/50debdb0-7ac7-46f9-83a5-a3e02ddfb0d4)

>[!TIP]
> Uma ferramenta excelente para projetar seus layouts, seja para sites, aplicativos desktop ou até mesmo apps de celular, é o [MockFlow](https://mockflow.com/). Embora a versão gratuita tenha algumas limitações, ela permite visualizar como o site ficará antes de começar a codificar.

Outro detalhe importante a ser considerado é a responsividade. Mesmo que tenhamos optado por criar um projeto simples, não abriremos mão da versatilidade. Queremos que nosso site possa ser visualizado em dispositivos com diferentes tamanhos de tela. Chamamos essa característica de responsividade. Um site responsivo é capaz de adaptar o tamanho de seus componentes para manter a plena visibilidade em qualquer tela. Geralmente, utilizamos min-width: 400px; (para telas pequenas) e max-width: 800px; (para telas muito grandes) para o elemento &lt;main&gt;.

>[!TIP]
> Também é possível aplicar outras técnicas para aumentar ainda mais a capacidade de adaptação do conteúdo, como as media queries com a regra @media e as caixas flexíveis utilizando flexbox.

Em seguida, decidiremos a paleta de cores a ser utilizada. Por fim, escolheremos as fontes para os destaques principais e para o texto padrão.

# Box model
É um conceito fundamental nas CSS que descreve a estrutura de elementos na web. Cada elemento é representado como uma caixa retangular, e o Box Model define como o espaço é distribuído ao redor do conteúdo de um elemento. Essa estrutura é composta por cinco áreas principais:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/168866cd-5a32-4bee-a513-ce6bc6eafce3)

1. **Content (Conteúdo)**: É a área onde o conteúdo, como texto ou imagens, é exibido. O tamanho desta área pode ser definido pelas propriedades width e height.
2. **Padding (Preenchimento)**: É o espaço entre o conteúdo e a borda. Aumentar o padding expande a caixa do elemento, mas não afeta a cor de fundo ou o tamanho total da caixa. O padding pode ser definido individualmente para cada lado (padding-top, padding-right, padding-bottom, padding-left) ou de forma abreviada (padding).
3. **Border (Borda)**: É a linha ao redor do padding e conteúdo. A borda pode ter largura, estilo e cor específicos, definidos pelas propriedades border-width, border-style e border-color. Assim como o padding, a borda pode ser ajustada individualmente para cada lado ou de forma abreviada (border).
4. **Outline**: É a linha para fora do border.
5. **Margin (Margem)**: É o espaço entre a borda do elemento e os elementos vizinhos. Margens negativas são permitidas e podem causar sobreposição de elementos. As margens também podem ser definidas individualmente para cada lado (margin-top, margin-right, margin-bottom, margin-left) ou de forma abreviada (margin).

>[!NOTE]
> Para centralizar uma caixa, use a seguinte declaração no seu seletor: margin: auto;

>[!TIP]
> A ordem para as duas configurações é sempre a mesma para as shorthands (border e outline): largura(width), estilo(style) e cor(color).

>[!TIP]
> Ao falar de padding e margin nas CSS, podemos imaginar um relógio, seguindo o sentido horário para determinar as direções: começando pelo topo (top), depois direita (right), inferior (bottom) e esquerda (left). Quando você especifica um único valor, ele será aplicado de forma uniforme em todas as direções (topo, direita, inferior e esquerda). Quando você fornece dois valores, o primeiro valor será aplicado ao topo e ao inferior, enquanto o segundo valor será aplicado às laterais (direita e esquerda).

## Tipos de caixa
Nas CSS, os elementos são classificados em dois tipos principais de caixa: block-level e inline-level. Cada tipo possui características distintas que influenciam como os elementos são renderizados e como ocupam espaço na página.

### Block-level Elements
Os elementos de nível de bloco (block-level) são aqueles que ocupam toda a largura disponível do contêiner pai, forçando uma quebra de linha antes e depois do elemento. Exemplos comuns de elementos de nível de bloco incluem &lt;address&gt;, &lt;article&gt;, &lt;aside&gt;, &lt;blockquote&gt;, &lt;canvas&gt;, &lt;dd&gt;, &lt;div&gt;, &lt;dl&gt;, &lt;dt&gt;, &lt;fieldset&gt;, &lt;figcaption&gt;, &lt;figure&gt;, &lt;footer&gt;, &lt;form&gt;, &lt;h1&gt; - &lt;h6&gt;, &lt;header&gt;, &lt;hr&gt;, &lt;li&gt;, &lt;main&gt;, &lt;nav&gt;, &lt;noscript&gt;, &lt;ol&gt;, &lt;p&gt;, &lt;pre&gt;, &lt;section&gt;, &lt;table&gt;, &lt;tfoot&gt;, &lt;ul&gt;, &lt;video&gt; entre outros.

* Sempre começam em uma nova linha.
* Ocupam toda a largura disponível do contêiner pai.
* Podem ter width, height, margin, padding e border aplicados.
* Podem conter outros elementos block-level ou inline-level.

### Inline-level Elements
Os elementos de nível de linha (inline-level) são aqueles que não iniciam uma nova linha e apenas ocupam o espaço necessário para o conteúdo. Eles são renderizados na mesma linha, ao lado de outros elementos inline. Exemplos comuns de elementos de nível de linha incluem &lt;a&gt;, &lt;abbr&gt;, &lt;acronym&gt;, &lt;b&gt;, &lt;bdo&gt;, &lt;br&gt;, &lt;button&gt;, &lt;cite&gt;, &lt;code&gt;, &lt;dfn&gt;, &lt;em&gt;, &lt;i&gt;, &lt;img&gt;, &lt;input&gt;, &lt;kbd&gt;, &lt;label&gt;, &lt;map&gt;, &lt;object&gt;, &lt;output&gt;, &lt;q&gt;, &lt;samp&gt;, &lt;script&gt;, &lt;select&gt;, &lt;small&gt;, &lt;span&gt;, &lt;strong&gt;, &lt;sub&gt;, &lt;textarea&gt;, &lt;tt&gt;, &lt;var&gt;, entre outros.

* Não começam em uma nova linha.
* Ocupam apenas o espaço necessário para o conteúdo.
* As propriedades width e height geralmente não têm efeito.
* Podem ter margin, padding (apenas nas direções esquerda e direita) e border aplicados.
* Podem conter apenas outros elementos inline-level.

## Grouping Tags e Semantic Tags
As grouping tags são usadas para agrupar e organizar o conteúdo em blocos lógicos, ajudando a estruturar o layout de uma página web. Essas tags não carregam significado semântico específico e são mais utilizadas para propósitos de layout e formatação.
* **&lt;div&gt;**: Utilizada para agrupar outros elementos. Serve como um contêiner genérico que não adiciona nenhum estilo ou semântica por padrão. É frequentemente usada para aplicar estilos CSS ou para trabalhar com JavaScript.
* **&lt;span&gt;**: Similar ao &lt;div&gt;, mas é um contêiner inline. Usada para aplicar estilos a partes específicas do texto ou para agrupar elementos inline.


As semantic tags foram introduzidas no HTML5 para adicionar significado ao conteúdo, melhorando a acessibilidade e a otimização para motores de busca. Essas tags indicam claramente o propósito do conteúdo que envolvem, tornando o código mais legível e compreensível tanto para desenvolvedores quanto para navegadores e leitores de tela.
* **&lt;header&gt;**: Cria áreas relativas a cabeçalhos. Pode ser o cabeçalho principal de um site ou até mesmo o cabeçalho de uma seção ou artigo. Normalmente inclui títulos &lt;h1&gt; - &lt;h6&gt; e subtítulos. Podem também conter menus de navegação, o &lt;nav&gt;.
* **&lt;main&gt;**: É um agrupador usado para delimitar o conteúdo principal do nosso site. Normalmente concentra as seções, artigos e conteúdos periféricos.
* **&lt;section&gt;**: Cria seções para sua página. Ela pode conter o conteúdo diretamente no seu corpo ou dividir os conteúdos em artigos com conteúdos específicos. Segundo a documentação oficial da W3C, "uma seção é um agrupamento temático de conteúdos, tipicamente com um cabeçalho".
* **&lt;article&gt;**: É um elemento que vai conter um conteúdo que pode ser lido de forma independente e dizem respeito a um mesmo assunto. Podemos usar um &lt;article&gt; para delimitar um post de blog ou fórum, uma notícia, etc.
* **&lt;aside&gt;**: Delimita um conteúdo periférico e complementar ao conteúdo principal de um artigo ou seção. Normalmente um conteúdo &lt;aside&gt; está posicionado ao lado de um determinado texto ou até mesmo no meio dele, exatamente como fizemos no bloco de texto apresentado anteriormente, falando sobre "MÚLTIPLOS NÍVEIS".
* **&lt;footer&gt;**: Cria um rodapé para o site inteiro, seção ou artigo. É um conteúdo que não faz parte diretamente do conteúdo nem é um conteúdo periférico (o que caracteriza um &lt;aside&gt;), mas possui informações sobre autoria do conteúdo, links adicionais, mapa do site, documentos relacionados.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/689262c6-2536-4424-964e-f1075c181eb7)

>[!NOTE]
> É possível ter um ou mais &lt;article&gt; dentro de uma &lt;section&gt; ou até mesmo criar &lt;section&gt; dentro de um &lt;article&gt;, a isso chamamos de aninhamento. Não existem limitações para a sua criatividade!

>[!TIP]
> Podemos adicionar sombras e arredondar elementos usando os comandos box-shadow e border-radius, respectivamente. Para criar bordas personalizadas, utilize o comando border-image.

### Importante para a(o)
* **Acessibilidade**: Melhora a experiência de usuários que dependem de tecnologias assistivas, como leitores de tela.
* **SEO**: Ajuda os motores de busca a entender melhor a estrutura e o conteúdo da página.
* **Manutenção**: Torna o código mais legível e organizado, facilitando a manutenção e a colaboração entre desenvolvedores.

# Cores
As cores têm um impacto significativo em nossas emoções e comportamentos. A psicologia das cores estuda como as diferentes cores influenciam nossas percepções e sentimentos. Por exemplo, o vermelho pode evocar sensações de urgência ou excitação, enquanto o verde é frequentemente associado à calma e à natureza.

Cor | Associada a | Usar em | Evitar
--- | --- | --- | ---
Vermelho | Amor, emoção energia, raiva e perigo | Comida, moda, entretenimento, serviços de emergência e saúde | Luxo, natureza e serviços em geral
Amarelo | Felicidade, alegria, otimismo e covardia | Dar luz, dar calma, felicidade e chamar atenção | Pode indicar que algo é barato ou spam
Laranja | Divertimento, ambição, calor e cautela | Comércio eletrônico, entretenimento e call-to-action | Pode se tornar cansativo se muito explorado
Verde | Saúde, natureza, dinheiro, sorte e inveja | Relaxamento, turismo, financeiros e meio ambiente | Luxo, tecnologia e meninas adolescentes
Azul | Competência, sabedoria, calma e frio | Tecnologia, medicina, ciências e governo | Comida (reduz apetite)
Roxo | Criatividade, poder, sabedoria e mistério | Produtos de beleza, astrologia, ioga, espiritualidade e adolescente | Não prende muito a atenção e é indiferente
Marrom | Terra, robustez, estabilidade e amizade | Alimentação, imobiliária, animais e finanças | Cor considerada conservadora
Preto | Elegância, autoridade, mistério e morte | Luxo, moda, marketing e cosméticos | Desconforto e medo
Branco | Pureza, limpeza, felicidade e segurança | Medicina, saúde, tecnologia, luxo (com preto, ouro e/ou cinza) | Não chama atenção (deve ser combinado)
Cinza | Formalidade, sofisticação, frieza e indiferença | Bens de luxo e efeito calmante | Dá a sensação de frieza
Rosa | Amor, romance, sinceridade e cuidados | Produtos femininos e cosméticos | Pode tornar muito sentimental e doce

>[!NOTE]
> A cor azul é amplamente aceita, com 46% dos homens e 44% das mulheres a preferindo, conforme pesquisas. Além disso, a rejeição do azul é extremamente baixa, variando entre 1% e 2%. Essa alta aceitação e baixa rejeição fazem do azul uma escolha popular em diversas aplicações, desde design de interiores até branding e moda.

## Círculo cromático

O círculo cromático é uma ferramenta visual que mostra a relação entre as cores. Ele é usado para criar esquemas de cores harmoniosos, como cores complementares (opostas no círculo) ou análogas (adjacentes no círculo). Isso ajuda designers e artistas a selecionar combinações de cores que funcionem bem juntas e transmitam a mensagem desejada.

As cores primárias são as bases de todas as outras cores e incluem amarelo, vermelho e azul. A partir dessas cores, podemos criar as cores secundárias, que são combinações de duas cores primárias:
* Laranja (vermelho + amarelo)
* Violeta/Roxo (vermelho + azul)
* Verde (azul + amarelo)

As cores terciárias são criadas misturando uma cor primária com uma cor secundária adjacente, resultando em tons frequentemente conhecidos como cores pastéis.

![image](https://upload.wikimedia.org/wikipedia/commons/7/74/Rgb-colorwheel.svg)

### Cores frias e quentes 
As cores podem ser classificadas como frias ou quentes, dependendo de suas propriedades visuais e emocionais.
* **Cores Quentes**: Incluem vermelho, laranja e amarelo. São associadas a sentimentos de energia, calor e entusiasmo, sendo frequentemente usadas para atrair atenção ou criar uma sensação de aconchego.
* **Cores Frias**: Incluem azul, verde e violeta. São associadas a sensações de calma, serenidade e tranquilidade, sendo ideais para ambientes relaxantes e serenos.

Na imagem abaixo, podemos ver a divisão entre as cores frias (cool colors) e quentes (warm colors), ajudando a entender melhor suas aplicações e efeitos emocionais em diferentes situações.

![Círculo cromático](https://upload.wikimedia.org/wikipedia/commons/f/fe/Warm_and_cool_colors.svg)

### Harmonia das cores
Refere-se à combinação equilibrada e agradável de cores, criando uma estética visualmente atraente e coerente. Existem várias formas de alcançar a harmonia das cores, e algumas das mais comuns são:
* **Harmonia Complementar:** Emprega cores que estão opostas no círculo cromático. Esse contraste forte pode criar um visual vibrante e dinâmico. Exemplo: Azul, vermelho-laranja e amarelo-laranja.
* **Harmonia Análoga:** Utiliza cores que são adjacentes no círculo cromático. Essas combinações são naturalmente harmoniosas e proporcionam um efeito suave e agradável. Exemplo: Azul, azul-verde e verde.
* **Harmonia Triádica:** Usa três cores equidistantes no círculo cromático, criando um visual vibrante e equilibrado, com bastante contraste e diversidade. Exemplo: Vermelho, amarelo e azul.
* **Harmonia Tetrádica:** Inclui duas pares de cores complementares, criando uma paleta rica e diversificada. Pode ser desafiador equilibrar, mas resulta em combinações dinâmicas e atraentes. Exemplo: Azul e laranja, vermelho e verde.
* **Harmonia Monocromática:** Usa variações de uma única cor, alterando apenas o brilho e a saturação. Isso cria um visual unificado e elegante. Exemplo: Vários tons de azul.

## Criação da paleta de cores
Ter uma paleta de cores bem definida é fundamental para o desenvolvimento de um site, pois ela garante consistência visual, fortalece a identidade da marca e melhora a experiência do usuário. Uma paleta de cores harmoniosa facilita a navegação, destaca elementos importantes e cria uma estética atraente e profissional. O número ideal de cores em uma paleta geralmente varia entre 3 a 5 cores, o que permite variedade suficiente para criar contraste e interesse visual sem sobrecarregar o design.
* [Extensão Chrome - Seletor de cores](https://chromewebstore.google.com/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp)
* [Crie a sua roda de cores - Adobe Color](https://color.adobe.com/create/color-wheel)
* [Paletton - Crie uma paleta de cores e visualize como ela ficaria no seus site](https://paletton.com/)
* [Coolors - Gerador de paletas de cores](https://coolors.co/generate)

>[!NOTE]
> O design sempre considera três elementos essenciais que devem estar em alta qualidade: imagens, cores e tipografia (representações gráficas).
 
## Representação de cores nas CSS
  Nas CSS, as cores podem ser representadas de várias maneiras, permitindo uma flexibilidade considerável na criação de estilos e temas. Aqui estão as formas mais comuns de definir cores em CSS: **Nomes de cor**, **Valores hexadecimais**, **Valores em RGB (Red, Green e Blue)** e **Característica em HSL (Hue, Saturation e Luminosity).**

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d9e5c48a-2f9c-424e-a78b-d7cc9ed8d8ac) (Efeito visual idêntico)

``` css
/* Regra @charset caso haja problemas com acentuação ou línguas com outros alfabetos */
@charset "UTF-8";

h1 {
   color: brown;
}
h2 {
   color: #a52a2a;
}
h3 {
   color: rgb(165, 42, 42);
}
h4 {
   color: hsl(0, 59%, 41%);
}
```

>[!TIP]
> A escolha do método de representação depende das necessidades do projeto. Valores hexadecimais são compactos e frequentemente usados, enquanto RGBA e HSLA oferecem controle adicional sobre a opacidade.

## Como adicionar um fundo normal e com gradiente de cores
Para adicionar um plano de fundo normal a um elemento em CSS, você usa a propriedade background-color para definir a cor de fundo desejada.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/5f242d09-bbc3-4e43-817c-135488f08859)

``` css
/* Regra @charset caso haja problemas com acentuação ou línguas com outros alfabetos */
@charset "UTF-8";

body {
   background-color: black;
}
h1 {
   color: white;
}
```

Para adicionar um gradiente como plano de fundo, você utiliza a propriedade background-image com a função linear-gradient ou radial-gradient.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/211cd14a-a45f-49b3-a76b-77e4eb16401b)

``` css
/* Regra @charset caso haja problemas com acentuação ou línguas com outros alfabetos */
@charset "UTF-8";

/* Seletor global */
* {
   height: 100%;
   background-attachment: fixed;
}

body {
   background-image: linear-gradient(to top, #03000D, #1F2326, #363C40, #4F5559, #0D0D0D;
}
h1 {
   color: white;
}
```

Além das configurações de plano de fundo temos outras configurações pontuais que podemos fazer, por exemplo:
* font-family: Tipo de fonte
* color: Altera a cor da fonte
* border-radius: Borda arrendodada
* box-shadow: Sombreamento de caixa
* width: Tamanho geral do seletor
* padding: Afasta de todas as bordas do seletor
* margin: auto; Centraliza o conteúdo (responsivo)
* text-shadow: Sombreaemnto de texto
* text-align: Alinhamento de texto

>[!TIP]
> Evite usar fundo preto com texto branco em grandes blocos de texto, pois essa combinação pode causar cansaço visual. Prefira um fundo branco com texto preto, de preferência com fontes não serifadas e com um peso leve (font-weight).

# Fontes
A escolha de uma boa paleta de cores não é o único aspecto crucial na construção de um site. Também é fundamental selecionar as famílias tipográficas adequadas. As fontes podem transmitir emoções e influenciar a experiência do usuário. Geralmente, é importante priorizar a legibilidade e a clareza ao escolher uma fonte, mas também devemos considerar o efeito desejado. Por exemplo, fontes serifadas podem transmitir tradição e seriedade, enquanto fontes sans-serif são frequentemente associadas à modernidade e simplicidade. Além disso, combinar diferentes tipos de fontes pode adicionar hierarquia e contraste, tornando o conteúdo mais atraente e fácil de navegar.

* **Fontes serifadas** são categorias de fontes clássicas, surgidas na época das prensas de impressão de livros. Tipicamente, os caracteres serifados foram amplamente aplicados em grandes blocos de texto impressos em papel, aproveitando uma característica da nossa percepção: nós não lemos as palavras letra por letra, mas como um conjunto. As serifas têm a capacidade de guiar nossos olhos graças aos pequenos prolongamentos que criam, fazendo com que as letras se "juntem" em palavras. Atualmente, evitamos usar fontes serifadas para apresentar textos longos na Web, pois as tendências modernas favorecem fontes visualmente mais leves. No entanto, as fontes serifadas são bastante usadas em títulos, pois chamam mais atenção devido às suas características distintivas.
* **Fontes não serifadas**, ou **sans-serif** (do francês "sem serifa"), são fontes que, como o nome sugere, não apresentam serifas. As primeiras fontes dessa categoria surgiram em 1816, mas foram consideradas avançadas demais para a época. Anos depois, ressurgiram em versões melhoradas e vieram para ficar, especialmente na Web. Isso ocorre porque elas são excelentes para exibição em telas e monitores, transmitindo uma sensação de limpeza, clareza e organização.
* **Fontes monoespaçadas** surgiram como uma variação das fontes serifadas e não serifadas. Elas possuem a característica de ter a mesma largura para todas as letras, garantindo uniformidade no espaçamento.
* **Fontes script** ou **handwriting** são aquelas que tentam imitar a escrita humana. Seu uso deve ser bem controlado e jamais devem ser aplicadas a textos muito longos, pois causam cansaço visual e se tornam difíceis de ler.
* **Fontes display** fogem completamente das definições feitas pelas classificações anteriores. Elas são fontes com muitos efeitos visuais, enfeitadas e até mesmo curiosas. Também são chamadas de **fontes comemorativas** e algumas delas sequer representam letras, podendo ser desenhos de animais, objetos, pessoas, personagens de quadrinhos, etc.

### Como aplicar fontes as CSS?
As fontes em CSS são aplicadas principalmente através da propriedade font-family. Essa propriedade permite que você especifique uma lista de fontes, onde a primeira fonte disponível no dispositivo do usuário será usada. Além disso, você pode ajustar vários aspectos das fontes com outras propriedades CSS, como font-size, font-weight, e font-style.

``` css
body {
   font-family: "Arial", "Helvetica", sans-serif;
   font-size: 16px;
   font-weight: normal;
   font-style: normal;
}
```

A ordem aqui é importante: se a primeira fonte não for encontrada no dispositivo, o navegador tentará carregar a segunda, e assim por diante. O último item na lista é um tipo genérico de fonte. Podemos também fazer um atalho para todos esses comandos utilizando a propriedade font, prestando atenção na ordem dos valores.

``` css
body {
   font: italic bold 16px/1.5 "Arial", "Helvetica", sans-serif;
}
```

1. font-style é o estilo da fonte, por exemplo: italic, normal, oblique etc.
2. font-variant é a variante da fonte.
3. font-weight é o peso da fonte, ou seja se ela vai está em negrito ou "mais fina", por exemplo: lighter, normal, bold ou bolder. Nesse caso também são aceitos valores de 100 a 900.
4. font-size ou line-height é relativo ao tamanho da fonte, geralmente utilizamos px (pixel) ou em (medida recomendada pela W3C).
5. font-family é relativo a família da fonte.

Além da font-family, você pode usar @font-face para importar fontes externas, por exemplo, do [Google fonts](fonts.google.com) ou [DaFont](dafont.com):

``` css
@font-face {
   font-family: 'nome da fonte';
   src: url('nome do arquivo da fonte') format('formato do arquivo');
}

body {
   font-family: 'nome da fonte', sans-serif;
}
```

Além disso, você pode incorporar um estilo embutido na primeira linha da sua tag &lt;style&gt;, seja dentro do próprio arquivo .html ou em uma folha de estilo separada (.css).

>[!NOTE]
> Os formatos geralmente aceitos são o opentype (.otf) e  o truetype (.ttf), mas também existem formatos como embedded-opentype, truetype-aat (Apple Advanced Typography) e .svg (muito usado com legendas)

>[!TIP]
> Se você quiser extrair uma fonte, uma extensão do Google Chrome muito útil é a [Ninja Fonts](https://www.fonts.ninja/). Você também pode encontrar mais detalhes sobre as fontes que estão em imagens em sites como [WhatFontIs (a melhor das opções)](whatfontis.com), [FontSquirrel](fontsquirrel.com) ou [MyFonts.com](myfonts.com). Recomendo utilizar essas ferramentas em conjunto para obter sempre o melhor resultado.

# Seletores personalizados
Às vezes, precisamos ser mais específicos quanto às modificações que queremos fazer nos elementos. É aí que entram os seletores personalizados. Antes de falar sobre isso, precisamos entender que utilizamos o id no HTML e # no CSS para identificar um elemento. Segundo a regra da W3C, só devemos ter um id por seletor em um documento. Já se quisermos agrupar várias características que serão usadas em diversos elementos específicos, podemos usar class no HTML e . no CSS. Veja abaixo como isso funciona:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a4ba1102-19d8-4de9-b97a-f84c423acb55)

``` html
<body>
   <h1>Primeiro</h1>
   <h1 id="seg">Segundo</h1>
   <h1 class="ter">Terceiro</h1>
</body>
```

``` css
/* Regra @charset caso haja problemas com acentuação ou línguas com outros alfabetos */
@charset "UTF-8";

h1 {
   color: black;
}

h1#seg {
   color: red;
}

/* Ou .ter */
h1.ter {
   color: blue;
}
```

A hierarquia em CSS é baseada em IDs e classes. Seletores de ID (#id) têm maior prioridade que seletores de classe (.classe). Portanto, tudo que estiver dentro de um ID será considerado primeiro que tudo que estiver dentro de uma classe. Preste atenção à ordem e especificidade ao inserir os parâmetros.

>[!NOTE]
> Evite dar nomes às classes e ids baseados na aparência visual dos elementos. Em vez disso, nomeie-os de acordo com a funcionalidade ou propósito dos elementos.

>[!TIP]
> Podemos utilizar a tag &lt;span&gt; para fazer configurações pontuais em determinados trechos de texto. Tudo o que estiver dentro do &lt;span&gt; será considerado como pertencente à classe ou id especificado. Além disso, podemos adicionar mais de uma classe dentro do atributo class="x y" separando os nomes das classes por espaços.

>[!TIP]
> Existe também um seletor especial nas CSS, o asterisco (*). Ele tem uma função importante, pois aplica uma configuração padrão a todos os elementos do código HTML ao qual o estilo está sendo aplicado. Geralmente, utilizamos esse seletor para definir background-color, margin: 0px; e padding: 0px;, criando um layout mais personalizado que cubra toda a tela.

## Pseudo-classe
Utilizamos o sinal de : para determinar uma pseudo-classe, que é aplicada a um elemento ou classe, relativa ao seu estado. Por exemplo, ao utilizar :hover, podemos definir um estilo que será aplicado quando o usuário passar o mouse sobre o elemento. Existem várias pseudo-classes que podemos usar além de :hover. Veja alguns exemplos [aqui](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-classes).
* :hover : Aplica o estilo quando o mouse está sobre o elemento.
* :focus : Aplica o estilo quando o elemento está focado (ex.: um campo de texto clicado).
* :active : Aplica o estilo quando o elemento está sendo clicado.
* :visited : Aplica o estilo a links que já foram visitados.
* :nth-child(n) : Aplica o estilo ao enésimo filho de um elemento pai.

>[!NOTE]
> Se criarmos uma &lt;div&gt;, que é um espaço em branco funcionando como um contêiner, podemos trabalhar com seletores internos utilizando 'filhos' ou children. Isso funciona da seguinte forma: div > p. Isso significa que o estilo será aplicado a todos os elementos &lt;p&gt; que são filhos diretos da &lt;div&gt;.

>[!TIP]
> text-decoration: none; irá remover todos os efeitos do texto, inclusive o sublinhado dos links.

``` html
<!--HTML5-->
<body>
   <div class="container">
      <p>Este parágrafo está dentro da div.</p>
   </div>
</body>
```

``` css
/* CSS3 */
.container > p {
   color: blue;
   font-weight: bold;
}
```

Utilizar seletores de filhos é importante para aplicar estilos de maneira específica e organizada, evitando a necessidade de classes adicionais desnecessárias. Isso permite um código CSS mais limpo e fácil de manter, garantindo que os estilos sejam aplicados somente onde desejado.

## Declarando uma variável
Embora CSS não seja uma linguagem de programação, podemos declarar variáveis que facilitam muito nosso trabalho. Para criar variáveis para nossas configurações, devemos definir uma área de definições dentro do estilo usando a pseudo-classe :root. Essa pseudo-classe define configurações na raiz do documento, aplicando-as a todo o documento.

``` css
:root {
   --cor0: #c5ebd6;
   --cor1: #83E1AD;
   --cor2: #3DDC84;
   --cor3: #2FA866;
   --cor4: #1A5C37;
   --cor5: #063d1e;
   --fonte0: Arial, Helvetica, sans-serif;
   --fonte1: 'Bebas Neue', cursive;
   --fonte2: 'Android', sans-serif;
}
```

A partir de agora, definir cores e fontes em nossos elementos HTML ficará mais fácil e personalizável, utilizando a função var().

``` css
body {
   font-family: var(--fonte0);
   color: var(--cor0);
   background-color: var(--cor1);
}
```

## Pseudo-elementos
São usados em CSS para aplicar estilos a partes específicas de elementos sem precisar adicionar classes ou IDs adicionais ao HTML. Eles permitem selecionar e estilizar subpartes de elementos, oferecendo um controle mais refinado sobre a aparência do conteúdo. Utilizamos o sinal :: para pseudo-elementos.
* ::before e ::after são usados para inserir conteúdo antes ou depois do conteúdo real de um elemento. Eles são frequentemente utilizados para adicionar ícones, gráficos ou texto decorativo.

``` css
.container::before {
   content: "Início: ";
   color: green;
}

.container::after {
   content: " Fim.";
   color: red;
}
```

Confira mais exemplos [aqui](https://developer.mozilla.org/pt-BR/docs/Web/CSS/Pseudo-elements).

## Tabelas
As tabelas em CSS são estilizadas para melhorar a aparência e a legibilidade dos dados tabulares em uma página web. Utilizando CSS, podemos adicionar cores, bordas, espaçamento e outras características visuais que tornam as tabelas mais atraentes e fáceis de ler. Aqui estão alguns aspectos importantes sobre a estilização de tabelas com CSS:

* **width:** A propriedade width define a largura de um elemento. Pode ser especificada em várias unidades, como pixels (px), porcentagem (%), ems (em), rems (rem), entre outras. No contexto de tabelas, pode ser usada para ajustar a largura de toda a tabela ou de colunas específicas.
* **border-collapse:** A propriedade border-collapse é usada para definir se as bordas das células de uma tabela devem ser colapsadas em uma única borda ou separadas. Tem dois valores principais:
   - collapse: Colapsa as bordas de tabelas adjacentes, removendo o espaço entre elas e combinando as bordas em uma única borda.
   - separate: Mantém as bordas das células separadas, criando um espaço entre elas (padrão).
* **border:** A propriedade border é uma abreviação que permite definir o estilo, a largura e a cor da borda de um elemento em uma única linha. No contexto de tabelas, é frequentemente usada para adicionar bordas às células (<th> e <td>) e à própria tabela.
* **text-align:** A propriedade text-align define o alinhamento horizontal do conteúdo de um elemento de bloco, como texto e outros elementos inline dentro de um <th> ou <td>. Os valores comuns são:
  - left: Alinha o texto à esquerda (padrão).
  - right: Alinha o texto à direita.
  - center: Centraliza o texto.
  - justify: Justifica o texto, ajustando o espaçamento para que o texto ocupe toda a largura disponível.
* **vertical-align:** A propriedade vertical-align define o alinhamento vertical do conteúdo dentro de um elemento de linha de tabela (<td> ou <th>) ou inline-block. Os valores comuns são:
  - top: Alinha o conteúdo ao topo da célula.
  - middle: Alinha o conteúdo ao meio da célula (padrão para tabelas).
  - bottom: Alinha o conteúdo à base da célula.
  - baseline: Alinha o conteúdo com a linha de base do texto dos elementos adjacentes.

``` css
table {
   border: 1px solid black;
}

caption {
   border: 1px solid red;
}

thead tr td {
   border: 1px solid blue;
}

tbody tr td {
   border: 1px solid yellow;
}

tfoot tr td {
   border: 1px solid purple;
}
```

 ![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/7a3dfd9b-e757-4c9b-bac2-b1166608eadf)

``` css
table {
   border: 1px solid black;
   border-collapse: collapse;
}

caption {
   border: 1px solid red;
}

thead tr td {
   border: 1px solid blue;
}

tbody tr td {
   border: 1px solid yellow;
}

tfoot tr td {
   border: 1px solid purple;
}
```

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6720be2f-a747-4458-9c6b-c9132817cc5f)


### Efeito zebrado
Para criar um efeito zebrado usamos a pseudo-classe --> :nth-child(nº de linhas). Vejamos um exemplo:

``` css
thead tr td {
   border: 1px solid blue;
}

thead tr td:nth-child(2n) {
   background-color: gray;
}

tbody tr td {
   border: 1px solid yellow;
}

tbody tr td:nth-child(2n-1) {
   background-color: yellow;
}
```

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/515d8783-1240-4282-8143-2c0f74f8a23b)

### Responsividade de tabelas
Quando se trata de tabelas, a responsividade é essencial para garantir que os dados sejam apresentados de forma clara e acessível em dispositivos com diferentes tamanhos de tela. Uma técnica comum para tornar tabelas responsivas é envolver a tabela em um contêiner &lt;div&gt; e ajustar seu estilo usando a propriedade overflow.

**Envolvendo a Tabela em um Contêiner &lt;div&gt;:**
Envolver a tabela em um contêiner &lt;div&gt; permite aplicar estilos de rolagem quando a tabela excede a largura da tela do dispositivo. Isso é especialmente útil em dispositivos móveis onde o espaço horizontal é limitado.

**Usando overflow**
A propriedade overflow é usada para controlar o comportamento de rolagem do conteúdo dentro de um contêiner. As opções mais comuns são:

* overflow-x: Controla a rolagem horizontal. Para tabelas, overflow-x é frequentemente usado para permitir a rolagem horizontal.
* overflow-y: Controla a rolagem vertical.
* overflow: Controla a rolagem em ambas as direções.

# Media queries
Media queries são uma funcionalidade do CSS3 que permitem aplicar estilos diferentes a um documento HTML com base em características específicas do dispositivo, como largura, altura, orientação da tela, e tipo de mídia (por exemplo, tela ou impressora). Isso possibilita a criação de designs responsivos, que se adaptam a diferentes tamanhos e tipos de dispositivos.

As media queries são definidas usando a regra @media no CSS.

``` html
<!--HTML5-->
<link rel="stylesheet" media="(max-width: 800px)" href="style.css">
```

``` css
/* CSS3 */

@media (max-width: 600px) {
   .facet_sidebar {
      display: none;
   }
}
```

## Versão para impressora
Para aplicar estilos específicos ao imprimir um documento, você pode usar a media query print. Isso garante que o conteúdo seja exibido corretamente ao ser impresso.

>[!NOTE]
> Em @media print {} o background-image não funciona.

## Conceito de Mobile First
O conceito de "Mobile First" é uma abordagem de design que prioriza a experiência em dispositivos móveis antes de se concentrar em telas maiores, como tablets e desktops. A ideia é começar a escrever o CSS para os menores dispositivos e, em seguida, adicionar media queries para ajustar o layout e a funcionalidade para dispositivos maiores.

## Breakpoints típicos para dispositivos (Typical devices breakpoints)
Breakpoints são pontos definidos em uma folha de estilo CSS que especificam onde o layout de uma página deve mudar em resposta ao tamanho da tela ou a outras características do dispositivo. Eles são essenciais para criar designs responsivos, que se adaptam perfeitamente a diferentes dispositivos e tamanhos de tela.

>[!NOTE]
> * Telas pequenas até 600px
> * Celulares de 600px até 768px
> * Tablets de 768px até 992px
> * Desktops de 992px até 1200px
> * Telas grandes acima de 1200px

Aprenda mais sobre media query na documentação da linguagem disponível [aqui](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_media_queries/Using_media_queries).

# Flexbox (CSS Flexible Box Module Level 1)
Flexbox é um layout de CSS3 projetado para fornecer uma maneira mais eficiente de distribuir espaço e alinhar itens dentro de um container, especialmente quando o tamanho dos itens é desconhecido ou dinâmico. O módulo Flexbox oferece um conjunto de propriedades que permitem criar layouts flexíveis e responsivos sem a necessidade de flutuações e posicionamento complexo.

**Benefícios do Flexbox**
1. **Layout Direcional:** Flexbox permite que os elementos sejam alinhados em várias direções - horizontalmente ou verticalmente.
2. **Espaçamento Consistente:** Ele distribui o espaço de forma igual ou proporcional entre os elementos, garantindo um espaçamento consistente.
3. **Alinhamento Centralizado:** Facilita o alinhamento centralizado de itens tanto no eixo principal quanto no eixo cruzado.
4. **Reordenamento dos Itens:** Permite reordenar visualmente os itens sem alterar a ordem do código HTML.
5. **Adaptabilidade:** Flexbox é ideal para layouts dinâmicos onde o tamanho dos itens pode variar.

**Comparando com media queries**
* **Media Queries:** Usadas para aplicar diferentes estilos baseados nas características do dispositivo, como largura da tela. Elas são essenciais para criar layouts responsivos que se adaptam a diferentes dispositivos.
* **Flexbox:** Proporciona um layout flexível dentro de um container, ajudando a distribuir e alinhar itens de forma eficiente. Flexbox complementa media queries ao fornecer ferramentas para organizar e alinhar elementos dentro dos diferentes layouts definidos pelas media queries.

## Contêiner Flexível (Flex Container)
No modelo de layout Flexbox em CSS, os contêineres são divididos em dois tipos principais: o contêiner pai (ou contêiner flex) e os contêineres filhos (ou itens flex).

### Contêiner Pai (Contêiner Flex)
O contêiner pai é o elemento que possui a propriedade ```display: flex```. Quando essa propriedade é aplicada, o contêiner pai se transforma em um contêiner flex, permitindo que todos os seus elementos filhos se comportem de acordo com as regras do Flexbox. O contêiner pai define o contexto em que os itens flexíveis (filhos) serão dispostos e controlados.

**Eixos no Flexbox**
* **Eixo Principal (Main Axis):** É o eixo ao longo do qual os itens flexíveis são colocados. Pode ser horizontal ou vertical, dependendo da propriedade flex-direction.
* **Eixo Cruzado (Cross Axis):** É perpendicular ao eixo principal. Se o eixo principal for horizontal, o eixo cruzado será vertical, e vice-versa.

**Principais propriedades aplicadas ao contêiner pai:**
- ```flex-direction```: Define a direção em que os itens flexíveis serão dispostos (em linha, em coluna, etc.).
- ```justify-content```: Controla o alinhamento dos itens ao longo do eixo principal (horizontal por padrão).
- ```align-items```: Controla o alinhamento dos itens ao longo do eixo transversal (vertical por padrão).
- ```flex-wrap```: Permite que os itens sejam quebrados em várias linhas, se necessário.
- ```align-content```: Controla o espaçamento entre as linhas do contêiner quando há múltiplas linhas de itens flexíveis.

![image](https://github.com/ReisLeonardo/html-css/assets/89877899/3b92e909-8065-4dcf-8428-de91419c15da)

![image](https://github.com/ReisLeonardo/html-css/assets/89877899/a1740b52-e73d-422c-a834-348ed2dbaaa3)

### Contêineres Filhos (Itens Flex)
Os contêineres filhos, ou itens flex, são os elementos diretos dentro de um contêiner pai flexível. Esses itens herdam o comportamento flexível e podem ser controlados individualmente usando várias propriedades CSS. Eles são dispostos de acordo com as regras estabelecidas pelo contêiner pai.

**Principais propriedades aplicadas aos contêineres filhos:**
- ```flex-grow```: Define a capacidade de um item de crescer para preencher o espaço disponível no contêiner.
- ```flex-shrink```: Controla o quanto um item pode encolher quando o espaço no contêiner é limitado.
- ```flex-basis```: Especifica o tamanho inicial de um item antes de ele crescer ou encolher.
- ```align-self```: Permite que um item seja alinhado de forma diferente dos outros ao longo do eixo transversal.
- ```order```: Determina a ordem de exibição dos itens, independentemente da ordem em que aparecem no HTML.

Aprenda mais sobre flexbox na documentação da linguagem disponível [aqui](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox).
