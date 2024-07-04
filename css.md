# Estrutura das CSS
CSS, ou Cascading Style Sheets (Folhas de Estilo em Cascata, em tradução livre), é uma linguagem usada para descrever a apresentação de um documento escrito em HTML ou XML. Com CSS, você pode controlar a aparência visual dos elementos em uma página web, incluindo layout, cores, fontes e espaçamento. CSS permite separar o conteúdo da apresentação, facilitando a manutenção e atualização do design de um site. As regras CSS podem ser aplicadas diretamente no HTML, em um arquivo CSS externo, ou dentro de tags &lt;style&gt; no cabeçalho do documento HTML.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/5e0ac22c-19f4-4f84-93fb-8d0b10d1c78a) 
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/59717da5-9bda-453b-8c84-3eda0c052c67)
(Site sem CSS)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/093570c2-5967-45ea-b4c7-41a79194513d)
(Site com CSS - cores apenas)


## CSS aplicado no próprio código: inline style
A forma mais simples de aplicar CSS é diretamente na própria tag HTML, utilizando o atributo style. No entanto, essa abordagem tem a desvantagem de ser difícil de manter. Por exemplo, se você precisar alterar a cor de fundo de vários textos no site, terá que modificar cada tag individualmente, o que pode ser muito trabalhoso. Apesar disso, essa forma de aplicação possui a maior prioridade na hierarquia de estilos CSS e pode ser muito útil para realizar ajustes específicos e pontuais.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/8e712d8c-c37f-428b-82ca-ae4bb2e18b98)

## CSS aplicado ao cabeçalho: internal style
Para aplicar estilos de forma mais dinâmica e prática, podemos adicionar uma tag &lt;style&gt; dentro da área &lt;head&gt; do nosso documento HTML local. A desvantagem desse método é que ele não aplicará os estilos a outras páginas do site. Se você tiver muitas páginas, precisará duplicar o estilo em cada uma delas, o que pode tornar o código muito extenso e difícil de gerenciar. Além disso, as regras CSS geralmente ocupam mais espaço que o próprio HTML, contribuindo para o aumento do tamanho total do documento.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/f074a89e-6858-439b-a433-305be2fbee23)

## CSS mais versátil: external style
Manter as folhas de estilo fora do código HTML proporciona uma maior organização e permite que os estilos sejam reutilizados de maneira mais eficiente em outras páginas do site. Para isso, utilizamos a tag &lt;link&gt;, especialmente configurada para trabalhar com arquivos de estilo externos. De preferência, coloque essa tag logo abaixo da tag &lt;title&gt; dentro da área <head> do documento.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/0221755d-9ec0-424d-a716-7b70ad926803)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/9bf3c6bb-4025-4f09-8b11-f38112480bd5) (Você pode escolher outro diretório como sua folha de estilo)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/3b3d56c4-00f6-4e6c-ac8c-a51badc38a17)

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

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/4a136aaf-e6d1-4700-9b04-105ea9b7174f) (style.css)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d9e5c48a-2f9c-424e-a78b-d7cc9ed8d8ac) (Efeito visual idêntico)

>[!TIP]
> A escolha do método de representação depende das necessidades do projeto. Valores hexadecimais são compactos e frequentemente usados, enquanto RGBA e HSLA oferecem controle adicional sobre a opacidade.

## Como adicionar um fundo normal e com gradiente de cores
Para adicionar um plano de fundo normal a um elemento em CSS, você usa a propriedade background-color para definir a cor de fundo desejada.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/5f242d09-bbc3-4e43-817c-135488f08859)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d3971203-5de8-4822-8ab3-8672ab90c6fa)

Para adicionar um gradiente como plano de fundo, você utiliza a propriedade background-image com a função linear-gradient ou radial-gradient.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/211cd14a-a45f-49b3-a76b-77e4eb16401b)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/34b48429-5612-4845-a117-aed92cd04045)

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

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/94347430-0b16-421a-8ac7-07f2e55fe6db)

A ordem aqui é importante: se a primeira fonte não for encontrada no dispositivo, o navegador tentará carregar a segunda, e assim por diante. O último item na lista é um tipo genérico de fonte. Podemos também fazer um atalho para todos esses comandos utilizando a propriedade font, prestando atenção na ordem dos valores.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/7fac3dca-ae84-4c63-b074-6c656da82262)

