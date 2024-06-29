# Estrutura da linguagem HTML
É organizada em uma série de elementos e tags que definem o conteúdo e a estrutura de uma página web. Os arquivos dessa linguagem possuem a extensão (.html). 
O exemplo abaixo ilustra a estrutura essencial de um documento HTML, incluindo a declaração do tipo de documento, o cabeçalho com metadados e o corpo com o conteúdo visível:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/fd15612a-77fb-4b33-9c40-884dda7a579d) (Como é o código escrito)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6833ed84-bf4a-49c7-9f99-9aad7343ccf3) (Como é o efeito visual)

* Declaração do Tipo de Documento: &lt;!DOCTYPE html&gt; indica ao navegador que o documento é um arquivo HTML5.
* Elemento: &lt;html&gt; indica o elemento raiz que envolve todo o conteúdo da página.
* Cabeçalho: &lt;head&gt; contém metadados sobre o documento, como o título, links para arquivos de estilo (CSS), scripts (JavaScript), e outras informações.
* Corpo: &lt;body&gt; contém todo o conteúdo visível da página, como texto, imagens, links, tabelas, listas, etc.

Exemplos de tags dentro do &lt;head&gt;:
 - &lt;title&gt;: Define o título da página que aparece na aba do navegador.
 - &lt;meta&gt;: Fornece metadados como charset, descrição, palavras-chave, autor, etc.
 - &lt;link&gt;: Conecta a página a arquivos externos, como folhas de estilo CSS.
 - &lt;style&gt;: Contém regras de estilo CSS que se aplicam ao documento.

Exemplos de tags dentro do &lt;body&gt;:
- &lt;h1&gt; a &lt;h6&gt;: Tags de cabeçalho, variando de h1 (mais importante) a h6 (menos importante).
- &lt;p&gt;: Define um parágrafo.
- &lt;a&gt;: Define um link.
- &lt;img&gt;: Insere uma imagem.
- &lt;ul&gt; e &lt;ol&gt;: Define listas não ordenadas e ordenadas, respectivamente.
- &lt;li&gt;: Define um item de lista. É um exemplo de tag que não precisa de fechamento na versão mais recente do HTML - HTML5.
- &lt;div&gt;: Define uma seção ou divisão no documento.
- &lt;span&gt;: Define uma seção de texto em linha.

>[!IMPORTANT]
> Antes de continuar lendo este material, recomendo que você baixe um editor de código ou um ambiente de desenvolvimento integrado (IDE). Eu costumo usar o [Visual Studio Code](https://code.visualstudio.com/download) para HTML, mas sinta-se à vontade para escolher o que preferir.

## As TAGs
HTML funciona com base em tags, sendo que a grande maioria delas possui abertura e fechamento com colchetes angulares, os famosos < (less than) e > (greater than). 
A estrutura dentro das tags não pode conter espaços. Além disso, podemos ter elementos com atributos, valores e conteúdo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/4125a51b-ab75-4428-8a3f-0f751f9b6264)

