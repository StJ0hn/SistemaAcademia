# Sistema Organizacional de Academia

Aplicação para gerenciamento administrativo de academias, integrando lógica em Python com persistência em banco de dados relacional.

## Objetivo
Desenvolvido como trabalho final para a disciplina de Fundamentos de Banco de Dados na Universidade Federal do Ceará (UFC). O projeto foca na implementação de um ciclo completo de desenvolvimento de banco de dados: desde a modelagem entidade-relacionamento e normalização até a automação de processos via gatilhos (triggers) e otimização de consultas por meio de visões (views).

## Stack Tecnológico
* Linguagem: Python
* SGBD: PostgreSQL
* Driver de Conexão: Psycopg2
* Ferramentas de Modelagem: dbDiagram.io / draw.io

## Arquitetura e Funcionalidades Principais
O sistema foi estruturado para separar a definição de dados da lógica de aplicação, garantindo integridade e performance:
* Camada de Dados (SQL): Scripts DDL e DML organizados para criação de tabelas, restrições de integridade e povoamento inicial.
* Automação via Triggers: Implementação de gatilhos para validação de regras de negócio diretamente no motor do banco de dados.
* Consultas Avançadas e Views: Estruturação de visões para simplificar relatórios complexos e otimizar o acesso às informações mais críticas.
* Interface de Gerenciamento: CRUD completo desenvolvido em Python para interação com as entidades do sistema (alunos, instrutores, treinos e pagamentos).

## Estrutura do Repositório
* /docs: Documentação técnica contendo os modelos ER e Relacional.
* /sql: Scripts de definição, manipulação e objetos de banco de dados (Views e Triggers).
* /src: Código-fonte da aplicação e lógica de integração.

## Como Executar Localmente

1. Clone o repositório:
git clone https://github.com/StJ0hn/sistema-academia.git

2. Configure o ambiente virtual e instale as dependências:
python -m venv venv
source venv/bin/activate (ou venv\Scripts\activate no Windows)
pip install -r requirements.txt

3. Configure as credenciais do PostgreSQL no arquivo `.env` seguindo o modelo do `.env.example`.

4. Execute a aplicação:
python src/main.py

## Desafios Técnicos e Aprendizados
O principal desafio do projeto foi a tradução das regras de negócio complexas para o esquema relacional, garantindo a terceira forma normal (3FN) para evitar redundâncias. Além disso, a implementação de triggers para controle de estados no banco exigiu um estudo aprofundado sobre a ordem de execução de operações e integridade referencial, consolidando os fundamentos de persistência de dados.

---
Equipe: John Miguel da Silva Fernandes, Raquel Santos Silva e Enzo Andrade dos Anjos.
Orientação: Prof. Robertty Costa.
