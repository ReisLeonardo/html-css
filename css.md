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