### Exemplos de TAGs de valores semânticos
* &lt;strong&gt; significa que o termo delimitado possui força dentro da frase. Logo, ele aparecerá em **negrito**.
* &lt;em&gt; significa que queremos dar ênfase ao termo (vinda do inglês emphasis). Logo, ele aparecerá em _itálico_.
* &lt;mark&gt; delimita um trecho como se estivéssemos usando uma caneta marca-texto.
* &lt;small&gt; reduzirá o tamanho do texto, sendo útil para contratos e cláusulas.
* &lt;del&gt; faz um ~traçado~ no meio da palavra, indicando que o texto deve ser desconsiderado pelo leitor.
* &lt;ins&gt; é o oposto do texto desconsiderado. Nesse caso, se colocarmos um texto qualquer dentro de &lt;ins&gt; e &lt;/ins&gt;, estamos dizendo que o texto está ali, deve ser lido e você deve prestar atenção nele.
* &lt;sup&gt; é usado quando queremos escrever equações matemáticas, por exemplo x^2.
* &lt;sup&gt; é usado quando queremos escrever equações químicias, por exemplo H2O.
* &lt;code&gt; é usado para aplicar espaçamento uniforme a todas as letras, sendo ideal para exibir trechos de código.
* &lt;pre&gt; é usado para manter o texto pré-formatado, exatamente da mesma maneira na qual ele foi digitado, incluindo quebras de linhas, espaços e tabulações.
* &lt;q&gt; é usado para citações curtas, vem do inglês quote. O texto dentro dessa tag irá receber automaticamente as aspas, mas não terá nenhum deslocamento. Essa técnica é mais usada quando queremos uma citação no meio de um parágrafo.
* &lt;blockquote&gt; é usada para citações mais longas (em bloco) que ocupam um parágrafo próprio. O texto recebe automaticamente um recuo. Podemos adicionar o atributo cite="" para melhorar o SEO da página e contribuir com a acessibilidade.
* &lt;abbr&gt; é uma novidade da HTML5 e que ajuda muito em áreas como a de Tecnologia, que usa muitas siglas e abreviações. Sempre que você quiser escrever uma sigla, mas deixar claro ao usuário (e aos mecanismos de busca) o significado dela, use a tag &lt;abbr&gt;.
* &lt;bdo&gt; vem de bi-directional override e ela basicamente inverte o texto, para direita (ltr) e para esquerda (rtl).

Veja mais exemplos de tags e explicações detalhadas na documentação da linguagem clicando [aqui](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

## Imagem favicon
O favicon é um pequeno ícone associado a um site, exibido na barra de endereços do navegador, nas abas e nos favoritos. Ele ajuda a identificar visualmente o site e a melhorar a experiência do usuário. O tipo de arquivo mais comum e recomendado para favicons é o .ico, pois ele é amplamente suportado por todos os navegadores e permite a inclusão de várias resoluções em um único arquivo, garantindo uma boa aparência em diferentes dispositivos e tamanhos de tela. Para adicionar um favicon a uma página HTML, usa-se a tag &lt;link&gt; dentro do elemento &lt;head&gt;:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/54c27393-b93b-41af-9c1f-9d3b85785901)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/b6a01d7a-c221-477f-b2ab-3fdfddf32a3a)

