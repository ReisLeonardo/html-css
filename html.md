# Estrutura da linguagem HTML
É organizada em uma série de elementos e tags que definem o conteúdo e a estrutura de uma página web. Os arquivos dessa linguagem possuem a extensão (.html). 
O exemplo abaixo ilustra a estrutura essencial de um documento HTML, incluindo a declaração do tipo de documento, o cabeçalho com metadados e o corpo com o conteúdo visível:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6833ed84-bf4a-49c7-9f99-9aad7343ccf3)

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/fd15612a-77fb-4b33-9c40-884dda7a579d)

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

## As TAGs
HTML funciona com base em tags, sendo que a grande maioria delas possui abertura e fechamento com colchetes angulares, os famosos < (less than) e > (greater than). 
A estrutura dentro das tags não pode conter espaços. Além disso, podemos ter elementos com atributos, valores e conteúdo:

![Exemplo do PDF do Guanabara - PDF 3 da aula da HTML e CSS pg. 4](https://github.com/ReisLeonardo/html-css-js/assets/89877899/9cf5fc12-db3a-4a52-b094-adb47b164506)

### TAGs de valores semânticos
* &lt;strong&gt; significa que o termo delimitado possui força dentro da frase. Logo, ele aparecerá em **negrito**.
* &lt;em&gt; significa que queremos dar ênfase (vinda do inglês emphasis) ao termo. Logo, ele aparecerá em _itálico_.
* &lt;mark&gt; delimita um trecho como se estivéssemos usando uma caneta marca-texto.
* &lt;small&gt; reduzirá o tamanho do texto, sendo útil para contratos e cláusulas.
* &lt;del&gt; faz um ~traçado~ no meio da palavra, indicando que o texto deve ser desconsiderado pelo leitor.
* &lt;ins&gt; é o oposto do texto desconsiderado. Nesse caso, se colocarmos um texto qualquer dentro de &lt;ins&gt; e &lt;/ins&gt;, estamos dizendo que o texto está ali, deve ser lido e você deve prestar atenção nele.
* &lt;sup&gt; é usado quando queremos escrever equações matemáticas, por exemplo x^2.
* &lt;sup&gt; é usado quando queremos escrever equações químicias, por exemplo H2O.
* &lt;code&gt; é usado para aplicar espaçamento uniforme a todas as letras, sendo ideal para exibir trechos de código.
* &lt;pre&gt; é usado manter o texto pré-formatado, exatamente da mesma maneira na qual ele foi digitado, incluindo quebras de linhas, espaços e tabulações.
* &lt;q&gt; é usado para citações curtas, vem do inglês quote. O texto dentro dessa tag irá receber automaticamente as aspas, mas não terá nenhum deslocamento. Essa técnica é mais usada quando queremos uma citação no meio de um parágrafo.
* &lt;blockquote&gt; é usada para citações mais longas (em bloco) que ocupam um parágrafo próprio. O texto recebe automaticamente um recuo. Podemos adicionar o atributo cite="(citação aqui)" para melhorar o SEO da página e contribuir com a acessibilidade.
* &lt;abbr&gt; é uma novidade do HTML5 e que ajuda muito em áreas como a de Tecnologia, que usa muitas siglas e abreviações. Sempre que você quiser escrever uma sigla, mas deixar claro ao usuário (e aos mecanismos de busca) o significado dela, use a tag &lt;abbr&gt;.
* &lt;bdo&gt; significa bi-directional override e ela basicamente inverte o texto, para direita (ltr) e para esquerda (rtl).

Veja mais exemplos de tags na documentação da linguagem [aqui](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

## Caracteres Especiais e Emojis
Em HTML, chamamos caracteres especiais e emojis de _HTML Entities_. Confira a tabela abaixo para ver alguns deles. Além disso, você pode encontrar uma lista de emojis no formato Unicode no site da
[Emojipedia](www.emojipedia.org).

![Exemplo do PDF do Guanabara - PDF 5 da aula da HTML e CSS pg. 4](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a9341857-f487-4879-aa5d-b8bc8fb7ffbc)

## Imagens, vídeo e aúdio.
Em HTML, imagens, vídeos e áudios são elementos usados para exibir gráficos, fotografias, clipes de vídeo e conteúdos sonoros em uma página da web.

> [!CAUTION]
> É importante estar atento(a) às imagens e conteúdos protegidos por direitos autorais, pois o uso não autorizado pode resultar em problemas legais, como processos judiciais. Recomendo assistir a um vídeo no YouTube que aborda essas questões de forma detalhada. 
[Clique aqui](https://youtu.be/Bkym20GqOoQ) para acessar o vídeo.

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
devido à sua capacidade de preservar com precisão as bordas dos pixels. Isso pode resultar em arquivos um pouco mais pesados, mas geralmente não de forma significativa.

> [!TIP]
> Existem duas maneiras de comprimir imagens grandes em diversos formatos. Você pode baixar o software de código aberto [GIMP](https://www.gimp.org/downloads/), ou acessar sites como [Convert.io](https://convert.io/image-converter) ou [iLoveIMG](https://www.iloveimg.com/pt/comprimir-imagem) e fazer o upload da imagem. Esses sites fornecerão uma versão mais compacta para download.

### Imagens dinâmicas
Quem acessa o site pelo celular, tablet, notebook/computador ou TV possui diferentes padrões de tela, e as imagens precisam se adaptar a esses formatos. Afinal, é muito desconfortável ver um site com margens laterais excessivas, especialmente em dispositivos móveis.

* Celulares: 300x300
* Tablets: 700x700
* TV: 1000x1000

### Como inserir imagens estaticas e dinâmicas
Para inserir imagens estáticas em HTML, você pode usar a tag &lt;img&gt; e especificar o caminho da imagem no parâmetro src e alt para texto alternativo. Por exemplo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/27511c4e-e592-4121-8088-273b72d3aa17)

Para inserir imagens dinâmicas, é necessário ter pelo menos três formatos separados (pequeno, médio e grande). Você deve utilizar a tag &lt;picture&gt; para isso. Dentro da tag &lt;picture&gt;, você deve incluir a tag &lt;source&gt;, onde pode definir o atributo media="max-width:nºdepx" e o atributo src para cada tamanho de imagem. Por exemplo:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/a1dc4a72-0bf2-454e-b9c8-a5abc02bc349)

> [!TIP]
> É sempre recomendável adicionar pelo menos 50px adicionais para evitar problemas de redimensionamento.

### Como inserir vídeos internos e externos
Para inserir vídeos internos (no servidor) em HTML, você pode usar a tag &lt;video&gt;. Você pode definir o caminho do arquivo de vídeo no atributo src. Além disso, você pode adicionar atributos opcionais, como controls para exibir controles de reprodução padrão, autoplay para iniciar a reprodução automaticamente e loop para fazer o vídeo repetir continuamente.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/66b4aca8-1091-47c4-9c22-fbf76875c461)

> [!WARNING]
> A hierarquia é fundamental aqui. Se você define o arquivo .mp4 como a primeira opção, ele será o primeiro a ser carregado. Se não for possível, o navegador tentará a próxima opção. Se nenhum dos formatos for suportado, o texto alternativo definido será exibido.

Inserir vídeos externos é bastante fácil. Basta acessar a opção de compartilhar e copiar o código de incorporação (embed) fornecido pelo serviço de hospedagem do vídeo, e em seguida, colar esse código dentro do elemento &lt;body&gt; do seu documento HTML. Isso é vantajoso, pois economiza espaço de armazenamento em sua hospedagem. No entanto, uma desvantagem é que o vídeo ou o serviço de hospedagem pode estar fora do ar, comprometendo a visualização do seu vídeo. Portanto, é importante analisar qual é a melhor opção para você ou seu cliente.

### Formato de vídeo
* .mp4
* .ogg
* .mpeg
* .m4v
* .webm
* .ogv

> [!TIP]
> Um excelente conversor de vídeo para gerar arquivos em diversos formatos e utilizando codecs padronizados é o programa de código aberto (gratuito), chamado [Handbrake](https://handbrake.fr/downloads.php).

### Como inserir áudio interno e externo
Lorem Ipsum

### Formato de áudio
* .mp3
* .wav
* .ogg

## Imagem favicon
O favicon é um pequeno ícone associado a um site, exibido na barra de endereços do navegador, nas abas e nos favoritos. Ele ajuda a identificar visualmente o site e a melhorar a experiência do usuário. O tipo de arquivo mais comum e recomendado para favicons é o .ico, pois ele é amplamente suportado por todos os navegadores e permite a inclusão de várias resoluções em um único arquivo, garantindo uma boa aparência em diferentes dispositivos e tamanhos de tela. Para adicionar um favicon a uma página HTML, usa-se a tag &lt;link&gt; dentro do elemento &lt;head&gt;:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/54c27393-b93b-41af-9c1f-9d3b85785901)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/b6a01d7a-c221-477f-b2ab-3fdfddf32a3a)

