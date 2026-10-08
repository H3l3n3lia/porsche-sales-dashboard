# Porsche Sales Dashboard

Dashboard interativo de análise de vendas de veículos Porsche desenvolvido para o desafio da DIO, utilizando HTML, CSS e JavaScript em um único arquivo `index.html`.

## 🔗 Dashboard publicado

> Após publicar no GitHub Pages, substitua o endereço abaixo pela URL gerada pelo GitHub:
>
> **https://SEU-USUARIO.github.io/porsche-sales-dashboard/**

## 🎯 Objetivo do projeto

Transformar uma base sanitizada de vendas de veículos Porsche em uma dashboard interativa capaz de responder perguntas de negócio de forma visual, objetiva e exploratória.

A proposta foi construir uma interface com aparência premium, inspirada no universo visual automotivo de alto padrão, utilizando preto, grafite, branco e vermelho como cores predominantes.

## 💼 Perguntas de negócio

### 1. Quais modelos Porsche geram maior receita?

**Por que essa pergunta é importante?**

Permite identificar os modelos que possuem maior contribuição financeira para as vendas. O gráfico de receita por modelo ajuda a comparar o impacto econômico dos diferentes veículos.

**Visual utilizado:** receita por modelo.

### 2. Quais cidades concentram o maior número de vendas?

**Por que essa pergunta é importante?**

Ajuda a identificar os mercados geográficos com maior volume de vendas e pode apoiar decisões comerciais, campanhas e priorização regional.

**Visual utilizado:** quantidade de vendas por cidade.

### 3. Como a receita evolui ao longo do tempo?

**Por que essa pergunta é importante?**

Permite observar a evolução da receita ao longo dos períodos disponíveis na base e identificar mudanças no comportamento das vendas.

**Visual utilizado:** evolução mensal da receita.

## 📊 KPIs

A parte superior da dashboard apresenta quatro indicadores:

- **Total de vendas**
- **Receita total**
- **Ticket médio**
- **Modelo mais vendido**

Os indicadores são recalculados de acordo com os filtros selecionados.

## 🔎 Filtros interativos

A dashboard permite filtrar os dados por:

- Modelo
- Cidade
- Estado
- Ano do modelo
- Forma de pagamento
- Status da entrega

Os gráficos e indicadores são atualizados automaticamente após a alteração dos filtros.

## 🧹 Tratamento dos dados

A base original fornecida pelo desafio possui uma aba chamada `Sanitized`. Para a dashboard foram utilizados somente os campos sanitizados:

- `SaleDateSanitized` → `SaleDate`
- `PorscheModelSanitized` → `PorscheModel`
- `ModelYearSanitized` → `ModelYear`
- `SalesPriceSanitized` → `SalesPrice`
- `VehicleMileageSanitized` → `VehicleMileage`
- `PayMethodSanitized` → `PayMethod`
- `CitySanitized` → `City`
- `StateSanitized` → `State`
- `DeliveryStatusSanitized` → `DeliveryStatus`

### Regras aplicadas

1. Foram utilizados somente os campos sanitizados da base.
2. Preços e anos de modelo foram tratados como valores numéricos.
3. Os registros de data com valor `INVALID` foram convertidos para ausência de data (`null`).
4. As datas inválidas **não foram inventadas, estimadas ou corrigidas artificialmente**.
5. As vendas com data inválida continuam participando dos KPIs e das análises que não dependem de tempo.
6. Somente a análise temporal exclui os registros sem data válida.
7. A dashboard informa visualmente essa regra ao usuário.

### Resultado geral da base

- **100 registros de vendas**
- **US$ 12.827.800,50** de receita total
- **US$ 128.278,01** de ticket médio
- Faixa de preços: **US$ 58.900 a US$ 286.500**
- **24 registros** apresentavam data `INVALID` e foram considerados sem data somente para a análise temporal.

## 🎨 Identidade visual

A interface foi construída com uma proposta visual premium:

- Fundo preto/grafite
- Contraste branco e cinza
- Vermelho como cor de destaque
- Cards com aparência sofisticada
- Tipografia limpa
- Hero visual com **Porsche Cayenne**, modelo utilizado como destaque visual por ser o modelo mais vendido na análise da base
- Layout responsivo para desktop e telas menores

A interface não utiliza o logotipo oficial da Porsche como elemento gráfico da aplicação.

### Imagem do Cayenne

A foto utilizada no hero é uma fotografia de Porsche Cayenne disponibilizada no Wikimedia Commons sob **CC0 (Creative Commons Zero)**, permitindo reutilização. A fonte foi mantida documentada no código do projeto.