Existem alguns sites que você pode fazer ou baixar o seu próprio favicon:
* [Icon Archive](https://www.iconarchive.com/)
* [Favicon.cc - Crie o seu próprio favicon](https://www.favicon.cc/)
* [Favicon.io - Gerador de favicon -> imagem, texto ou emoji](https://favicon.io/)

## Caracteres especiais e Emojis
Na HTML5, chamamos caracteres especiais e emojis de _HTML Entities_. Confira a tabela abaixo para ver alguns deles. Além disso, você pode encontrar uma lista de emojis no formato _unicode_ no site da
[Emojipedia](www.emojipedia.org).

![Exemplo do PDF do Guanabara - PDF 5 da aula da HTML e CSS pg. 4](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a9341857-f487-4879-aa5d-b8bc8fb7ffbc)

>[!NOTE]
> Unicode é um padrão de codificação de texto que permite a representação de praticamente todos os caracteres usados em sistemas de escrita ao redor do mundo. Ele foi criado para resolver os problemas de incompatibilidade entre diferentes sistemas de codificação de caracteres, que eram comuns antes de sua adoção.
>
>Unicode é essencial para a interoperabilidade em um mundo digital globalizado, permitindo que informações textuais sejam trocadas e processadas corretamente em qualquer língua e em qualquer plataforma.

## Audiovisual
Na HTML, imagens, vídeos e áudios são elementos usados para exibir gráficos, fotografias, clipes de vídeo e conteúdos sonoros em uma página da web.

> [!CAUTION]
> É importante estar atento(a) aos conteúdos protegidos por direitos autorais, pois o uso não autorizado pode resultar em problemas legais, como processos judiciais. Saiba mais clicando [aqui](https://youtu.be/Bkym20GqOoQ).

Existem diversos sites onde você pode encontrar imagens e vídeos para uso sem se preocupar com direitos autorais. Alguns exemplos incluem:
* Foto:
  - [Pexels](https://www.pexels.com/)
  - [Unsplash](https://unsplash.com/)
  - [Pixabay](https://pixabay.com/)
* Vídeo:
  - [Videvo](https://www.videvo.net/)
  - [Coverr](https://coverr.co/)
 
### Formato da imagem
Um site que possui um bom SEO (Search Engine Optimization - otimização para mecanismos de busca) geralmente utiliza imagens leves em seu banco de dados. Isso significa que o site carrega rapidamente, proporcionando uma excelente experiência ao usuário. 
Ao criar seu site, é importante considerar não apenas a experiência do usuário, mas também o propósito de cada imagem utilizada, além das questões de redimensionamento.

* JPEG (.jpg), ou Joint Photographic Experts Group, é um algoritmo de compressão usado para criar imagens fotográficas com um tamanho significativamente reduzido. É amplamente adotado por câmeras digitais modernas e softwares de edição de imagens. A principal vantagem
desse formato é sua capacidade de gerar arquivos compactos, ocupando pouco espaço em disco. No entanto, é importante ter cuidado ao comprimir as imagens para evitar uma degradação excessiva na qualidade.
* O formato PNG (.png), ou Portable Network Graphics, se diferencia do JPEG pela capacidade de configurar a opacidade de cada pixel, permitindo torná-lo transparente ou com transparência limitada. No entanto, em comparação com o JPEG, o PNG tende a ocupar mais espaço
devido à sua capacidade de preservar com precisão as bordas dos pixels.

>[!TIP]
> Existem duas maneiras de comprimir imagens grandes em diversos formatos. Você pode baixar o software de código aberto [GIMP](https://www.gimp.org/downloads/), ou acessar sites como [Convert.io](https://convert.io/image-converter) ou [iLoveIMG](https://www.iloveimg.com/pt/comprimir-imagem) e fazer o upload da imagem, esses sites fornecerão uma versão mais compacta (mais leve) para download.

>[!TIP]
> Se você quiser remover o fundo de uma imagem, pode fazê-lo usando o [GIMP](https://www.gimp.org/downloads/) ou uma inteligência artificial online gratuita chamada [removebg](https://www.remove.bg/pt-br).

### Imagens dinâmicas
Quem acessa o site pelo celular, tablet, notebook/computador ou TV possui diferentes padrões de tela, e as imagens precisam se adaptar a esses formatos. Afinal, é muito desconfortável ver um site com margens laterais excessivas, especialmente em dispositivos móveis.

Esses são os tamanhos padrão para cada dispositivo:
* Celulares: 300x300
* Tablets: 700x700
* TVs: 1000x1000

### Como inserir imagens estaticas e dinâmicas?
Para inserir imagens estáticas em HTML, você pode usar a tag &lt;img&gt; e especificar o caminho da imagem no parâmetro src e alt para texto alternativo. Por exemplo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/991ddc3f-722c-4d3d-a9ca-b512298ecdb4)

Para inserir imagens dinâmicas, é necessário ter pelo menos três formatos separados (pequeno, médio e grande). Você deve utilizar a tag &lt;picture&gt; para isso. Dentro da tag &lt;picture&gt;, você deve incluir a tag &lt;source&gt;, onde pode definir o parâmetro media="", src="" e type="" para cada tamanho de imagem. Por exemplo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a1dc4a72-0bf2-454e-b9c8-a5abc02bc349)

> [!TIP]
> É sempre recomendável adicionar pelo menos 50px adicionais para evitar problemas de redimensionamento.

### Como inserir vídeos internos e externos?
Para inserir vídeos internos (no servidor) na HTML, você pode usar a tag &lt;video&gt;. Você pode definir o caminho do arquivo de vídeo no parâmetro src. Além disso, você pode adicionar parâmetros opcionais, como controls para exibir controles de reprodução padrão, autoplay para iniciar a reprodução automaticamente e loop para fazer o vídeo repetir continuamente.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/66b4aca8-1091-47c4-9c22-fbf76875c461)

> [!WARNING]
> A hierarquia é fundamental aqui. Se você define o arquivo .mp4 como a primeira opção, ele será o primeiro a ser carregado. Se não for possível, o navegador tentará a próxima opção. Se nenhum dos formatos for suportado, o texto alternativo definido será exibido.

Inserir vídeos externos é bastante fácil. Basta acessar a opção de compartilhar e copiar o código de incorporação (embed) fornecido pelo serviço de hospedagem do vídeo, e em seguida, colar esse código dentro da tag &lt;body&gt; do seu documento HTML. Isso é vantajoso, pois economiza espaço de armazenamento em sua hospedagem. No entanto, uma desvantagem é que o vídeo ou o serviço de hospedagem pode ficar fora do ar, comprometendo a visualização do seu conteúdo. Portanto, é importante analisar qual é a melhor opção para você ou seu cliente.

### Exemplos de formato de vídeo
1. mp4
2. webm
3. ogv
4. ogg
5. mpeg
6. m4v

> [!TIP]
> Um excelente conversor de vídeo para gerar arquivos em diversos formatos e utilizando codecs padronizados é o programa de código aberto (gratuito), chamado [Handbrake](https://handbrake.fr/downloads.php).

### Como inserir áudio interno e externo?
Os princípios que se aplicam a outras mídias também se aplicam ao áudio. Escolher um arquivo de áudio muito pesado pode afetar o carregamento do site. Podemos especificar o áudio utilizando o parâmetro src="", seja ele hospedado localmente ou em outro servidor. A declaração de um elemento de áudio é simples.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/2b43baea-229e-433c-a1ca-251a4aa7098b)

Agora para mais de uma opção de formato, utilizamos:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d3bbdc3a-5a03-4911-9f12-8fc7fe2a8b39)

### Exemplos de formato de áudio
1. mp3
2. ogg
3. wav

## Listas e dicionários
A HTML chama de ordered lists (&lt;ol&gt;) todas aquelas listas onde a ordem dos itens é algo muito importante e os itens são numerados automaticamente. Por exemplo um passo a passo para fazer um bolo ou uma lista de aprovados em um concurso.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/2db1ee1f-c815-4f75-971f-b24a8704498d) (Como é escrito)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6e53f846-ede3-4d40-ba76-d3ff16e83fe8) (Efeito visual)

As unordered lists (&lt;ul&gt;), também chamadas de listas com marcadores, que são aquelas onde a ordem dos itens não influenciará no significado da lista e os itens são marcados com marcadores (pontos) por padrão.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/17b9c1c6-3f30-420b-9ec8-3d035a1bc892)(Como é escrito)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/0f1f3360-7009-48f5-8fad-8e806dec6dfe)(Efeito visual)

### Parâmetro type e start
Dentro das lista podemos adicionar o parâmetro type. 
As listas ordenadas possuem os seguintes parâmetros:
* 1 - Valor padrão. Cria listas numeradas. Ex.: 1, 2, 3...
* A - Cria listas alfabéticas em maiúsculas. Ex.: A, B, C...
* a - Cria listas alfabéticas em minúsculas. Ex.: a, b, c...
* I - Cria listas com algarismos romanos em maiúsculas. Ex.: I, II, III...
* i - Cria listas com algarismos romanos em minúsculas. Ex.: i, ii, iii...

Já as listas não ordenadas possuem apenas três que são:
* disc - padrão. Uma bola preta totalmente pintada
* circle - Uma bola com uma borda preta e sem preenchimento
* square - Um pequeno quadrado preto totalmente pintado

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/c25ad72f-0d3d-4c5c-bae9-67bda970b5e7)

O parâmetro start é utilizado para definir o início da contagem, ele apenas pode receber um valor númerico mesmo se tratando de uma letra do alfabeto.

#### Dicionários
Por fim, utilizamos dicionários para definir termos e suas descrições:
* &lt;dl&gt; (Definition List) envolve toda a lista de definições.
* &lt;dt&gt; (Definition Term) representa um termo a ser definido.
* &lt;dd&gt; (Definition Description) contém a definição ou descrição do termo.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/1355342c-6747-48eb-a278-d16ce5adcb12) (Como é escrito)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d168706d-ce62-4f42-9cbb-6776e3877ccf) (Efeito visual)

