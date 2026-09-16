# Ementa — GitHub Copilot para Engenharia de Software Moderna

## Visão geral

O treinamento apresenta o GitHub Copilot como colaborador ao longo do ciclo de desenvolvimento de software, sempre sob supervisão humana. O programa foi consolidado em **três módulos de 240 minutos**, com prioridade para demonstrações, prática guiada, critérios de decisão e evidências verificáveis.

Os guias [GH-300](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-300) e [GH-600](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600) orientam a cobertura, mas o treinamento não tem como objetivo preparar para exames de certificação.

Antes do primeiro módulo, os participantes devem concluir o [pre-work](https://github.com/impacta-ghcp-eng-moderna/00-pre-work) para validar o acesso ao GitHub, a criação de repositórios, o GitHub Codespaces e a execução da aplicação.

## Módulo 01 — Do requisito à aplicação

### Resultado de aprendizagem

Ao final do módulo, o participante deverá reconhecer como o Copilot pode apoiar um fluxo de desenvolvimento completo, escolher a forma de interação adequada no VS Code e transformar requisitos em incrementos verificáveis, mantendo responsabilidade sobre contexto, decisões, código e validação.

### Formato

O módulo combina um grande walkthrough com um laboratório prático:

1. [Walkthrough: desenvolvimento assistido pelo Copilot](https://github.com/impacta-ghcp-eng-moderna/01-walkthrough-desenvolvimento-assistido);
2. [Lab 01: inscritos em treinamentos](https://github.com/impacta-ghcp-eng-moderna/01-lab).

### Conteúdo

| Tema | Conteúdo apresentado |
| --- | --- |
| Intenção e requisitos | Construção de uma especificação versionada, definição de escopo, contratos, critérios de aceitação e exemplos; comparação entre abordagens zero-shot e few-shot. |
| Contexto durável | Uso de repository instructions para registrar convenções e decisões relevantes para o trabalho no repositório. |
| Superfícies e agentes | Escolha entre sugestões inline, Ask, Plan e Agent de acordo com a complexidade, o risco e o grau de autonomia necessário. |
| Desenvolvimento em fatias verticais | Implementação incremental de API, persistência, interface e testes a partir de um mesmo requisito. |
| API e tratamento de erros | Criação e revisão de contratos HTTP, DTOs, validações, respostas de erro e documentação OpenAPI. |
| Prompt files | Extração de um método validado para um prompt reutilizável, com parâmetros, contexto e validações explícitas. |
| Persistência | Modelagem do domínio, configuração do Entity Framework Core, migrations e validação da persistência. |
| Interface | Integração de uma aplicação Blazor WebAssembly com a API e tratamento dos estados de carregamento, sucesso e erro. |
| Qualidade e entrega | Testes derivados dos critérios de aceitação, revisão do contrato OpenAPI e automação de build e testes com GitHub Actions. |
| Checkpoints e recuperação | Uso de estados recuperáveis para reduzir repetição sem ocultar decisões, contratos ou evidências. |
| Supervisão humana | Revisão de mudanças inesperadas, atualização da especificação antes do código e aceitação baseada em evidências. |

### Laboratório

O participante amplia a aplicação construída no walkthrough com o cadastro e a listagem de inscritos em treinamentos. A atividade exercita leitura da especificação, planejamento, implementação incremental, testes e validação do resultado.

**Apresentação:** [baixar slides do Módulo 01](./apresentacoes/01-ghcp-eng-moderna.pptx?raw=1)

## Módulo 02 — Da personalização ao controle

### Resultado de aprendizagem

Ao final do módulo, o participante deverá escolher o mecanismo de personalização adequado para cada necessidade, limitar contexto e ferramentas, delegar tarefas especializadas, observar ações do agente e integrar capacidades externas com controles proporcionais ao risco.

### Formato

O módulo é conduzido como uma sequência de demonstrações independentes, cada uma em seu próprio repositório, seguida de um laboratório:

1. [Instruction files](https://github.com/impacta-ghcp-eng-moderna/02-demo-instructions);
2. [Prompt files](https://github.com/impacta-ghcp-eng-moderna/02-demo-prompt-file);
3. [Custom agents, subagents e handoffs](https://github.com/impacta-ghcp-eng-moderna/02-demo-custom-agents);
4. [Agent Skills](https://github.com/impacta-ghcp-eng-moderna/02-demo-agent-skills);
5. [Hooks: logs no Copilot CLI](https://github.com/impacta-ghcp-eng-moderna/02-demo-hooks-logs);
6. [Hooks: logs no VS Code](https://github.com/impacta-ghcp-eng-moderna/02-demo-hooks-logs-vscode);
7. [Hooks: prevenção](https://github.com/impacta-ghcp-eng-moderna/02-demo-hooks-prevencao);
8. [GitHub MCP Server](https://github.com/impacta-ghcp-eng-moderna/02-demo-mcp-server);
9. [Lab 02: revisão delegada e correção supervisionada](https://github.com/impacta-ghcp-eng-moderna/02-lab).

### Conteúdo

| Tema | Conteúdo apresentado |
| --- | --- |
| Escolha do mecanismo | Comparação entre instructions, prompt files, skills, custom agents, hooks e MCP conforme necessidade, gatilho, escopo e responsabilidade. |
| Instructions | Instruções de repositório, por caminho, pessoais e organizacionais; descoberta, aplicabilidade, composição, front matter e limites de precedência. |
| Prompt files | Criação de templates de tarefas repetitivas com entradas, contexto, ferramentas e critérios de validação explícitos. |
| Custom agents | Definição de papel, comportamento, ferramentas e limites de um agente especializado. |
| Subagents e handoffs | Separação entre coordenação, pesquisa, julgamento e implementação; delegação em contexto isolado e transferência supervisionada para o próximo papel. |
| Menor privilégio | Distribuição de ferramentas conforme a responsabilidade de cada agente e distinção entre leitura, busca, edição e execução. |
| Agent Skills | Organização de conhecimento, procedimentos, recursos e scripts reutilizáveis; descoberta automática e carregamento progressivo. |
| Hooks | Diferença entre orientar o modelo e executar controles; eventos e contratos do Copilot CLI, cloud agent e Agent mode no VS Code. |
| Observabilidade | Registro de eventos em JSONL para correlacionar sessão, prompt, ferramentas, subagentes e conclusão. |
| Prevenção | Uso de hooks para bloquear mutações em arquivos críticos, combinado com controles de defesa em profundidade. |
| Model Context Protocol | Conceitos de cliente, servidor, tools, autenticação e confirmação; uso do GitHub MCP Server para investigação remota. |
| Permissões externas | Distinção entre ferramentas expostas ao agente e permissões concedidas por autenticação ou OAuth. |
| Validação | Uso de evidências determinísticas para confirmar que instructions, skills, agentes, hooks e integrações produziram o comportamento esperado. |

### Laboratório

O participante configura um fluxo de revisão delegada com um subagent pesquisador, um agente coordenador e um handoff para correção supervisionada. A atividade exige conferir evidências, classificar conclusões e implementar somente uma lacuna confirmada, seguida de revisão do diff e validação focada.

**Apresentação:** [baixar slides do Módulo 02](./apresentacoes/02-ghcp-eng-moderna.pptx?raw=1)

## Módulo 03 — GitHub Copilot no SDLC

### Resultado de aprendizagem

Ao final do módulo, o participante deverá delimitar e delegar uma entrega agêntica, interpretar as evidências produzidas ao longo do SDLC e aplicar revisão, aprovações e guardrails sem substituir julgamento humano por automação.

### Formato

O módulo consiste em uma única grande demonstração, mantida no repositório [GitHub Copilot no SDLC](https://github.com/impacta-ghcp-eng-moderna/03-demo-sdlc), e dividida em duas partes complementares.

### Parte 1 — Da issue à produção

Uma solicitação aparentemente simples percorre um fluxo automatizado completo:

1. registro do requisito em uma issue;
2. delegação para o cloud agent;
3. exploração, planejamento, implementação e testes em ambiente remoto;
4. abertura do pull request e inspeção das evidências;
5. Copilot Code Review;
6. required checks, aprovação, auto-merge e pipeline final.

Embora especificação, código, testes, revisão e pipeline sejam consistentes entre si, a entrega resolve o problema errado porque uma premissa de negócio não foi questionada. O cenário demonstra que estar no loop não equivale a supervisionar e que evidências técnicas não validam, sozinhas, a intenção do produto.

### Parte 2 — Automatizar sem abandonar o controle

O fluxo é reconstruído com fronteiras de decisão explícitas:

| Tema | Conteúdo apresentado |
| --- | --- |
| Problema e hipótese | Separação entre a observação do problema, a hipótese inicial e a solução aprovada. |
| Especificação | Uso da especificação como ponto de decisão e fonte de contratos verificáveis antes da implementação. |
| Responsabilidade | Definição de responsáveis com CODEOWNERS e exigência de revisão pelas pessoas adequadas. |
| Delegação delimitada | Escopo, restrições e critérios claros para o cloud agent, preservando decisões de domínio para revisão humana. |
| Evidências independentes | Verificação da especificação, dos testes, do comportamento e do diff por fontes distintas. |
| Copilot Code Review | Uso da revisão automatizada como segunda opinião, com classificação, validação e decisão humana sobre cada comentário. |
| Proteções do repositório | Rulesets, required reviews, required checks, descarte de aprovações antigas e resolução de conversas. |
| Publicação | Separação entre gerar um artefato e autorizar uma implantação, com ambientes e aprovações proporcionais ao risco. |
| Autonomia proporcional | Aumento gradual de controles conforme impacto, reversibilidade e sensibilidade da ação. |
| Checklist de entrega | Verificação de problema, contrato, escopo, risco, evidências e decisão antes, durante e depois da execução agêntica. |

O módulo incorpora os conteúdos de qualidade e operação responsável que antes estavam previstos em um quarto módulo. Não há laboratório separado: a análise comparativa das duas partes é a atividade central.

**Apresentação:** [baixar slides do Módulo 03](./apresentacoes/03-ghcp-eng-moderna.pptx?raw=1)

## Cobertura dos guias de referência

| Guia | Domínio | Cobertura principal |
| --- | --- | --- |
| GH-300 | Uso responsável, prompting e construção de contexto | Módulos 01 e 02 |
| GH-300 | Desenvolvimento assistido, testes, documentação e produtividade | Módulos 01 e 03 |
| GH-300 | Personalização do Copilot | Módulo 02 |
| GH-300 | Copilot no VS Code, CLI e GitHub | Módulos 01, 02 e 03 |
| GH-600 | Custom agents, subagents, tools e MCP | Módulo 02 |
| GH-600 | Arquitetura de agentes e integração com o SDLC | Módulo 03 |
| GH-600 | Avaliação, evidências, guardrails e supervisão | Módulos 02 e 03 |

## Decisões de escopo

- O treinamento privilegia demonstrações e atividades práticas, não uma exposição exaustiva de todos os recursos do GitHub Copilot.
- Valores, limites, planos, modelos e recursos em preview devem ser reconfirmados antes de cada turma.
- Segurança é tratada por meio de menor privilégio, revisão e ferramentas especializadas; o Copilot não é apresentado como scanner de segurança.
- GitHub Actions, CODEOWNERS, rulesets e environments aparecem como componentes do fluxo, sem substituir treinamentos específicos dessas plataformas.
- Recursos administrativos ou dependentes de planos organizacionais são apresentados conceitualmente quando não houver ambiente compatível para demonstração.
- O julgamento humano permanece obrigatório para decisões de produto, domínio, arquitetura, segurança e autorização de mudanças de maior risco.

## Referências estruturantes

- [Study guide GH-300: GitHub Copilot](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-300)
- [GitHub Copilot Fundamentals — Parte 1](https://learn.microsoft.com/en-us/training/paths/copilot/)
- [GitHub Copilot Fundamentals — Parte 2](https://learn.microsoft.com/en-us/training/paths/gh-copilot-2/)
- [Study guide GH-600: Developing in Agentic AI Systems](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600)
- [Developing Agentic AI Systems — Parte 1](https://learn.microsoft.com/en-us/training/paths/gh-developing-agentic-systems-1/)
- [Developing Agentic AI Systems — Parte 2](https://learn.microsoft.com/en-us/training/paths/github-agentic-systems-part-two/github-agentic-systems-part-two/)
- [Documentação do GitHub Copilot](https://docs.github.com/en/copilot)
