# Projeto Integrado de Doação e Gestão de Banco de Sangue

## Apresentação

Este projeto apresenta uma solução completa para o ciclo de doação de sangue, desde a captação e qualificação do doador até a gestão e distribuição inteligente do estoque. O sistema é dividido em dois módulos principais e complementares:

1.  **E-TRIAGEM:** Uma plataforma focada em otimizar a experiência do doador, antecipando o questionário de triagem de primeiro nível para reduzir o tempo de espera e agilizar o processo no local da coleta.
2.  **NEED:** Um sistema de gestão de estoque (back-office) que visa otimizar a distribuição de bolsas de sangue entre as unidades, equilibrando o fornecimento com base na demanda, tipo sanguíneo e localização.

Juntos, os módulos criam um ecossistema mais eficiente, seguro e ágil para bancos de sangue.

## Especificação

### Módulo 1: E-TRIAGEM

-   **Principais Funcionalidades:**
    -   Cadastro e gerenciamento de voluntários (doadores).
    -   Preenchimento digital do questionário de triagem de primeiro nível (N1).
    -   Agendamento, cancelamento e remarcação de sessões de doação.
    -   Associação da triagem a uma sessão de doação específica.
    -   Manutenção de histórico de doações por usuário.

-   **Atores (Usuários):**
    -   **VOLUNTÁRIO:** Pessoa interessada em doar, que utiliza o sistema para se qualificar e agendar a doação.
    -   **TRIAGEM-N1:** Profissional ou sistema que valida os questionários.

### Módulo 2: NEED

-   **Principais Funcionalidades:**
    -   Cadastro e gerenciamento das unidades do banco de sangue.
    -   Controle de estoque de bolsas por tipo sanguíneo (O, A, B, AB...).
    -   Registro de entradas (doações) e saídas (retiradas) do estoque.
    -   Gerenciamento de usuários internos com diferentes permissões.
    -   Geração de relatórios para análise de distribuição e demanda.

-   **Atores (Usuários):**
    -   **Admin:** Gerencia o sistema, cadastra unidades e usuários.
    -   **Atendimento:** Opera o sistema no dia a dia, registrando doações e retiradas.
    -   **Doador:** Pode interagir com o sistema para consultar agendamentos.

### Tecnologias Envolvidas

-   **Linguagem:** [Ex: Python, Java, JavaScript]
-   **Banco de Dados:** [Ex: SQLite, PostgreSQL, MySQL]
-   **Frameworks:** [Ex: Django, Spring Boot, React]
-   **Outras Ferramentas:** [Ex: Docker, Git]

## Projeto

### Principais Entidades de Negócio

O sistema é modelado em torno de um conjunto de entidades que se interconectam entre os módulos:

-   **VOLUNTARIO / USUARIO:** Representa a pessoa física, seja como doador no E-TRIAGEM ou como usuário do sistema NEED. Contém dados cadastrais e histórico.
-   **SESSAO:** Entidade central que representa um agendamento. Inicia-se no E-TRIAGEM e, após a doação ser concluída, gera um registro de `DOACAO` no módulo NEED.
-   **TRIAGEM:** Armazena as respostas do questionário de pré-triagem, vinculada a um `VOLUNTARIO` e a uma `SESSAO`.
-   **UNIDADE:** Representa uma unidade física do banco de sangue, onde as doações ocorrem e o estoque é gerenciado.
-   **ESTOQUE:** Controla a quantidade de bolsas por tipo de sangue em cada `UNIDADE`.
-   **DOACAO / RETIRADA:** Registros que representam a movimentação do estoque, sendo a `DOACAO` o resultado de uma `SESSAO` bem-sucedida.

  ![]()
<img src="https://github.com/facclab-opositivo/maistriagem-/blob/main/projetos/Captura%20de%20tela%202025-09-25%20202225.png">
> Figura 1 - BD NEED

![]()
<img src="https://github.com/facclab-opositivo/maistriagem-/blob/main/projetos/Captura%20de%20tela%202025-09-25%20203901.png">
> Figura 2 - BO NEED

![]()
<img src="https://github.com/facclab-opositivo/maistriagem-/blob/main/projetos/Untitled%20diagram%20_%20Mermaid%20Chart-2025-09-25-231821.png">
> Figura 3 - BO E-triagem

![]()
<img src="https://github.com/facclab-opositivo/maistriagem-/blob/main/projetos/Untitled%20diagram%20_%20Mermaid%20Chart-2025-09-25-232014.png">
> Figura 4 - BD E-triagem 

## Resultados

### Aceitação

O sucesso do projeto integrado será medido pela combinação dos seguintes fatores:

1.  **Para o Doador (E-TRIAGEM):** Redução do tempo total do processo de doação e aumento da taxa de satisfação e de comparecimento dos voluntários.
2.  **Para o Banco de Sangue (NEED):** Melhoria na eficiência da gestão de estoque, redução do desperdício de bolsas de sangue e garantia de uma distribuição mais ágil e equilibrada entre as unidades.

O objetivo final é fortalecer a cadeia de doação, tornando-a mais atrativa para o doador e mais eficiente para a instituição.