Fonte: [Wikimedia Commons — Porsche Cayenne (2023)](https://commons.wikimedia.org/wiki/File:Porsche_Cayenne_(2023)_(54832849799).jpg)

## 🤖 Processo com IA e evolução dos prompts

### Prompt — Versão 1

```text
Crie uma dashboard interativa de análise de vendas de veículos Porsche utilizando HTML, CSS e JavaScript, em um único arquivo index.html.

A dashboard deve ter aparência profissional, moderna e limpa, inspirada no segmento automotivo premium. Use uma paleta baseada em preto, branco, cinza e vermelho como cor de destaque, sem utilizar o logotipo oficial da Porsche.

A base possui 100 registros de vendas e deve utilizar somente os campos sanitizados:
- SaleDate
- PorscheModel
- ModelYear
- SalesPrice
- VehicleMileage
- PayMethod
- City
- State
- DeliveryStatus

Objetivos:
1. Identificar quais modelos Porsche geram maior receita.
2. Identificar quais cidades concentram o maior número de vendas.
3. Analisar a evolução da receita ao longo do tempo.

KPIs:
- Total de vendas
- Receita total
- Ticket médio
- Modelo mais vendido

Filtros:
- Modelo
- Cidade
- Estado
- Ano
- Forma de pagamento
- Status da entrega

Gráficos:
1. Receita por modelo.
2. Quantidade de vendas por cidade.
3. Evolução da receita ao longo do tempo.

Os indicadores e gráficos devem ser atualizados automaticamente quando os filtros forem alterados.

As datas marcadas como INVALID devem ser consideradas como datas ausentes e não devem participar dos gráficos temporais. Porém, as respectivas vendas devem continuar sendo consideradas nos indicadores e nas análises que não dependem de data.

O dashboard deve ser responsivo para computador e celular.
Inclua uma pequena indicação visual de que os registros com datas inválidas foram excluídos apenas da análise temporal.
Entregue o resultado como um único arquivo index.html pronto para ser publicado no GitHub Pages.
```

### Evolução — Versão 2

Após avaliar a primeira apresentação, o direcionamento visual foi refinado para aproximar a dashboard de uma experiência automotiva premium.

Principais alterações solicitadas:

- visual mais elegante e sofisticado;
- maior contraste entre fundo e informações;
- estrutura de hero no topo;
- destaque para o Cayenne;
- aparência inspirada no padrão visual de sites automotivos premium;
- manutenção integral da parte funcional da dashboard.

### Evolução — Versão final

A versão final preservou a estrutura funcional e substituiu a imagem anterior do hero por uma fotografia real de um Porsche Cayenne, incorporada como imagem de fundo do topo.

Também foram mantidos:

- filtros interativos;
- KPIs;
- gráficos de receita por modelo;
- gráfico de vendas por cidade;
- série temporal de receita;
- tratamento das datas inválidas;
- layout responsivo;
- arquivo único `index.html`.

## 🧰 Ferramentas utilizadas

- HTML5
- CSS3
- JavaScript
- Plotly.js para visualizações interativas
- ChatGPT como apoio na análise, tratamento, estruturação e desenvolvimento
- GitHub para versionamento e publicação
- GitHub Pages para hospedagem da dashboard

**Canvas:** não foi utilizado como ferramenta de construção final. A implementação final foi realizada diretamente em HTML, CSS e JavaScript.

## 📁 Estrutura do repositório

```text
porsche-sales-dashboard/
├── index.html
├── README.md
└── .nojekyll
```

## 🚀 Como publicar no GitHub Pages

1. Crie um repositório público chamado `porsche-sales-dashboard`.
2. Envie `index.html`, `README.md` e `.nojekyll` para a raiz do repositório.
3. Abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`.
6. Clique em **Save**.
7. Aguarde a publicação e clique em **Visit site**.
8. Copie a URL publicada e substitua o endereço de exemplo no início deste README.

O GitHub informa que a publicação pode levar alguns minutos após o envio dos arquivos.

## 📌 Checklist antes da entrega do desafio

- [x] Repositório com nome em minúsculas e sem acentos
- [x] `index.html` na raiz
- [x] Dashboard interativa
- [x] KPIs funcionando
- [x] Filtros funcionando
- [x] Três perguntas de negócio respondidas visualmente
- [x] Tratamento das datas `INVALID` documentado
- [x] Prompts e evolução documentados
- [x] Origem da imagem do Cayenne documentada
- [ ] Repositório público no GitHub
- [ ] GitHub Pages publicado
- [ ] URL final adicionada neste README
- [ ] Link enviado na plataforma da DIO como **link do repositório**, conforme solicitado pelo desafio

## 📚 Fontes

- Base de dados fornecida pelo desafio DIO: https://hermes.dio.me/files/assets/8683bed0-cc33-4e06-bca9-04db9c31f9e2.xlsx
- GitHub Pages: https://docs.github.com/pt/pages/getting-started-with-github-pages/creating-a-github-pages-site
- Imagem do Cayenne: https://commons.wikimedia.org/wiki/File:Porsche_Cayenne_(2023)_(54832849799).jpg
