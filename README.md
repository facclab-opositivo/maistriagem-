# Projeto E-TRIAGEM

## Apresentação
O projeto E-TRIAGEM visa otimizar o processo de doação de sangue, reduzindo o tempo de espera, o envolvimento desnecessário e os translados. A solução antecipa o questionário obrigatório da entrevista de triagem de primeiro nível, permitindo que o voluntário chegue ao local de doação com uma etapa já concluída.

## Especificação

### Principais Funcionalidades
-   Cadastro e gerenciamento de voluntários (doadores).
-   Realização de questionário de triagem de primeiro nível (N1) de forma digital.
-   Agendamento, cancelamento e remarcação de sessões de doação.
-   Associação de um doador e sua triagem a uma sessão específica.
-   Manutenção de histórico de doações e triagens por usuário.

### Atores (Usuários)
-   **VOLUNTÁRIO:** Pessoa interessada em doar sangue, que preenche o formulário de triagem e agenda sua doação.
-   **TRIAGEM-N1:** Profissional de saúde ou sistema responsável por validar e processar os questionários de triagem.

### Tecnologias Envolvidas
-   **Linguagem:** [Ex: Python, Java, JavaScript]
-   **Banco de Dados:** [Ex: SQLite, PostgreSQL, MySQL]
-   **Frameworks:** [Ex: Django, Spring Boot, React]
-   **Outras Ferramentas:** [Ex: Docker, Git]

## Projeto

### Principais Entidades de Negócio
-   **VOLUNTARIO:** Armazena os dados cadastrais do doador (Nome, CPF, Contato, etc.).
-   **SESSAO:** Representa um agendamento de doação, contendo informações como data, hora, status (agendada, cancelada, remarcada) e o voluntário associado.
-   **TRIAGEM:** Contém as respostas do questionário de pré-triagem do voluntário, associada a uma sessão.
-   **USUARIO:** Entidade para controle de acesso e histórico.
-   **HISTORICO:** Registro das atividades e doações passadas do usuário.

## Resultados

### Aceitação
O projeto busca ser validado através da redução do tempo médio do processo de doação, do aumento da taxa de comparecimento aos agendamentos e da satisfação dos voluntários, medida por meio de pesquisas de feedback. Espera-se que a plataforma simplifique e incentive o ato de doar sangue.
