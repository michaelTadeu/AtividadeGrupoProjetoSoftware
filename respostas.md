# Relatório de Resolução de Conflitos e Melhoria de Layout

## 1. Entendimento do conflito
- **O que causou o conflito no arquivo `index.html`?**
  > O conflito ocorreu porque dois desenvolvedores do grupo alteraram as mesmas linhas de código simultaneamente em branches separadas.
- **Em qual parte do código ele ocorreu?**
  > O conflito se concentrou na tag `<aside>`, especificamente na `<div class="list-group">` que contém os links do menu lateral de navegação.

## 2. Processo de resolução
- **Qual opção vocês utilizaram inicialmente?**
  - [ ] Accept Current Change
  - [ ] Accept Incoming Change
  - [x] Accept Both Changes
- **Foi necessário ajuste manual após isso? Explique o que foi feito.**
  > Sim. Ao aceitar ambas as mudanças, o código ficou com links duplicados e algumas classes conflitantes do Bootstrap. Foi necessário limpar manualmente as tags duplicadas, organizar a indentação e mesclar as classes (por exemplo, manter as novas cores e, ao mesmo tempo, os novos links e ícones adicionados).

## 3. Decisão técnica
- **Quais partes do código da branch `prd` vocês mantiveram?**
  > Mantivemos a estrutura base do cabeçalho (Navbar), as tags `<head>` originais e a estrutura do rodapé (Footer), pois já estavam padronizados e funcionando corretamente.
- **Quais partes da sua branch foram preservadas?**
  > Preservamos toda a nova estrutura do conteúdo principal (`<main>`), incluindo o sistema de grid de cards do Bootstrap, as classes de sombra (`shadow-sm`) e as importações do CDN do Bootstrap Icons.

## 4. Dificuldades encontradas
- **Quais foram as principais dificuldades durante:**
  - **O merge?**
    > A principal dificuldade foi garantir que todos tivessem feito o `git fetch` e o `git pull` corretamente antes de tentar integrar as branches, para evitar sobrescrever o trabalho de alguém.
  - **A resolução de conflitos?**
    > Entender visualmente o que o Git estava mostrando com as marcações (`<<<<<<< HEAD`, `=======`, `>>>>>>>`). Tivemos que analisar com cuidado no VS Code para não apagar o fechamento de tags HTML importantes (`</div>`).
  - **A melhoria de layout?**
    > Ajustar a responsividade no Bootstrap. Fazer com que os novos Cards de grupos de estudo quebrassem de forma correta em telas menores (celulares) sem perder a formatação ou o alinhamento dos ícones.

## 5. Solução adotada
- **Como o grupo resolveu os problemas encontrados?**
  > O grupo realizou uma chamada rápida e usou o Live Share (ou compartilhamento de tela) para revisar o conflito em conjunto. Discutimos linha por linha qual código fazia mais sentido manter e testamos a página localmente antes de realizar o commit de resolução do conflito.
- **Houve necessidade de pesquisar? Onde?**
  > Sim. Pesquisamos na documentação oficial do Bootstrap 5 (para verificar as classes de grid `row-cols-md-2` e espaçamentos) e na documentação do próprio GitHub sobre melhores práticas para resolução de conflitos de merge.

## 6. Melhoria de layout
- **Qual página foi escolhida para melhoria?**
  > A página de Grupos de Estudo e Pesquisa do curso de Sistemas de Informação.
- **Quais mudanças visuais foram implementadas?**
  > Substituímos a lista genérica (`<ul>`) por um grid de Cards modernos. Adicionamos uma imagem ilustrativa responsiva no topo, incluímos ícones vetoriais (Bootstrap Icons) nos títulos e botões, aplicamos sombras (`shadow-sm`) para dar profundidade e melhoramos a hierarquia de cores destacando elementos com as classes de sucesso (`text-success`, `bg-success`).
- **Qual foi o objetivo dessas melhorias?**
  > O objetivo foi modernizar a interface, melhorar a experiência do usuário (UX) deixando a leitura mais escaneável e garantir que a página fosse totalmente responsiva, passando mais profissionalismo para quem acessa as informações do curso.

## 7. Aprendizado
- **O que o grupo aprendeu sobre:**
  - **Uso de branches:**
    > Aprendemos que as branches são fundamentais para o desenvolvimento em equipe, pois isolam novas funcionalidades (features) e evitam que o código principal (main) seja quebrado durante os testes.
  - **Merge:**
    > O merge não é apenas um comando automático; exige comunicação da equipe para garantir que as integrações façam sentido funcionalmente e não gerem bugs ocultos.
  - **Conflitos no Git:**
    > Percebemos que conflitos são normais e indicam que duas ou mais pessoas trabalharam na mesma área do projeto. Eles não são "erros", mas sim pontos onde o Git precisa da decisão humana para prosseguir com segurança.

## 8. Autoavaliação do grupo
*Dê uma nota de 0 a 10 para as métricas abaixo:*

- **Organização do grupo:** `9 / 10`
- **Entendimento da atividade:** `10 / 10`
- **Resultado final:** `10 / 10`
