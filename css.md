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
> Para aplicar estilos globais a todas as tags, basta usar o seletor universal * no CSS, no mesmo lugar onde você aplicaria estilos ao body. Por exemplo:

## A importância das cores
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
* Cores Quentes: Incluem vermelho, laranja e amarelo. São associadas a sentimentos de energia, calor e entusiasmo, sendo frequentemente usadas para atrair atenção ou criar uma sensação de aconchego.
* Cores Frias: Incluem azul, verde e violeta. São associadas a sensações de calma, serenidade e tranquilidade, sendo ideais para ambientes relaxantes e serenos.

Na imagem abaixo, podemos ver a divisão entre as cores frias (cool colors) e quentes (warm colors), ajudando a entender melhor suas aplicações e efeitos emocionais em diferentes situações.

![Círculo cromático](https://upload.wikimedia.org/wikipedia/commons/f/fe/Warm_and_cool_colors.svg)

### Harmonia das cores
Refere-se à combinação equilibrada e agradável de cores, criando uma estética visualmente atraente e coerente. Existem várias formas de alcançar a harmonia das cores, e algumas das mais comuns são:
* **Harmonia Complementar:** Emprega cores que estão opostas no círculo cromático. Esse contraste forte pode criar um visual vibrante e dinâmico.
  * Exemplo: Azul, vermelho-laranja e amarelo-laranja.
* **Harmonia Análoga:** Utiliza cores que são adjacentes no círculo cromático. Essas combinações são naturalmente harmoniosas e proporcionam um efeito suave e agradável.
  * Exemplo: Azul, azul-verde e verde.
* **Harmonia Triádica:** Usa três cores equidistantes no círculo cromático, criando um visual vibrante e equilibrado, com bastante contraste e diversidade.
  * Exemplo: Vermelho, amarelo e azul.
* **Harmonia Tetrádica:** Inclui duas pares de cores complementares, criando uma paleta rica e diversificada. Pode ser desafiador equilibrar, mas resulta em combinações dinâmicas e atraentes.
  * Exemplo: Azul e laranja, vermelho e verde.
* **Harmonia Monocromática:** Usa variações de uma única cor, alterando apenas o brilho e a saturação. Isso cria um visual unificado e elegante.
  * Exemplo: Vários tons de azul.

## Criação da paleta de cores
Ter uma paleta de cores bem definida é fundamental para o desenvolvimento de um site, pois ela garante consistência visual, fortalece a identidade da marca e melhora a experiência do usuário. Uma paleta de cores harmoniosa facilita a navegação, destaca elementos importantes e cria uma estética atraente e profissional. O número ideal de cores em uma paleta geralmente varia entre 3 a 5 cores, o que permite variedade suficiente para criar contraste e interesse visual sem sobrecarregar o design.
* [Extensão Chrome - Seletor de cores](https://chromewebstore.google.com/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp)
* [Crie a sua roda de cores - Adobe Color](https://color.adobe.com/create/color-wheel)
* [Paletton - Crie uma paleta de cores e visualize como ela ficaria no seus site](https://paletton.com/)
* [Coolors - Gerador de paletas de cores](https://coolors.co/generate)
 
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
