# Chatbot AI SQL — Chatbot Inteligente para Consultas em Banco de Dados

**2024-1**

**Empresa**: FATEC São José dos Campos - SP
Profº Giuliano Bertoti

#### Problema: 
A empresa parceira enfrentava barreiras no acesso a informações estratégicas em sua base de dados. O processo de extração de dados era manual e exigia conhecimento técnico em SQL, o que gerava gargalos operacionais, inconsistências nos relatórios e atrasos na tomada de decisão por parte dos colaboradores não técnicos.

#### Solução:
Desenvolvimento de uma aplicação desktop que utiliza Inteligência Artificial para converter linguagem natural em comandos SQL. A solução permite que o usuário interaja com o banco de dados de forma intuitiva, oferecendo suporte a múltiplos modelos de linguagem (LLMs) e diferentes sistemas gerenciadores de banco de dados, garantindo flexibilidade e privacidade ao processar os dados localmente.

##### [Repositório](https://github.com/victorrgodoy/chatbot-ai-sql)

#### Tecnologias Utilizadas
| **Tecnologia**  | **Funcionalidade**                                                                                                   |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Java**       | Linguagem principal utilizada tanto para a lógica de backend quanto para a interface gráfica (Swing). |
| **MySQL**       | Armazenamento de informações do usuário                                                                              |
| **LangChain4j** | Framework de integração para orquestração de LLMs e encadeamento de prompts em Java.                                                           |
| **Ollama**   | Runtime utilizado para execução local de modelos de linguagem de larga escala.                                                             |
| **Git**         | Sistema de controle de versão utilizado para gerenciar e versionar o código-fonte.                                   |

## Contribuições Pessoais

### Engenharia de Prompt e Integração de LLMs
Atuei como desenvolvedor responsável pela pesquisa e seleção do modelo **duckdb-nsql:7b**, especializado na tradução de linguagem natural para SQL. Minha principal contribuição foi o desenvolvimento de uma estratégia de **Prompt Engineering**, estruturando o contexto (DDL do banco de dados) para minimizar alucinações da IA e garantir a precisão das queries geradas.

Utilizei o framework **LangChain4j** para realizar a comunicação assíncrona entre o sistema em Java e o servidor local **Ollama**. Além disso, projetei a arquitetura para que a aplicação permitisse que o usuário alterne entre diferentes LLMs instalados na máquina para equilibrar performance e hardware.

<details>
<code class="language-java">  

    public static String sendOllamaQuestion(String ddl, String question, String nameModel)  {

        OllamaChatModel model = OllamaChatModel.builder()
                .baseUrl("http://localhost:11434") //host ollama server
                .modelName(nameModel)
                .temperature(0.4)
                .build();
        
        String instructions = "Task\n" +
                    "Generate a SQL query to answer [QUESTION]"+question+"[/QUESTION]\n" +
                    "Instructions\n" +
                    "If you cannot answer the question with the available database schema, return 'Eu não sei'. No explanation needed.\n" +
                    "Database Schema\n" +
                    "The query will run on a database with the following schema: "+ ddl + "\n" +
                    "Answer\n" +
                    "Given the database schema, here is the SQL query that answers [QUESTION]"+question+"[/QUESTION]\n" +
                    "[SQL] Your SQL query goes here[/SQL]";

        return model.generate(instructions);
    }
</code>
</details>

### Desenvolvimento Full Stack e Arquitetura
Implementei a camada de persistência e a lógica de execução das queries retornadas pela IA, integrando-as ao MySQL. No frontend, utilizei Java Swing para criar uma interface de chatbot, focada na experiência do usuário final.

## Hard Skills
| Tecnologia      | Proficiência       | Descrição                                                                     |
| :-------------- | :----------------- | :---------------------------------------------------------------------------- |
| **Java**        | Autonomia     | Desenvolvimento completo da aplicação (MVC) e integração de APIs.               |
| **MySQL**       | Autonomia     | Modelagem e desenvolvimento do banco de dados                                 |
| **LangChain4j** | Autonomia     | Orquestração de fluxos de IA e gerenciamento de contexto de chat.                                                        |
| **Ollama**   | Autonomia     | Configuração de modelos LLM locais.                                          |
| **Git**         | Autonomia | Controle de versão, trabalho em equipe com branches e gestão de repositórios. |


## Soft Skills
- **Proatividade:** *Tomei a iniciativa na fase de pesquisa técnica, identificando os modelos de LLM mais eficientes no Ollama e estruturando o MVP (Mínimo Produto Viável) do projeto. Minha experiência prévia em Java permitiu acelerar a entrega da base do sistema.*

- **Comunicação:** *Promovi o alinhamento técnico entre os membros da equipe que exploravam diferentes abordagens. Liderei a integração dos módulos desenvolvidos separadamente, garantindo que a melhor solução técnica (em termos de arquitetura e modelo de IA) fosse adotada como padrão do projeto.*

[Voltar](../README.md)