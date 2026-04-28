# 🚀 Respostas da Atividade: Atualização de Branch com Hotfix e Resolução de Conflitos

## 1. Entendimento do Conflito

> **O que causou o conflito no arquivo `index.html`?**

O conflito foi gerado devido a edições simultâneas no mesmo bloco de código em branches distintas. A branch principal (`main`/produção) recebeu uma correção de emergência (hotfix) que alterou os diretórios dos links inserindo `pages/`. Paralelamente, na nossa branch de desenvolvimento, havíamos customizado os rótulos de exibição desses mesmos links. Quando tentamos unificar o trabalho, o Git não soube qual alteração priorizar.

> **Em qual parte do código ele ocorreu?**

O conflito incidiu nas tags de ancoragem (`<a>`) do menu lateral "DESTAQUES DO CURSO", localizadas aproximadamente entre as linhas 38 e 43 do arquivo `index.html`.

---

## 2. Processo de Resolução

> **Qual opção vocês utilizaram inicialmente?**

- [ ] Accept Current (Manter a versão atual)
- [ ] Accept Incoming (Aceitar a modificação que está chegando)
- [x] **Accept Both** (Combinação manual de ambas as alterações)

> **Foi necessário ajuste manual após isso? Explique o que foi feito.**

Sim. A opção de aceitar ambas inseriu as duas versões no código, exigindo uma refatoração manual. Limpamos os marcadores de conflito do Git (`<<<<<<<`, `=======`, `>>>>>>>`) e reescrevemos as tags fundindo as duas necessidades: inserimos o caminho atualizado (`href="pages/..."`) e mantivemos o novo texto descritivo do botão.

---

## 3. Decisão Técnica

> **Quais partes do código da `main` vocês mantiveram?**

Adotamos exclusivamente a estrutura de rotas corrigida pelo hotfix, ou seja, o valor atualizado dos atributos de destino (ex: `href="pages/laboratory.html"`).

> **Quais partes da sua branch foram preservadas?**

Preservamos toda a customização visual e de texto que havíamos desenvolvido (ex: os nomes de exibição `Labs de TI`, `Eventos`, `Jornada SI`).

---

## 4. Dificuldades Encontradas

> **Quais foram as principais dificuldades durante o processo?**

- **O merge:** A principal tensão foi garantir que a integração do hotfix ocorresse de forma fluida, sem sobrescrever ou perder o trabalho de layout que já havíamos consolidado na nossa _feature branch_.
- **A resolução de conflitos:** Exigiu atenção redobrada na leitura do código para não gerar uma sintaxe HTML quebrada ou tags duplicadas na hora de juntar a `HEAD` com a `origin`.
- **A melhoria de layout:** Escolher os componentes adequados do framework e definir uma paleta de ícones que fizesse sentido para o contexto dos laboratórios, mantendo a harmonia e a hierarquia visual da interface.

---

## 5. Solução Adotada

> **Como o grupo resolveu os problemas encontrados? Houve necessidade de pesquisar? Onde?**

A resolução do código em si foi feita com revisão linha a linha, combinando lógica e paciência para entender a intenção de cada branch. Para os desafios de design, recorremos ativamente à documentação oficial do **Bootstrap 5**, focando nas seções de _Cards_ e classes utilitárias. Também utilizamos a biblioteca do **Bootstrap Icons** para buscar a iconografia correta que ilustrasse cada ambiente.

---

## 6. Melhoria de Layout

> **Qual página foi escolhida para melhoria?**

Focamos nossos esforços na página `laboratory.html`.

> **Quais mudanças visuais foram implementadas? Qual foi o objetivo dessas melhorias?**

Substituímos o visual estático por uma estrutura de cartões (_Cards_) modernizada. Implementamos sombras suaves (`shadow-sm` / `shadow`), bordas coloridas no topo para destaque (`border-top border-success`), cantos arredondados e integramos ícones vetoriais junto aos títulos. O objetivo foi transformar um texto maçante em informações altamente escaneáveis, melhorando a Experiência do Usuário (UX) com uma interface mais limpa e profissional.

---

## 7. Aprendizados

> **O que o grupo aprendeu sobre:**

- **Uso de branches:** São ambientes isolados e seguros. Elas nos dão liberdade para inovar, testar ou consertar falhas sem o risco de quebrar o sistema que está em produção.
- **Merge:** É o ponto de convergência do trabalho em equipe; o mecanismo essencial para integrar diferentes linhas de desenvolvimento em um código unificado.
- **Conflitos no Git:** Compreendemos que conflitos não são "erros", mas sim uma trava de segurança do versionamento. Eles acontecem quando o sistema não consegue deduzir a intenção lógica sobre a mesma linha de código, exigindo um olhar humano e colaborativo para a tomada de decisão.

---

## 8. Autoavaliação do Grupo

- **Organização do grupo:** 10
- **Entendimento da atividade:** 10
- **Resultado final:** 10

> **Justificativa:**

A equipe atuou de forma sinérgica e metódica. Cumprimos todas as etapas técnicas de versionamento e resolução exigidas, e ainda fomos além do básico na reestruturação da interface gráfica. O resultado foi um repositório limpo, atualizado e uma aplicação visualmente superior à original.
