# Respostas da Atividade: Atualização de Branch com Hotfix na main e Novo Pull Request

## 1. Entendimento do conflito
**O que causou o conflito no arquivo index.html?**
O conflito foi causado porque a mesma parte do arquivo (o menu lateral) foi modificada em duas branches diferentes. A branch `main` (`prd`) aplicou um hotfix para adicionar "pages/" aos caminhos dos links, enquanto na branch de desenvolvimento os nomes dos links foram customizados de acordo com a atividade.

**Em qual parte do código ele ocorreu?**
Ele ocorreu nas linhas 38-43 do arquivo `index.html`, no trecho onde estão definidos os links das tags `<a>` do menu lateral "DESTAQUES DO CURSO".

## 2. Processo de resolução
**Qual opção vocês utilizaram inicialmente?**
o ( ) Accept Current
o ( ) Accept Incoming
o (X) Accept Both (ajuste manual combinando ambos)

**Foi necessário ajuste manual após isso? Explique o que foi feito.**
Sim. Foi necessário um ajuste manual para juntar as duas intenções. Ao resolver as marcações do Git, combinamos o caminho do link que veio da branch de correção (`href="pages/..."`) com o texto/conteúdo interno que definimos na nossa branch (`>Labs de TI</a>`).

## 3. Decisão técnica
**Quais partes do código da main vocês mantiveram?**
Mantivemos o valor dos atributos `href` corrigidos da main (exemplo: `href="pages/laboratory.html"`).

**Quais partes da sua branch foram preservadas?**
Foram preservados os nomes de exibição dos botões do menu (exemplo: `Labs de TI`, `Eventos`, `Jornada SI`).

## 4. Dificuldades encontradas
**Quais foram as principais dificuldades durante:**
*   **o merge:** Garantir que estaríamos trazendo a versão correta do hotfix para dentro da feature sem perder o trabalho recém-feito.
*   **a resolução de conflitos:** Observar cuidadosamente qual linha pertencia à `HEAD` e qual vinha da `origin` para combiná-las de forma que a sintaxe do HTML não fosse quebrada (e.g. evitar duplicação de tags `<a>`).
*   **a melhoria de layout:** Encontrar as classes corretas do Bootstrap que combinassem bem juntas e decidir os melhores ícones para cada informação de laboratório para criar uma hierarquia visual limpa.

## 5. Solução adotada
**Como o grupo resolveu os problemas encontrados? Houve necessidade de pesquisar? Onde?**
O grupo resolveu os problemas do merge lendo minuciosamente o código que estava em conflito e reescrevendo a linha para unir o `href` corrigido ao texto customizado. Para a melhoria do layout, pesquisamos na documentação oficial do Bootstrap (versão 5) sobre "Cards" e "Utilities", e no site do Bootstrap Icons para pegar as classes das imagens vetoriais (ícones).

## 6. Melhoria de layout
**Qual página foi escolhida para melhoria?**
A página escolhida, conforme a designação do grupo, foi `laboratory.html`.

**Quais mudanças visuais foram implementadas? Qual foi o objetivo dessas melhorias?**
Foram adicionados os Bootstrap Icons nas informações de texto e nos títulos. A estrutura dos cards foi modernizada aplicando sombras (`shadow`), bordas coloridas no topo (`border-top border-success border-3`) e arredondamento nas bordas (`rounded-3`). O objetivo das melhorias foi tornar as informações sobre cada laboratório mais fáceis de escanear, mais bonitas e com um design mais contemporâneo e profissional que incentiva o clique.

## 7. Aprendizado
**O que o grupo aprendeu sobre:**
*   **uso de branches:** Permitem o desenvolvimento isolado de funcionalidades ou testes sem quebrar o código principal (produção/main).
*   **merge:** É a forma de unificar diferentes linhas do tempo de um projeto, integrando código de forma colaborativa.
*   **conflitos no Git:** Ocorrem sempre que o sistema de controle de versão não consegue definir automaticamente o que preservar quando as mesmas linhas de código sofrem alterações concorrentes. Eles não são "erros", mas sim um pedido de intervenção humana para combinar as intenções com inteligência.

## 8. Autoavaliação do grupo
Dê uma nota de 0 a 10 para:
*   **Organização do grupo:** 10
*   **Entendimento da atividade:** 10
*   **Resultado final:** 10

**Justifique brevemente:**
O grupo conseguiu se coordenar bem para cumprir todos os requisitos da tarefa em ordem cronológica, usando os comandos git requeridos e produzindo uma página bem diagramada sem quebrar a navegabilidade do sistema original.
