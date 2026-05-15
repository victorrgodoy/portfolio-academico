# Descriptum — Agente de Inteligência Artificial para Registro de Importação

**2025-2**

**Empresa**: Empresa TecSys
Creonice Honório

#### Problema
Os funcionários da empresa relatavam que demoravam muito tempo para encontrar todos os dados relacionados a um determinado produto importado. Após reunir essas informações, era necessário criar manualmente uma planilha que posteriormente seria utilizada para apresentar os detalhes da importação à Receita Federal. Como a empresa importa muitos produtos eletrônicos, esse processo era demorado e exigia bastante trabalho operacional.

#### Solução
Foi desenvolvida uma página web para automatizar esse fluxo. O sistema recebia um PDF gerado pela empresa contendo o código do produto. A partir desse código, eram realizadas buscas em sites especializados para localizar informações correspondente ao produto.
Após encontrar as informações do produto, os dados eram enviados para uma IA de embeddings, responsável por comparar os resultados encontrados com a tabela oficial do governo, identificando assim o NCM mais adequado.
Por fim, o sistema gerava automaticamente uma planilha Excel contendo todas as informações necessárias, como nome do produto, código NCM, região e demais dados exigidos pela Receita Federal. Com isso, o processo passou a ser realizado em muito menos tempo e com menor esforço manual.

##### [Repositório](https://github.com/CodeDontBlow/Tecsys-Descriptum)

#### Tecnologias Utilizadas
| **Tecnologia**  | **Funcionalidade**                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| **TypeScript**       | Linguagem utilizada no desenvolvimento do frontend da aplicação. |
| **Python**           | Linguagem utilizada no desenvolvimento do backend e nas integrações com IA. |
| **Postgresql**       | Banco de dados relacional responsável pelo armazenamento das informações do sistema. |
| **FastAPI**          | Framework Python utilizado para gerenciar as rotas e a comunicação da API entre o frontend e o banco de dados. |
| **React.js**         | Biblioteca utilizada para construir a interface do usuário, com foco em componentes interativos e dashboards. |
| **Chromadb**         | Banco de dados vetorial utilizado para armazenar embeddings e realizar buscas semânticas relacionadas aos códigos NCM.|
| **Git**         | Sistema de controle de versão utilizado para gerenciar e versionar o código-fonte.                                   |
| **Ollama** | Ferramenta utilizada para execução local de modelos de inteligência artificial. |
| **Figma** | Software de design usado para criar o protótipo visual e o layout das telas. |

## Contribuições Pessoais

### Desenvolvedor Back-End
Atuei como responsável pelo desenvolvimento do Back-End, com foco em arquitetura de alto desempenho e integração de Inteligência Artificial. Minhas principais contribuições incluíram:

Arquitetura e API: Participei ativamente do desenho da arquitetura do sistema utilizando FastAPI, garantindo uma aplicação escalável, rápida e de fácil manutenção.

Processamento de Dados e IA: Implementei o pipeline de dados para IA, realizando a extração e o tratamento (limpeza) das tabelas oficiais de NCM (Nomenclatura Comum do Mercosul) do governo.

Busca Vetorial (Embeddings): Responsável pela vetorização dos dados de NCM utilizando ChromaDB. Essa implementação permitiu a criação de um sistema de busca semântica eficiente para comparar e validar os dados dos produtos com a base oficial de forma automatizada.

## Hard Skills
| Tecnologia      | Proficiência       | Descrição                                                                     |
| :-------------- | :----------------- | :---------------------------------------------------------------------------- |
| **Python**  | Autonomia     | Desenvolvimento completo da aplicação e integração de APIs.               |
| **PostgreSQL** | Autonomia     | Modelagem do esquema relacional e implementação de consultas eficientes via TypeORM.                                 |
| **ChromaDB** | Autonomia | Gerenciamento de bancos vetoriais e otimização de busca por similaridade. | 
| **Git**         | Autonomia | Controle de versão, trabalho em equipe com branches e gestão de repositórios. |

## Soft Skills
- **Proatividade:** *Tomei a iniciativa de pesquisar e implementar tecnologias de LLM Embeddings e bancos de dados vetoriais logo no início do projeto, antecipando desafios técnicos e buscando constantemente a melhoria na precisão dos resultados de busca.*

- **Comunicação:** *Prezei pela transparência e compartilhamento de conhecimento. Todas as descobertas sobre novas tecnologias foram detalhadas para a equipe, alinhando o nível técnico de todos e evitando retrabalho.*

- **Autonomia**: *Demonstrei independência na configuração do ambiente de desenvolvimento e na resolução de bugs complexos. Gerenciei meus próprios prazos, servindo como um ponto de apoio técnico confiável para o grupo sem a necessidade de supervisão constante.*

[Voltar](../README.md) 