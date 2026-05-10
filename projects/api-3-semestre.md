# PontoLog — Plataforma Web Acompanhamento Estatísticas Comércio Brasil

**2025-1**

**Empresa**: FATEC São José dos Campos - SP
Coord. Logística Marcus Nascimento

#### Problema: 
A principal barreira na análise dos dados do comércio exterior brasileiro está na forma como as informações são entregues. Bases como o Comex Stat oferecem dados brutos em arquivos enormes e nada amigáveis para quem precisa de uma visão rápida do cenário. Sem uma interface visual e interativa, o analista perde muito tempo tentando cruzar informações de NCMs, vias de transporte e URFs de forma manual. Esse processo, além de demorado, abre margem para falhas e impede que as empresas e órgãos tenham uma visão estratégica clara do mercado.

#### Solução:
Desenvolvemos uma plataforma web focada em simplificar a interpretação de dados de exportação e importação. Através de painéis visuais e gráficos interativos, o usuário consegue extrair insights detalhados de qualquer produto apenas pesquisando seu nome. O sistema permite visualizar o volume comercial por estado, país e município, além de identificar as vias de transporte mais utilizadas e as respectivas unidades da Receita Federal. A ferramenta também possibilita análises comparativas anuais, filtros por períodos específicos e confrontação direta de dados entre diferentes estados ou países.

##### [Repositório](https://github.com/CodeDontBlow/PontoLog)

#### Tecnologias Utilizadas
| **Tecnologia**  | **Funcionalidade**                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Python**           | Utilizado para o processamento, limpeza e análise estatística das bases de dados brutas. |
| **TypeScript**       | Linguagem base do projeto |
| **Postgresql**       | Banco de dados relacional responsável pelo armazenamento dos dados. |
| **Express.js**       | Framework para Node.js que gerencia as rotas e a comunicação (API) entre o banco de dados e o site. |
| **React.js**         | Biblioteca utilizada para criar a interface do usuário, focada em componentes interativos e dashboards. |
| **Redis**            | Banco de dados em memória que acelera o carregamento das páginas através do sistema de cache. |
| **Git**         | Sistema de controle de versão utilizado para gerenciar e versionar o código-fonte.                                   |
| **Figma** | Software de design usado para criar o protótipo visual e o layout das telas. |

## Contribuições Pessoais

### Desenvolvedor Back-End
Atuei como responsável pelo back-end, estabelecendo a fundação do sistema com **Express.js** para a criação de uma API REST eficiente. Implementei o **TypeORM** para o mapeamento de dados e integração com o banco **PostgreSQL**, garantindo uma comunicação segura e organizada com o servidor.

Para garantir a escalabilidade do projeto, adotei uma arquitetura baseada em separação de responsabilidades, dividindo o código em:

**Entidades**: Definição das estruturas de dados.

**Repositórios**: Gerenciamento das consultas ao banco de dados.

**Services**: Centralização da lógica de negócio e validações.

**Controllers**: Manipulação das rotas e requisições.

Além da parte estrutural, implementei o Redis para otimizar a experiência do usuário através do cache em memória, reduzindo o tempo de resposta da interface. No campo colaborativo, atuei compartilhando o conhecimento técnico com a equipe, garantindo que todos estivessem alinhados com a arquitetura e o fluxo de desenvolvimento


## Hard Skills
| Tecnologia      | Proficiência       | Descrição                                                                     |
| :-------------- | :----------------- | :---------------------------------------------------------------------------- |
| **Typescript**  | Autonomia     | Desenvolvimento completo da aplicação e integração de APIs.               |
| **Postgresql**       | Autonomia     | Modelagem do esquema relacional e implementação de consultas eficientes via TypeORM.                                 |
| **Python** | Com Auxilio | Scripting para o tratamento, limpeza e normalização de grandes volumes de dados brutos. |
| **Express.js** | Autonomia | Criação da arquitetura de API REST, gerenciamento de rotas e integração de middlewares. |
| **Redis** | Com Auxilia | Implementação de camadas de cache para otimizar a performance e reduzir a latência da aplicação. | 
| **Git**         | Autonomia | Controle de versão, trabalho em equipe com branches e gestão de repositórios. |


## Soft Skills
- **Proatividade:** *Foquei na antecipação de soluções para o projeto. Identifiquei gargalos de performance e propus prontamente a implementação do Redis para otimizar as consultas. Além disso, sugeri e apliquei o modelo Star Schema na arquitetura do banco, visando uma estrutura mais eficiente para a análise de grandes volumes de dados.*

- **Comunicação:** *Prezei pela transparência e pelo aprendizado em grupo. Toda nova tecnologia ou melhoria de código era compartilhada detalhadamente com a equipe, garantindo que todos estivessem tecnicamente alinhados. Isso evitou retrabalho e permitiu que o projeto seguisse um fluxo ágil.*

- **Colaboração** *Trabalhei em total sintonia com o time, garantindo que minhas tarefas estivessem sempre integradas ao progresso coletivo. Além de facilitar o fluxo de trabalho dos demais desenvolvedores, mantive o compromisso com a qualidade das entregas para que o projeto avançasse sem interrupções.*

- **Autonomia**: *Demonstrei independência na configuração completa do ambiente de desenvolvimento e na resolução de desafios técnicos complexos. Gerenciei meu próprio fluxo de trabalho com segurança, o que me permitiu cumprir os prazos estabelecidos sem a necessidade de supervisão constante, agindo como um suporte técnico confiável para o grupo.*

[Voltar](../README.md)