## Links (endereços virtuais)
Os hyperlinks são um dos conceitos mais antigos da história da linguagem HTML. Eles permitem que você ligue um ponto a outro na World Wide Web. Toda vez que você está acessando um site e clica em um local para ir para outra página, outro site ou até para baixar um arquivo, você está interagindo com um hyperlink. Para criar um hyperlink, devemos criar âncoras através da tag &lt;a&gt;. O principal parâmetro dessa tag é o href, que cria uma referência hipertexto.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/4125a51b-ab75-4428-8a3f-0f751f9b6264)

Além desse parâmetro de href, temos outros como:
* hreflang - Define o idioma do que está por trás do link, é uma boa prática de SEO.
* target - Define onde o site de destino vai abrir
  - _blank vai abrir o link em uma nova janela em branco
  - _self vai abrir o link na janela ou frame atual (padrão)
  - _top vai desfazer todos os frames e abrir o destino no navegador completo
  - _parent similar ao uso do _top em uma referência à janela mãe
  - (nome-do-frame) caso esteja usando frames, indicar o nome da janela a abrir
* rel - Indica a natureza do destino
  - next indica que o link é para a próxima parte do documento atual
  - prev indica que o link é para a parte anterior do documento atual
  - author indica que é um link para o site do autor do artigo atual
  - external indica que é um link para outro site que não faz parte do site atual
  - nofollow indica que é um link para um site não endossado, como um link pago.

