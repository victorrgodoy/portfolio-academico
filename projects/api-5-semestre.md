# Orbita — Plataforma Centralizada de Atendimento e Triagem Inteligente

**2026-1**

**Empresa**: Empresa Pro4Tech
Rafael Monteiro

#### Problema
A empresa enfrenta gargalos operacionais no relacionamento com o cliente devido à fragmentação dos canais de atendimento. A falta de uma triagem inicial centralizada resulta em sobrecarga dos atendentes com dúvidas repetitivas, além de erros e lentidão no direcionamento dos chamados para os níveis corretos de suporte. Sem um sistema unificado, o histórico de interações se perde, gerando retrabalho, falta de rastreabilidade para os gestores e, consequentemente, uma experiência frustrante e ineficiente para o cliente final. 

#### Solução
O Orbita: uma plataforma integrada que centraliza e automatiza o fluxo de atendimento. A jornada começa com uma triagem inteligente via aplicativo mobile, que resolve demandas simples e direciona os casos complexos de forma assertiva para equipes humanas estruturadas por níveis de suporte.
A solução oferece flexibilidade total: os clientes interagem por um aplicativo mobile moderno, os atendentes operam via web, e os administradores gerenciam filas e monitoram o desempenho em tempo real por meio de um painel web robusto. Tudo isso com registro automatizado do histórico de ponta a ponta, garantindo controle gerencial e eficiência operacional.

##### [Repositório](https://github.com/CodeDontBlow/pro4tech-Orbita)

#### Tecnologias Utilizadas
| **Tecnologia**  | **Funcionalidade**                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Docker** | Plataforma de conteinerização utilizada para isolar e padronizar os ambientes de desenvolvimento e produção, facilitando o deploy dos bancos de dados e serviços. |
| **TypeScript**       | Linguagem utilizada no desenvolvimento do frontend e backend da aplicação, garantindo tipagem estática e segurança ao código. |
| **Postgresql**       | Banco de dados relacional responsável pelo armazenamento estruturado das informações do sistema (usuários, chamados, permissões). |
| **Mongodb**          | Banco de dados não relacional utilizado para armazenar dados flexíveis e de rápida leitura, como as mensagens e históricos dos chats. |
| **Nest.js**           | Framework escalável em Node.js utilizado para a construção da API RESTful do backend. |
| **Next.js** |         Framework React utilizado para o desenvolvimento do frontend web, permitindo renderização no lado do servidor (SSR), gerenciamento eficiente de rotas e otimização de performance.
| **React.js**         | Biblioteca utilizada para construir a interface web do usuário, com foco em componentes interativos, painéis e dashboards. |
| **Tailwind CSS**         | Framework CSS utilizado para a estilização e construção dos elementos visuais da interface web. |
| **MiniIO** |          Servidor de armazenamento de objetos de alta performance, utilizado para gerenciar e armazenar mídias, imagens e anexos trafegados no chat. |
| **Git**         | Sistema de controle de versão utilizado para gerenciar e versionar o código-fonte.                                   |
| **Figma** | Software de design usado para criar o protótipo visual e o layout das telas. |

## Contribuições Pessoais

### Desenvolvedor Back-End
Fui responsável por estruturar toda a infraestrutura de containers Docker do projeto, criando e configurando o ambiente com docker-compose, garantindo que toda a equipe tivesse um ambiente padronizado, isolado e pronto para desenvolvimento desde o início do projeto.

Além disso, atuei como responsável pelo desenvolvimento do Back-End da plataforma, utilizando o ecossistema NestJS com foco em uma arquitetura modular altamente escalável, tipada e organizada. Implementei o padrão de camadas dentro de cada módulo do framework, dividindo as responsabilidades da seguinte forma:
Controllers: Gerenciamento de rotas, validação de requisições (DTOs) e controle de entrada/saída de dados.
Services: Centralização, isolamento e execução de toda a lógica de negócio da aplicação.
Repositories + Prisma ORM: Camada isolada para comunicação direta com o banco de dados, utilizando o Prisma como ORM para garantir consultas eficientes, seguras e com tipagem estática ponta a ponta.
Além disso, fui o responsável por estruturar a camada de segurança do sistema, desenvolvendo NestJS Guards customizados para validação de autenticação e autorização via RBAC (Role-Based Access Control). Isso garantiu o controle estrito de acessos às rotas com base nos papéis de usuários (Admin, Agent e Client), além de liderar a implementação das demais regras de negócio críticas nos módulos do sistema.

### Desenvolvedor Front-End
Atuei desde o início no desenvolvimento da aplicação Web, utilizando o ecossistema Next.js para construir uma interface performática, escalável e segura. Minhas principais contribuições envolveram:
Autenticação e Segurança no Servidor: Implementei o controle de acesso baseado em cookies utilizando Middleware/Interceptors do Next.js. O sistema lê o cookie diretamente no lado do servidor (Server-Side) para identificar a role (papel) do usuário em tempo real. Isso me permitiu blindar as rotas da aplicação, separando de forma segura os fluxos e telas de login específicos para Agent e Admin.
Arquitetura de Componentes: Estruturei o projeto seguindo as melhores práticas de arquitetura do Next.js, criando um padrão de componentes compartilhados e reutilizáveis. Isso garantiu a consistência visual da plataforma, facilitou a manutenção do código e acelerou o desenvolvimento de novas funcionalidades (como os dashboards e telas de chat).

## Hard Skills
| Tecnologia      | Proficiência       | Descrição                                                                     |
| :-------------- | :----------------- | :---------------------------------------------------------------------------- |
| **Docker** | Autonomia | Criação e configuração de containers e orquestração de serviços necessários para rodar a aplicação localmente |
| **Typescript**  | Autonomia     | Desenvolvimento completo da aplicação (frontend e backend), garantindo tipagem estática e segurança ao código.               |
| **PostgreSQL** | Autonomia     | Modelagem do esquema relacional e implementação de consultas eficientes utilizando o Prisma ORM.
| **Nest.js** | Autonomia | Gerenciamento e estruturação da API RESTful do backend através de uma arquitetura modular, além da criação de Guards para segurança.  | 
| **React.js** | Autonomia | Criação da interface do usuário com foco em componentes interativos, reaproveitáveis e estruturação de layouts.
| **Next.js** | Autonomia | Desenvolvimento do ecossistema web com renderização no lado do servidor (SSR), controle de rotas e autenticação/validação de papéis via cookies.
| **Mongodb** | Com Ajuda | Armazenamento de dados flexíveis e de rápida leitura, como a persistência de mensagens e históricos dos chats. |
| **Tailwind CSS** | Autonomia | Estilização da interface utilizando classes utilitárias para construção de layouts, componentes visuais e responsividade. |
| **Git**         | Autonomia | Controle de versão, trabalho em equipe com branches e gestão de repositórios. |

## Soft Skills
- **Proatividade:** *Demonstrei forte iniciativa desde o primeiro dia do projeto. Fui o responsável por antecipar as necessidades técnicas da equipe ao configurar toda a infraestrutura inicial com Docker e estruturar a arquitetura base do Back-End. Essa ação garantiu que o time tivesse um ambiente pronto, padronizado e escalável para começar a desenvolver sem gargalos.*

- **Autonomia**: *Sempre pautei meu trabalho na independência e na confiabilidade. Demonstrei alta capacidade de autogerenciamento ao resolver bugs complexos por conta própria e ao implementar regras de negócio refinadas. Além disso, fiz a gestão dos meus próprios prazos de entrega, garantindo a qualidade do código sem a necessidade de microgerenciamento.*

[Voltar](../README.md) 