1. font-style é o estilo da fonte, por exemplo: italic, normal, oblique etc.
2. font-variant é a variante da fonte.
3. font-weight é o peso da fonte, ou seja se ela vai está em negrito ou "mais fina", por exemplo: lighter, normal, bold ou bolder. Nesse caso também são aceitos valores de 100 a 900.
4. font-size ou line-height é relativo ao tamanho da fonte, geralmente utilizamos px (pixel) ou em (medida recomendada pela W3C).
5. font-family é relativo a família da fonte.

Além da font-family, você pode usar @font-face para importar fontes externas, por exemplo, do [Google fonts](fonts.google.com) ou [DaFont](dafont.com):

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/c3c6ec81-af8b-440b-9a49-7ddeea7036ac)

Além disso, você pode incorporar um estilo embutido na primeira linha da sua tag &lt;style&gt;, seja dentro do próprio arquivo .html ou em uma folha de estilo separada (.css).

>[!NOTE]
> Os formatos geralmente aceitos são o opentype (.otf) e  o truetype (.ttf), mas também existem formatos como embedded-opentype, truetype-aat (Apple Advanced Typography) e .svg (muito usado com legendas)

>[!TIP]
> Se você quiser extrair uma fonte, uma extensão do Google Chrome muito útil é a [Ninja Fonts](https://www.fonts.ninja/). Você também pode encontrar mais detalhes sobre as fontes que estão em imagens em sites como [WhatFontIs (a melhor das opções)](whatfontis.com), [FontSquirrel](fontsquirrel.com) ou [MyFonts.com](myfonts.com). Recomendo utilizar essas ferramentas em conjunto para obter sempre o melhor resultado.

# Seletores personalizados
Às vezes, precisamos ser mais específicos quanto às modificações que queremos fazer nos elementos. É aí que entram os seletores personalizados. Antes de falar sobre isso, precisamos entender que utilizamos o id no HTML e # no CSS para identificar um elemento. Segundo a regra da W3C, só devemos ter um id por seletor em um documento. Já se quisermos agrupar várias características que serão usadas em diversos elementos específicos, podemos usar class no HTML e . no CSS. Veja abaixo como isso funciona:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a4ba1102-19d8-4de9-b97a-f84c423acb55) (Efeito visual)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/86805582-725a-474d-80d6-ea20dfaef193) (HTML)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/1bb8fc41-d042-4dbf-a72c-0e1000e5eaca) (CSS)

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

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/9f525f88-8904-4ed5-a4b0-2d703c14e351)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/f7755c48-ac06-4a2f-928d-aa8cbeb7f2a9)

Utilizar seletores de filhos é importante para aplicar estilos de maneira específica e organizada, evitando a necessidade de classes adicionais desnecessárias. Isso permite um código CSS mais limpo e fácil de manter, garantindo que os estilos sejam aplicados somente onde desejado.

## Declarando uma variável
Embora CSS não seja uma linguagem de programação, podemos declarar variáveis que facilitam muito nosso trabalho. Para criar variáveis para nossas configurações, devemos definir uma área de definições dentro do estilo usando a pseudo-classe :root. Essa pseudo-classe define configurações na raiz do documento, aplicando-as a todo o documento.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/54030cb0-b7c3-46e6-8e27-60c3ba3a947b)

A partir de agora, definir cores e fontes em nossos elementos HTML ficará mais fácil e personalizável, utilizando a função var().

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/0c4252a3-01bd-45f7-a673-f99099df1088)

## Pseudo-elementos
São usados em CSS para aplicar estilos a partes específicas de elementos sem precisar adicionar classes ou IDs adicionais ao HTML. Eles permitem selecionar e estilizar subpartes de elementos, oferecendo um controle mais refinado sobre a aparência do conteúdo. Utilizamos o sinal :: para pseudo-elementos.
* ::before e ::after são usados para inserir conteúdo antes ou depois do conteúdo real de um elemento. Eles são frequentemente utilizados para adicionar ícones, gráficos ou texto decorativo.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/030560a8-f443-4675-9372-4b9ddbe21baa)

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

 ![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/7a3dfd9b-e757-4c9b-bac2-b1166608eadf)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/4755fe31-003b-4ec0-aed7-57b30712ebe8)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6720be2f-a747-4458-9c6b-c9132817cc5f)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/82f2ec26-5255-4bfb-9544-993c5ab525af)

### Efeito zebrado
Para criar um efeito zebrado usamos a pseudo-classe --> :nth-child(nº de linhas). Vejamos um exemplo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/9756c536-8a45-40b8-9629-6cbc132b748e)

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
Lorem Ipsum

# Flexbox
Lorem Ipsum
