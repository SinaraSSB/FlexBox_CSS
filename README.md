![CSS Flex](https://imgur.com/ytMIIUO.png)
## 
# CSS Flexbox

Página inicial do Luz e Cena.

## 🔨 Funcionalidades do Projeto

A página possui um cabeçalho, um banner, uma lista de filmes, uma seção de newsletter e um rodapé.

## ✔️ Técnicas e Tecnologias Utilizadas

As principais técnicas e tecnologias utilizadas neste projeto são:

- **`HTML`**: Linguagem de marcação utilizada para estruturar o conteúdo das páginas web.
- **`CSS`**: Utilizado para estilizar a apresentação da página web.
  - **`CSS Flexbox`**: Utilizado para organizar elementos de forma flexível e responsiva, garantindo um layout moderno e adaptável. Abaixo estão os principais atributos utilizados do Flexbox:
    - **`display: flex`**: Define um elemento como um container flexível, ativando as propriedades Flexbox para os elementos filhos.
    - **`flex-direction`**: Define a direção principal do layout dos itens flexíveis.
    - **`justify-content`**: Alinha os itens ao longo do eixo principal (horizontal por padrão).
    - **`align-items`**: Alinha os itens ao longo do eixo transversal (vertical por padrão).
    - **`align-content`**: Alinha várias linhas de itens flexíveis quando há espaço extra no eixo transversal. Funciona quando há múltiplas linhas (com `flex-wrap`).
    - **`flex-wrap`**: Define se os itens devem ou não quebrar para a próxima linha.
    - **`flex-flow`**: Combina `flex-direction` e `flex-wrap` em uma única propriedade.
    - **`order`**: Define a ordem dos itens dentro do container flexível.
    - **`flex-grow`**: Define a capacidade de um item flexível de crescer, ocupando o espaço disponível.
    - **`flex-shrink`**: Define a capacidade de um item de encolher caso necessário.
    - **`flex-basis`**: Define o tamanho inicial do item antes de o espaço disponível ser distribuído.
    - **`flex`**: Combina `flex-grow`, `flex-shrink` e `flex-basis` em uma única propriedade para maior simplicidade.
    - **`align-self`**: Permite modificar o alinhamento de um item específico, substituindo o valor definido em `align-items` para aquele item.

Esses atributos são essenciais para criar um layout flexível, garantindo que a página seja responsiva e adaptável a diferentes tamanhos de tela e dispositivos.

## 📁 Acesso ao Projeto

Você pode [acessar o código-fonte do projeto inicial](https://github.com/monicahillman/3992-css-grid/tree/projeto-base) ou [baixá-lo](https://github.com/monicahillman/3992-css-grid/archive/refs/heads/projeto-base.zip).

** Acessando o protótipo do projeto no figma>>> 
https://www.figma.com/design/5R7RVz8QGMuOzJafDPnz5h/CSS--Avan%C3%A7ando-em-flexbox-%7C-Luz---Cena--Community-?node-id=0-1&p=f&t=IB2LvaHWOwTDYJmK-0

## 🛠️ Como Abrir e Rodar o Projeto

Após baixar o projeto, você pode abri-lo no Visual Studio Code. Para isso, siga os passos abaixo:

1. No menu superior do VS Code, clique em:
   * **File > Open Folder** (ou uma opção similar).
2. Procure o local onde o projeto foi salvo e selecione a pasta (se o projeto foi baixado como um arquivo ZIP, será necessário extraí-lo antes).
3. Clique em **OK**.

Após finalizar esses passos, você pode executar a aplicação usando a extensão **Live Server** 🏆. Isso facilitará a visualização do projeto em seu navegador e garantirá que as alterações sejam refletidas automaticamente.


---
07
Para saber mais: ordenando itens


No mundo de desenvolvimento web, a criação de layouts responsivos e bem estruturados é essencial para garantir uma boa experiência do usuário em diferentes dispositivos e tamanhos de tela. O CSS Flexbox é uma ferramenta poderosa para isso, permitindo a criação de layouts flexíveis e alinhados com facilidade. Entre as suas propriedades, display: flex e order são particularmente importantes para controlar a disposição e a ordem dos elementos dentro de um contêiner flexível. Este texto explora como essas propriedades podem ser utilizadas para estilizar cabeçalhos, criar navegações flexíveis e responsivas, e ajustar layouts com media queries.

Criar layouts responsivos e bem organizados pode ser desafiador, especialmente quando se trata de alinhar elementos de forma precisa e controlar a ordem em que aparecem na tela. Por exemplo, um cabeçalho pode precisar ser centralizado e ter uma largura máxima, uma lista de navegação deve se adaptar a diferentes tamanhos de tela, e um campo de input de pesquisa deve ser estilizado adequadamente. Além disso, a ordem dos elementos pode precisar ser ajustada para diferentes visualizações, o que pode ser complexo sem uma abordagem sistemática.

O Flexbox fornece uma maneira mais eficiente e intuitiva de distribuir espaço e alinhar itens em um contêiner, mesmo quando o tamanho dos itens é desconhecido ou dinâmico.

**display: flex:** Define o contêiner como um contêiner flexível, ativando as propriedades flexbox nos itens filhos. Os itens dentro do contêiner podem ser alinhados e distribuídos facilmente usando propriedades como justify-content, align-items, e flex-direction.

**order:** Permite alterar a ordem visual dos itens dentro de um contêiner flexível sem alterar o HTML. Itens com um valor de order menor aparecem antes dos itens com valores maiores. Isso é útil para ajustar a ordem dos elementos responsivamente.

Exemplo de código usando order:
> 
> <div class="container">
>     <div class="item1">Item 1</div>
>     <div class="item2">Item 2</div>
>     <div class="item3">Item 3</div>
> </div>`
> 
> 
> .container {
>     display: flex;
> }
> 
> .item1 { order: 2; }
> .item2 { order: 1; }
> .item3 { order: 3; }`

.item1 é exibido em segundo lugar.
.item2 é exibido em primeiro lugar.
.item3 é exibido em terceiro lugar.

Combinando essas propriedades com media queries, você pode criar layouts adaptáveis que mantêm a funcionalidade e a estética em diferentes dispositivos e tamanhos de tela.