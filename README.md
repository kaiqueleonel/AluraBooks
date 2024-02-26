
# AluraBooks

Desenvolvimento da página inicial da AluraBooks, site de uma empresa fictícia de vendas de livros, baseado no design disponibilizado em um [arquivo Figma](https://www.figma.com/file/sSMbIqKaGBd66Y8roxTk2p/AluraBooks?type=design&node-id=122%3A4916&mode=design&t=YrSPYE7JLI87yyOb-1).

| :placard: Vitrine.Dev |     |
| -------------  | --- |
| :sparkles: Nome        | Página inicial da AluraBooks
| :label: Tecnologias | HTML, CSS, Swiper
| :rocket: URL         | [https://kaiqueleonel.github.io/AluraBooks/](https://kaiqueleonel.github.io/AluraBooks/)
| :fire: Curso     | [https://www.alura.com.br/curso-online-html-css-responsividade-mobile-first](https://www.alura.com.br/curso-online-html-css-responsividade-mobile-first)

![AluraBooks](https://github.com/kaiqueleonel/AluraBooks/assets/110237903/4a61eb01-1d75-43c5-b31d-0b86e4eb09fc#vitrinedev)

Obs: Swiper é uma plugin javascript que permite a criação de carrossel e outros tipo de elementos para o seu site.

Pode acessar o site do Swiper clicando [aqui](https://swiperjs.com).


## Créditos

Este projeto foi desenvolvido em um curso da [Alura](https://www.alura.com.br), o nome do curso é 'HTML e CSS: responsividade com mobile-first'.

**Instrutora**: [Mônica Hillman](https://github.com/MonicaHillman)


## O que é mobile-first?

Mobile-first consiste em desenvolver o site priorisando os dispositovos mobile e depois fazer a responsividade para os demais tipos de telas, por exemplo, desktop, tablet etc. 

## O que aprendemos

### Metodoloia BEM
Apartir do arquivo Figma, nós identificamos elementos e seções semelhantes, com isso facilitou a estruturação do HTML e CSS para fazermos reúso de estilos, padrões e classes.

Os elementos HTML tiveram suas classes  nomeadas usando a [metodologia   BEM](https://getbem.com/introduction/)(Block-Element-Modifier), o que é uma boa forma de nomeaçaõ de classes para facilitar a identificação da classe e de onde ela pertence.

Exemplo:
```HTML
<section class="carrossel">
  <h2 class="carrossel__titulo">últimos lançamentos</h2>
  <div class="corrossel__container">
```

### Menu Hambúrguer
Desenvolvemos um menu hambúrguer para dispositivos mobile, utilizando apenas HTML e CSS, para obtermos o resultado abaixo utilizamos pseudo-classes e combinadores. Utilizamos a pseudo-classe ``` :checked ``` e o combinador ``` ~ ```. A pseudo-classe ``` :checked ``` é utilizada quando temos um input do tipo ``` checked ```, somente vai ser aplicado os estilos quando estiver com o ``` checked ```
ativo. Já o combinador ``` ~ ``` , denominado irmão geral,  ele seleciona todos os elementos que estão dentro do primeiro elemento.

![AluraBooks-menu__hamburguer](https://github.com/kaiqueleonel/AluraBooks/assets/110237903/702f44c2-b89e-411b-aaa4-114966c7c807)

Exemplo da pseudo-classe ``` :checked ``` e do combinador ``` ~ ```.
```CSS
.container__botao:checked ~ .lista-menu{
    display: block;
    position: absolute;
    top: 100%;
}

```

Neste exemplo, os estilos somente serão aplicados quando o input  do tipo ``` checked ``` estiver ativo,  o input estando ativo os estilos serão aplicados somente na classe ``` .lista-menu ```.

### Váriaveis CSS

Nós definimos variáveis no arquivo CSS para as cores e fontes utilizadas no site, prevenindo a repetição de código e favorecendo seu reúso e manutenção. Quando é necessária uma mudança em uma cor ou fonte, precisamos somente modificar estas variáveis, ao invés de procurar no código todo onde elas foram aplicadas. Segue um exemplo:
```CSS

:root{
    --cor-de-fundo: #EBECEE;
    --branco: #FFFFFF;
    --laranja: #EB9800;
    --azul-degrade: linear-gradient(97.54deg, #002F52 35.49%, #326589 165.37%);
    --fonte-principal: "Poppins";
    --azul:#002F52;
    --preto: #000;
    --fonte-secundaria: "Josefin Sans";
    --cinza-claro: #858585;
    --cinza: #474646;
}

body{
    background-color: var(--cor-de-fundo);
    font-size: 16px;
    font-family: var(--fonte-principal);
    font-weight: 400;
}
```

###  Background com linear-gradient em texto

Nós observamos no figma que alguns dos texto tinha como cor um linear-gradient, para aplicamos está cor utilizamos o background para aplicar a cor e depois especificamos que o backgound devia ser aplicado somente onde tinha texto e definimos a cor do texto para transparente para não interferir com o background. Segue um exemplo: 

```CSS
.lista-menu__link{
    background: var(--azul-degrade);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-transform: uppercase;
}
```
Obs: O ``` -webkit-background-clip: text; ``` e o ```  background-clip: text; ``` aplicam o mesmo efeito. O  prefixo ``` -webkit- ``` é usada em navegadores WebKit (como Chrome e Safari).

## Resultado Final 

O resultado obtido foi um site responsivo para três tipo de telas a de celular(428px), a de tablets e monitores pequenos(1024px) e para monitores(1728px).

### Tela de celular

![AluraBooks-Celular2](https://github.com/kaiqueleonel/AluraBooks/assets/110237903/f73a6fa3-cb79-4c86-b70c-b0b9d3841125)

### Tela de Tablet

![AluraBooks-Tablet2](https://github.com/kaiqueleonel/AluraBooks/assets/110237903/a2e5e963-79f0-4150-ae18-5391e92b83d8)


### Tela de Monitor

![AluraBooks-Monitor2](https://github.com/kaiqueleonel/AluraBooks/assets/110237903/a26a7b6f-7724-4323-9e9f-38120dac3ce3)



