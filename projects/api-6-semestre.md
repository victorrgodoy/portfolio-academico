# Camplana — Plataforma Web com IA Generativa para Criação de Campanhas de Comissionamento

**2026-2**

**Empresa**: Empresa Dom Rock
André de Almeida

#### Problema
Empresas possuem regras de negócio para comissionamento que mudam constantemente devido a novos produtos, campanhas de vendas, alterações de preços e acordos comerciais. No entanto, essas regras muitas vezes não são registradas ou organizadas adequadamente. Essa falta de padronização dificulta a utilização, manutenção e rastreabilidade dos cálculos, gerando inconsistências operacionais, conflitos financeiros e uma enorme dependência do conhecimento tácito dos funcionários.

#### Solução
O Camplana: uma plataforma que utiliza IA Generativa explicável (a agente **Lana**) para planejar e simular campanhas de comissionamento. Pela plataforma, o gerente descreve a regra desejada em linguagem natural por meio de um chat. A IA interpreta o comando, extrai os parâmetros e permite que o usuário simule o impacto financeiro daquela campanha sobre o histórico real de vendas da empresa.
Para garantir precisão e evitar alucinações da IA, **nenhum cálculo financeiro vem diretamente da LLM**: a IA atua apenas gerando o código Python da regra. Esse código é executado em um ambiente isolado sobre o banco de dados e conferido contra um cálculo determinístico, retornando ao usuário um resultado explicável, rastreável e seguro.

##### [Repositório](https://github.com/codedontblow-org/domrock-camplana)

#### Tecnologias Utilizadas
| **Tecnologia**  | **Funcionalidade**                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Python**      | Linguagem base do microsserviço de Inteligência Artificial e processamento de dados isolado. |
| **FastAPI**     | Framework utilizado para expor as rotas HTTP do agente de IA e simulações. |
| **LangGraph**   | Biblioteca utilizada para orquestrar o fluxo, estado e as ferramentas (*tools*) do agente de IA (Lana). |
| **Java / Spring Boot** | Ecossistema utilizado para o desenvolvimento da API principal (Back-End), gerenciamento de regras de negócio, autenticação e segurança. |
| **Vue.js (Vue 3)** | Framework JavaScript progressivo utilizado para a construção de toda a interface do usuário (Front-End) no ecossistema Vite. |
| **PostgreSQL**  | Banco de dados relacional responsável por armazenar as informações do sistema, usuários e bases de vendas/RH. |
| **Docker**      | Plataforma de conteinerização utilizada para isolar os microsserviços (Front, Back, IA e Banco) e garantir padronização nos ambientes. |
| **gRPC**        | Protocolo de alta performance utilizado para a comunicação direta e rápida entre o Back-End (Spring) e o microsserviço de IA (FastAPI). |

## Contribuições Pessoais

### Desenvolvedor Front-End
Atuei no desenvolvimento da interface da aplicação utilizando **Vue.js 3** e **Vite**, com foco especial no módulo administrativo. Desenvolvi a tela de gerenciamento completo de usuários, criando tabelas dinâmicas com ordenação inteligente e *feedbacks* visuais (ex: usuários desativados renderizados em cinza no final da lista). 
Implementei formulários robustos de criação e edição com validações assíncronas (formato de e-mail, força de senha e obrigatoriedade de perfis), tratando os erros do backend (como o 409 de e-mail duplicado ou 400) diretamente na interface para melhorar a UX. Também apliquei regras de negócio no Front-end, como desabilitar ações inválidas (ex: bloquear o botão de autodesativação do administrador com *tooltips* explicativos). Toda essa camada de interface foi validada através de testes unitários utilizando o **Vitest**.

### Desenvolvedor Back-End & Segurança
Fui responsável por toda a estruturação da camada de segurança e controle de acessos da API principal utilizando **Spring Boot** e **Spring Security**. Implementei um sistema de autenticação via **JWT (JSON Web Token)** sem estado (*stateless*), com tempo de expiração seguro e criptografia de senhas utilizando **BCrypt**. 
Desenvolvi o **Role-Based Access Control (RBAC)**, garantindo que o roteamento das requisições respeitasse estritamente a matriz de perfis (Administrador, Gerente e Supervisor). Pensando na produtividade da equipe, criei um *profile dev* customizado no Spring que simulava autenticações via *headers*, acelerando os testes sem comprometer a segurança.
Atuei também no CRUD completo de Usuários, implementando o conceito de *Soft Delete* (desativação lógica via *migrations* no **Flyway**) para garantir a rastreabilidade histórica das campanhas. Para assegurar a confiabilidade de todas essas lógicas (exceções 401, 403 e 409), escrevi baterias completas de testes automatizados com **JUnit**.

### Engenharia de Dados & Inteligência Artificial
Atuei ativamente no motor de inteligência artificial (microsserviço *Lana*). Desenvolvi a ferramenta **Text-to-SQL**, que permite ao agente consultar o banco de dados de forma autônoma a partir de contextos fornecidos via RAG (Retrieval-Augmented Generation). 
Para garantir a segurança, integrei a API do **Google Gemini** implementando **Guardrails** rigorosos, limitando a IA apenas ao escopo desejado e validando as consultas SQL para evitar comportamentos inesperados. Fui o responsável por documentar toda essa arquitetura (Query Tool), incluindo diagramas e visão geral.
Além disso, atuei na **Engenharia de Dados** inicial: recebi os dados brutos de vendas e RH da empresa, realizei a normalização e criei os diagramas conceituais e lógicos que serviram de base estrutural para a modelagem do banco de dados relacional. Todo esse fluxo de IA e dados foi blindado com testes unitários em **Pytest**.

## Hard Skills
| Tecnologia      | Proficiência       | Descrição                                                                     |
| :-------------- | :----------------- | :---------------------------------------------------------------------------- |
| **Java / Spring Boot**| Autonomia     | Estruturação de APIs seguras, JWT, Spring Security e testes com JUnit. |
| **Python / FastAPI** | Autonomia     | Criação de microsserviços de IA, integração de LLMs e ferramentas (*tools*). |
| **Vue.js / Vitest** | Autonomia     | Criação de interfaces reativas, componentização, validação de formulários e testes de UI. |
| **PostgreSQL**  | Autonomia     | Modelagem do banco (conceitual/lógico), normalização de dados e *queries* seguras. |
| **LangGraph / LLM** | Autonomia | Desenvolvimento de agentes de IA, RAG, implementação de Guardrails e prompts. |
| **Docker**      | Autonomia     | Subida e integração do ecossistema de microsserviços localmente e em CI. | 

## Soft Skills
- **Foco em Qualidade e Resiliência:** *Implementei uma cultura forte de testes em todas as camadas (Vitest no Front, JUnit no Back e Pytest na IA). Isso garantiu que o código entregue desde as primeiras Sprints fosse altamente resiliente e documentado, reduzindo significativamente os bugs em produção.*
- **Visão Sistêmica (DX e UX):** *Além de focar no cliente final desenvolvendo interfaces com tratamento amigável de erros e validações em tempo real, também me preocupei com o time (Developer Experience). A criação do 'Profile Dev' no Spring para ignorar tokens durante o desenvolvimento acelerou muito o trabalho de integração dos outros desenvolvedores.*
- **Autonomia e Autogestão:** *Atuei de ponta a ponta na aplicação, navegando com fluidez entre banco de dados, construção da IA, segurança no backend e renderização na interface, entregando tarefas complexas dentro do prazo e liderando a documentação de arquiteturas críticas, como a Query Tool.*

[Voltar](../README.md)