>[!TIP]
> Se você quiser aprender mais sobre links, leia a documentação da linguagem disponível [aqui](https://developer.mozilla.org/pt-BR/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)

### Downloads
Você também pode criar links para downloads usando âncoras. Veja um exemplo abaixo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/aa8ce8de-a9c6-4d3d-88e1-0bdfcf462575)

>[!TIP]
> Se você quiser saber o que escrever dentro do atributo type de uma âncora de hypertext, você pode consultar a lista oficial da IANA.org disponível [aqui](https://www.iana.org/assignments/media-types/media-types.xhtml).

## Tabelas
As tabelas em HTML são usadas para organizar e apresentar dados em formato tabular. Elas são especialmente úteis para exibir informações estruturadas, como horários, listas de preços, resultados de pesquisa, entre outros. 

>[!Warning]
> Não devemos usá-las para criar a estrutura do site, pois o HTML5 é semântico e já realiza essa função. Antigamente, a construção do site era feita com tabelas. Hoje, essa organização é feita pelo CSS, como já sabemos.

A hierarquia de uma tabela simples segue a ordem da lista abaixo:
1. &lt;table&gt;: Define o elemento da tabela.
2. &lt;caption&gt;: Define uma legenda para o topo da tabela.
3. &lt;thead&gt;: Define a cabeça da tabela
4. &lt;tbody&gt;: Define o corpo da tabela.
5. &lt;tfoot&gt;: Define o rodapé da tabela.
6. &lt;tr&gt; (table row): Define uma linha da tabela.
7. &lt;th&gt; (table header): Define uma célula de cabeçalho, geralmente usada para títulos de colunas ou linhas.
8. &lt;td&gt; (table data): Define uma célula de dados.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/ff4c9e90-54f3-44db-954e-e51f75cc0272)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6112448c-0f46-421a-8b09-1ea28e630cb5)

>[!Note]
> Nossa tabela não possui cores nem divisões, que seriam ideais para uma tabela bem formatada. No [repositório sobre CSS](https://github.com/ReisLeonardo/html-css-js/blob/main/css.md), ensino como deixá-las mais atraentes.

## iframe
Lorem Ipsum

## Formulários