Existem alguns sites que você pode fazer ou baixar o seu próprio favicon:
* [Icon Archive](https://www.iconarchive.com/)
* [Favicon.cc - Crie o seu próprio favicon](https://www.favicon.cc/)
* [Favicon.io - Gerador de favicon -> imagem, texto ou emoji](https://favicon.io/)

## Listas ordenadas, não ordenadas e dicionários em HTML
A HTML chama de ordered lists todas aquelas listas onde a ordem dos itens é algo muito importante e os itens são numerados automaticamente. Por exemplo um passo a passo para fazer um bolo ou uma lista de aprovados em um concurso. As unordered lists, também chamadas de listas com marcadores, que são aquelas onde a ordem dos itens não influenciará no significado da lista e os itens são marcados com marcadores (pontos) por padrão. Independentemente do tipo de lista, ela deve estar no seguinte formato:

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/2db1ee1f-c815-4f75-971f-b24a8704498d)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/6e53f846-ede3-4d40-ba76-d3ff16e83fe8)

&lt;ol&gt; é para lista ordenada e &lt;ul&gt; é para lista não ordenada.

Por fim, utilizamos dicionários para definir termos e suas descrições:
* &lt;dl&gt; (Definition List) envolve toda a lista de definições.
* &lt;dt&gt; (Definition Term) representa um termo a ser definido.
* &lt;dd&gt; (Definition Description) contém a definição ou descrição do termo.

![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/1355342c-6747-48eb-a278-d16ce5adcb12)
![image](https://github.com/ReisLeonardo/html-css-js/assets/89877899/d168706d-ce62-4f42-9cbb-6776e3877ccf)



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

## Links (endereços virtuais)
Lorem Ipsum.
