# Ementa — GitHub Copilot para Engenharia de Software Moderna

## Propósito e critérios de cobertura

Este curso apresenta o GitHub Copilot como colaborador no ciclo de vida de software, sempre sob supervisão humana. A ementa usa os guias [GH-300](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-300) e [GH-600](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600) como referências de cobertura e profundidade, mas não prepara para exames.

Cada aula tem 240 minutos. Os tópicos marcados como:

- **prática** devem aparecer em demonstração, walkthrough ou lab;
- **aplicação** devem orientar decisões e ser retomados nas atividades;
- **panorama** dão repertório para reconhecer o recurso, seus limites e quando aprofundá-lo.

As referências foram consultadas em **15 de agosto de 2026**. Nomes, disponibilidade, planos, modelos, limites e cobrança devem ser reconfirmados antes da publicação dos materiais.

## Módulo 1 — Do requisito à aplicação: desenvolvimento assistido pelo Copilot

### Resultado de aprendizagem

Ao final da aula, o aluno deverá reconhecer como o Copilot participa de um fluxo de desenvolvimento completo, escolher entre suas principais formas de interação no VS Code e transformar requisitos em incrementos verificáveis, mantendo responsabilidade sobre contexto, decisões, código e validação.

### Estratégia

Um walkthrough longo apresenta a construção de uma aplicação de treinamentos em .NET 10: solução, API CRUD, persistência, UI Blazor WebAssembly, testes, documentação e CI/CD. O instrutor especifica e constrói em profundidade uma única fatia vertical — requisito, endpoint, persistência, interface e teste —, extrai um prompt file para repetir o método nos demais endpoints e usa checkpoints recuperáveis para preservar continuidade e acelerar etapas mecânicas.

O objetivo é tornar visível o ciclo completo e as decisões de engenharia, não ensinar profundamente todas as tecnologias nem digitar cada variação do CRUD. Os alunos podem acompanhar no próprio Codespace ou apenas observar. A aula reserva 30 minutos para uma prática individual delimitada; os módulos seguintes devem compensar essa exceção para que o curso totalize pelo menos quatro horas de prática.

Na atividade individual, o aluno adiciona um agregado independente de alunos, sem inscrições ou relação com treinamentos: `POST` e `GET /api/students`, persistência de nome e e-mail, formulário, listagem e pelo menos um teste. O objetivo é reutilizar o método observado em uma nova fatia, não ampliar o domínio.

O Módulo 1 também funciona como uma visão espiral do curso: recursos que serão aprofundados depois aparecem brevemente quando resolvem uma necessidade real do walkthrough. A apresentação deve mostrar seu propósito e seus limites, sem transformar essa primeira aula em treinamento completo de cada mecanismo.

### Conteúdo

| Nível | Tópico | Conteúdo e limites | Fundamentação |
| --- | --- | --- | --- |
| prática | Intenção, especificação e escolha da interação | Converter a necessidade em uma especificação versionada com escopo, contrato, critérios de aceitação e evidências; usar o Copilot para apontar lacunas sem delegar decisões; decidir entre sugestões e chat inline e os agentes Ask, Plan e Agent. Engenharia de prompts e governança serão aprofundadas depois. | [Responsible AI with GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/responsible-ai-with-github-copilot/), [chat e agentes no VS Code](https://docs.github.com/en/copilot/how-tos/chat-with-copilot/chat-in-ide), [Spec-Driven Development](https://developer.microsoft.com/blog/spec-driven-development-ai-native-engineering/) |
| prática | Base da solução e API da fatia vertical | Criar repositório, solução e projetos; implementar e revisar o primeiro endpoint, incluindo DTO, validação e tratamento de erro; extrair o método validado para um prompt file parametrizado e reutilizá-lo nos demais endpoints. Invocações preparadas e checkpoint podem acelerar a execução sem omitir contratos e validações. | [APIs Web com ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/web-api/), [tratamento de erros em APIs](https://learn.microsoft.com/en-us/aspnet/core/web-api/handle-errors), [prompt files no VS Code](https://code.visualstudio.com/docs/agent-customization/prompt-files) |
| prática | Persistência da fatia vertical | Modelar a entidade, configurar Entity Framework Core, criar a primeira migration e persistir o fluxo escolhido; revisar o resultado antes de avançar. Configuração repetitiva e dados iniciais podem vir do checkpoint. | [Entity Framework Core](https://learn.microsoft.com/en-us/ef/core/), [migrations](https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/) |
| prática | Interface da fatia vertical | Integrar uma tela Blazor WebAssembly à API e tratar carregamento, sucesso e erro no fluxo escolhido. Formulários e operações CRUD restantes são apresentados no checkpoint seguinte. | [Blazor](https://learn.microsoft.com/en-us/aspnet/core/blazor/), [chamar uma API Web no Blazor](https://learn.microsoft.com/en-us/aspnet/core/blazor/call-web-api) |
| prática | Validação e fechamento da jornada | Criar um teste relevante para a fatia vertical, inspecionar o OpenAPI e executar um workflow básico de CI. Testes, documentação e CI/CD entram como partes do incremento; sua estratégia será aprofundada no Módulo 4. | [Testes com GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-using-github-copilot-tools/), [OpenAPI no ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/openapi/overview), [GitHub Actions para .NET](https://docs.github.com/en/actions/how-tos/use-cases-and-examples/building-and-testing/building-and-testing-net) |
| panorama | Natureza multilinguagem | Comparar brevemente como o mesmo requisito se expressa em C#, TypeScript, Python, Java, PHP, Go e SQL; destacar que qualidade depende do contexto e da validação, não apenas da linguagem. | [Sugestões de código](https://docs.github.com/en/copilot/concepts/completions/code-suggestions), [introdução ao GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/introduction-to-github-copilot/) |
| panorama | Contexto e customização em ação | Mostrar transversalmente, sem aprofundar, zero-shot, few-shot, prompt file, instructions, escolha de agente, criação de um agent skill e de um custom agent; apresentar conceitualmente content exclusion; comparar a reutilização de uma conversa com o início de um novo chat. | [Zero-shot e few-shot](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/zero-shot-learning), [cheat sheet de customização](https://docs.github.com/en/copilot/reference/customization-cheat-sheet), [content exclusion](https://docs.github.com/en/copilot/concepts/context/content-exclusion) |

Responsabilidade, legibilidade, reutilização, segurança, consumo e validação são critérios transversais observados durante cada etapa, não blocos expositivos independentes.

### Progressão espiral

| Primeiro contato no Módulo 1 | Aprofundamento |
| --- | --- |
| Zero-shot, few-shot, prompt files, seleção de contexto e ciclo de uma conversa | Módulo 2 |
| Repository instructions, escopo das instruções e content exclusion | Módulo 2 |
| Escolha entre agentes, criação de agent skill e custom agent | Módulo 3 |
| Testes, revisão, documentação, CI e evidências de qualidade | Módulo 4 |

Content exclusion deve ser apresentado conceitualmente no Módulo 1, sem demonstração: depende de configuração administrativa e de plano compatível e não é atualmente compatível com Agent mode no VS Code. O tema será aprofundado conceitualmente no Módulo 2 e não dependerá de um ambiente administrado para acompanhar a aula.

### Uso dos checkpoints

| Etapa demonstrada | O que o checkpoint pode fornecer |
| --- | --- |
| Criação da solução | Dependências restauradas e configuração estável |
| Primeiro fluxo da API e prompt file | Invocações preparadas e estado funcional com os demais endpoints |
| Primeira persistência | Banco configurado e dados iniciais |
| Primeira tela integrada | Formulários e operações restantes |
| Primeiro teste e execução da CI | Suíte mínima, OpenAPI, README e workflow funcionais |

O checkpoint deve eliminar repetição e espera, mas preservar a explicação das decisões, dos critérios e das evidências de validação.

### Distribuição de tempo

| Período | Atividade |
| --- | --- |
| 0–8 min | Objetivos, dinâmica e preparação |
| 8–24 min | Cenário, tipos de prompt e especificação da fatia vertical |
| 24–28 min | Repository instructions e contexto durável |
| 28–44 min | Escolha da interação, arquitetura da fatia e base da solução |
| 44–54 min | Implementação e validação do primeiro endpoint |
| 54–59 min | Intervalo |
| 59–77 min | Criação e reuso do prompt file nos demais endpoints |
| 77–88 min | Validação, checkpoint e comparação |
| 88–109 min | Persistência e migration |
| 109–119 min | Intervalo |
| 119–138 min | Blazor integrado à API |
| 138–156 min | Teste, OpenAPI e CI como fechamento da jornada |
| 156–165 min | Síntese, dúvidas e preparação da prática |
| 165–195 min | Exercício individual: cadastro e listagem de alunos |
| 195–200 min | Intervalo |
| 200–218 min | Resolução do exercício |
| 218–236 min | Questionário e correção comentada |
| 236–240 min | Síntese e conexão com o Módulo 2 |

## Módulo 2 — Contexto, prompts, personalização, privacidade e uso consciente

### Resultado de aprendizagem

Ao final da aula, o aluno deverá construir prompts e contexto adequados à tarefa, selecionar modelo e modo conscientemente, criar personalizações reutilizáveis e explicar como dados, políticas, exclusões e consumo afetam o uso do Copilot.

### Conteúdo

| Nível | Tópico | Conteúdo e limites | Fundamentação |
| --- | --- | --- | --- |
| aplicação | Como o Copilot processa uma solicitação | Context window, composição do prompt, histórico, arquivos e seleção de código; ciclo da sugestão, hospedagem de modelos, filtros e pós-processamento. Evitar representar a arquitetura como acesso irrestrito ao repositório. | [Conceitos de prompting](https://docs.github.com/en/copilot/concepts/prompting), [hospedagem de modelos](https://docs.github.com/en/copilot/reference/ai-models/model-hosting), [indexação de repositório](https://docs.github.com/en/copilot/concepts/context/repository-indexing) |
| prática | Anatomia de prompts eficazes | Explicitar contexto, tarefa, restrições, critérios de aceitação e formato de saída; usar zero-shot, few-shot, exemplos e contraexemplos; decompor tarefas e validar respostas. | [Engenharia de prompts para o Copilot](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [introdução à engenharia de prompts](https://learn.microsoft.com/en-us/training/modules/introduction-prompt-engineering-with-github-copilot/) |
| prática | Prompt chaining e refinamento | Separar descoberta, plano, implementação, revisão e validação; preservar decisões úteis e iniciar uma nova conversa quando o histórico introduzir ruído ou conflito. | [Engenharia de prompts para o Copilot](https://docs.github.com/en/copilot/concepts/prompting/prompt-engineering), [gerenciamento de contexto no Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/context-management) |
| prática | Seleção e redução de contexto | Referenciar arquivos e símbolos relevantes, evitar anexos desnecessários, usar indexação e Spaces quando apropriado e reconhecer contexto obsoleto. | [Contexto no GitHub Copilot](https://docs.github.com/en/copilot/concepts/context), [Copilot Spaces](https://docs.github.com/en/copilot/concepts/context/spaces), [indexação de repositório](https://docs.github.com/en/copilot/concepts/context/repository-indexing) |
| prática | Personalização reutilizável | Criar instruções de repositório e por caminho, prompt files e padrões de revisão; decidir entre instrução persistente, prompt reutilizável, skill, hook, agente customizado e MCP. | [Personalização de respostas](https://docs.github.com/en/copilot/concepts/prompting/response-customization), [cheat sheet de personalização](https://docs.github.com/en/copilot/reference/customization-cheat-sheet), [suporte a custom instructions](https://docs.github.com/en/copilot/reference/custom-instructions-support) |
| prática | Modelos, modos e consumo | Relacionar complexidade, latência, contexto e custo; consultar modelos disponíveis e uso; reduzir iterações desperdiçadas. Não fixar valores ou recomendar sempre o modelo mais caro. | [Modelos e preços](https://docs.github.com/en/copilot/reference/copilot-billing/models-and-pricing), [limites de uso](https://docs.github.com/en/copilot/concepts/usage-limits), [monitoramento de AI Credits](https://docs.github.com/en/copilot/how-tos/manage-and-track-spending/monitor-ai-usage) |
| aplicação | Privacidade, retenção e propriedade | Distinguir planos e configurações; explicar tratamento de dados, retenção, propriedade e limitações das saídas sem prometer confidencialidade além da política vigente. | [Planos do Copilot](https://docs.github.com/en/copilot/get-started/plans), [hospedagem de modelos](https://docs.github.com/en/copilot/reference/ai-models/model-hosting), [GitHub Trust Center](https://github.com/trust-center) |
| explicação | Exclusão de conteúdo e código público | Explicar como administradores configuram exclusões e analisar suas limitações sem exigir demonstração em ambiente Enterprise; configurar o filtro de sugestões semelhantes a código público e investigar por que uma sugestão ou referência não apareceu. | [Content exclusion](https://docs.github.com/en/copilot/concepts/context/content-exclusion), [code referencing](https://docs.github.com/en/copilot/concepts/completions/code-referencing) |
| panorama | Superfícies usadas no treinamento | Configurar o Copilot no VS Code e reconhecer a continuidade do trabalho no GitHub Copilot CLI e no GitHub Copilot App. Outras IDEs não fazem parte do treinamento. | [Instalar a extensão do Copilot](https://docs.github.com/en/copilot/how-tos/set-up/install-copilot-extension), [Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-copilot-cli), [GitHub Copilot App](https://docs.github.com/en/copilot/concepts/agents/github-copilot-app) |
| panorama | Administração e governança organizacional | Políticas de recursos e Copilot Code Review, auditoria, acesso, subscriptions/seats e REST API; responsabilidades distintas de desenvolvedor, liderança e administrador. | [Gerenciar políticas na organização](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-for-organization/manage-policies), [REST API de gerenciamento do Copilot](https://docs.github.com/en/rest/copilot/copilot-user-management), [gestão e personalização](https://learn.microsoft.com/en-us/training/modules/github-copilot-management-and-customizations/) |

## Módulo 3 — Copilot e agentes no ciclo de vida das aplicações

### Resultado de aprendizagem

Ao final da aula, o aluno deverá escolher e supervisionar uma experiência agêntica, definir seus limites de planejamento e execução, configurar contexto, ferramentas e permissões e manter estado e evidências suficientes para retomar, revisar ou interromper o trabalho.

### Conteúdo

| Nível | Tópico | Conteúdo e limites | Fundamentação |
| --- | --- | --- | --- |
| prática | Requisitos, design e arquitetura assistidos | Produzir histórias, critérios, fluxos, diagramas, ADRs e planos; verificar pressupostos e manter rastreabilidade entre intenção, implementação e testes. | [Escolher a ferramenta de IA adequada](https://docs.github.com/en/copilot/concepts/tools/ai-tools), [Spec-Driven Development](https://developer.microsoft.com/blog/spec-driven-development-ai-native-engineering/), [GitHub Spec Kit](https://github.com/github/spec-kit) |
| aplicação | Arquitetura de agentes no SDLC | Identificar etapas adequadas para agentes, entradas, saídas, critérios de sucesso e antipadrões; tratar o agente como contribuidor sujeito aos mesmos controles do repositório. | [Foundations of Agentic AI in GitHub](https://learn.microsoft.com/en-us/training/modules/foundations-agentic-ai/), [Designing Agent Architecture and SDLC Integration](https://learn.microsoft.com/en-us/training/modules/design-agent-architecture-integration/) |
| prática | Fronteiras entre planejamento, raciocínio e ação | Solicitar plano estruturado, revisar riscos e dependências, impedir execução prematura e aprovar apenas o próximo incremento verificável. Não exigir exposição de raciocínio interno; exigir artefatos e justificativas inspecionáveis. | [Guia GH-600: arquitetura e SDLC](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600#prepare-agent-architecture-and-sdlc-processes), [riscos e mitigações do cloud agent](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations) |
| prática | Experiências agênticas e delegação | Comparar alterações locais, Plan e Agent no VS Code com cloud agent, GitHub Copilot App e subagentes; gerenciar sessões e delegar tarefas delimitadas para preservar contexto; selecionar execução local ou remota, síncrona ou assíncrona, conforme risco e feedback necessário. | [Recursos do Copilot](https://docs.github.com/en/copilot/get-started/features), [GitHub Copilot App](https://docs.github.com/en/copilot/concepts/agents/github-copilot-app), [cloud agent](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/about-cloud-agent), [custom agents e subagentes](https://docs.github.com/en/copilot/how-tos/copilot-sdk/features/custom-agents) |
| prática | GitHub Copilot CLI | Instalar e autenticar; usar sessões interativas e prompts não interativos; inspecionar permissões; gerar, explicar e revisar comandos, scripts e alterações de arquivos antes da execução. | [Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-copilot-cli), [começar a usar o Copilot CLI](https://docs.github.com/en/copilot/how-tos/copilot-cli/cli-getting-started), [sandbox local](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/understanding-local-sandboxing) |
| prática | Ferramentas e permissões | Selecionar somente ferramentas necessárias, limitar escopo e permissões, revisar chamadas e diferenciar leitura, edição, execução e operações externas. | [Tooling, MCP, and Agent Execution Environments](https://learn.microsoft.com/en-us/training/modules/agent-tooling-mcp-execution-environments/), [riscos e mitigações do cloud agent](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations) |
| prática | Model Context Protocol | Entender cliente, servidor, tools, resources e prompts; conectar o GitHub MCP Server; avaliar confiança, autenticação, dados expostos e risco de ferramentas de terceiros. | [MCP e GitHub Copilot](https://docs.github.com/en/copilot/concepts/context/mcp), [aprimorar o modo agente com MCP](https://docs.github.com/en/copilot/tutorials/enhance-agent-mode-with-mcp), [GitHub MCP Server](https://github.com/github/github-mcp-server) |
| panorama | Registries e allow lists de MCP | Reconhecer controles organizacionais para descoberta e restrição de servidores; não transformar a aula em administração completa de enterprise. | [Gerenciar uso de MCP](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-mcp-usage), [configurar MCP registry](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-mcp-usage/configure-mcp-registry), [restringir por registry](https://docs.github.com/en/copilot/how-tos/administer-copilot/manage-mcp-usage/restrict-based-on-registry) |
| prática | Ambiente e caminho de execução | Delimitar repositório e branch, preparar dependências, integrar a CI, controlar acesso à rede e permitir criação de branch e PR sem acesso irrestrito. | [Customizar o ambiente do cloud agent](https://docs.github.com/en/copilot/customizing-copilot/customizing-the-development-environment-for-copilot-coding-agent), [customizar o firewall](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-the-firewall), [Designing Agent Architecture and SDLC Integration](https://learn.microsoft.com/en-us/training/modules/design-agent-architecture-integration/) |
| prática | Erros, retries, rollback e escalonamento | Detectar falha, interromper com segurança, evitar repetição destrutiva, preservar diagnóstico, reverter mudanças e pedir intervenção humana quando os limites forem atingidos. | [Tooling, MCP, and Agent Execution Environments](https://learn.microsoft.com/en-us/training/modules/agent-tooling-mcp-execution-environments/), [cancelar e reverter no Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/cancel-and-roll-back) |
| aplicação | Memória, estado e context drift | Distinguir memória de curto e longo prazo e estado externo; definir escopo, expiração e reset; registrar progresso e decisões em artefatos duráveis; manter continuidade entre VS Code, CLI, GitHub Copilot App e cloud agent sem propagar contexto obsoleto ou conflitante. | [Memory, State, and Evaluation](https://learn.microsoft.com/en-us/training/modules/memory-state-evaluation/), [Copilot Memory](https://docs.github.com/en/copilot/concepts/agents/copilot-memory) |
| panorama | Custom agents, skills e hooks | Reconhecer quando encapsular persona, ferramentas, conhecimento ou controles de execução; avaliar portabilidade, manutenção e risco antes de criar novas customizações. | [Custom agents](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/about-custom-agents), [agent skills](https://docs.github.com/en/copilot/concepts/agents/about-agent-skills), [hooks](https://docs.github.com/en/copilot/concepts/agents/hooks) |

## Módulo 4 — Qualidade, avaliação, documentação e operação responsável

### Resultado de aprendizagem

Ao final da aula, o aluno deverá usar o Copilot para ampliar a qualidade e a capacidade de validação sem terceirizar julgamento, avaliar falhas de agentes com evidências, operar coordenação multiagente com isolamento e aplicar guardrails proporcionais ao risco.

### Conteúdo

| Nível | Tópico | Conteúdo e limites | Fundamentação |
| --- | --- | --- | --- |
| prática | Estratégia de testes e edge cases | Derivar cenários dos critérios de aceitação, criar testes unitários e de integração, mocks e dados de teste; revisar assertions, isolamento, determinismo e cobertura útil. | [Testes com GitHub Copilot](https://learn.microsoft.com/en-us/training/modules/develop-unit-tests-using-github-copilot-tools/), [testes no .NET](https://learn.microsoft.com/en-us/dotnet/core/testing/) |
| prática | Refatoração e modernização orientadas por evidências | Identificar duplicação, acoplamento, legibilidade, manutenção e gargalos; modernizar código legado em incrementos; preservar comportamento com testes e medir desempenho antes de aceitar otimizações. | [Casos de uso do Copilot para desenvolvedores](https://learn.microsoft.com/en-us/training/modules/developer-use-cases-for-ai-with-github-copilot/), [boas práticas do Copilot](https://docs.github.com/en/copilot/get-started/best-practices) |
| aplicação | Segurança apoiada por ferramentas especializadas | Usar o Copilot para levantar hipóteses e explicar achados, mas combinar revisão humana, análise de código, dependências e segredos; não apresentar o Copilot como scanner de segurança. | [Segurança no GitHub](https://docs.github.com/en/code-security/getting-started/github-security-features), [Autofix para code scanning](https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/about-autofix-for-codeql-code-scanning) |
| aplicação | Documentação viva | Produzir README orientado a tarefas, comentários úteis, decisões arquiteturais e OpenAPI; verificar exemplos e manter documentação próxima do código e do pipeline. | [OpenAPI no ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/openapi/overview), [sobre READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) |
| prática | Pull requests e revisão de código | Gerar resumo de mudanças, solicitar code review do Copilot, avaliar comentários, personalizar padrões e manter revisão humana para lógica, arquitetura, segurança e domínio. | [Copilot code review](https://docs.github.com/en/copilot/concepts/agents/code-review), [usar code review no GitHub](https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/copilot-code-review), [ciclo de vida de PR](https://docs.github.com/en/copilot/tutorials/use-copilot-code-review-across-the-pull-request-lifecycle) |
| aplicação | Critérios e sinais de avaliação de agentes | Definir resultados, restrições e sinais qualitativos e quantitativos; usar testes, linters, scanners, logs, planos, traces e artefatos como evidência. | [Memory, State, and Evaluation](https://learn.microsoft.com/en-us/training/modules/memory-state-evaluation/), [guia GH-600: avaliação e tuning](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600#perform-evaluation-error-analysis-and-tuning) |
| aplicação | Análise de falhas e tuning | Classificar causa raiz como problema de instrução, raciocínio, contexto, ferramenta ou ambiente; ajustar instruções, workflow, memória, acesso e critérios e executar nova avaliação controlada. | [Memory, State, and Evaluation](https://learn.microsoft.com/en-us/training/modules/memory-state-evaluation/), [implementation planner](https://docs.github.com/en/copilot/tutorials/customization-library/custom-agents/implementation-planner) |
| aplicação | Orquestração multiagente | Escolher padrão de coordenação, decompor responsabilidades, isolar execução paralela e tratar sobreposição de código, trabalho duplicado e resultados contraditórios. Usar múltiplos agentes apenas quando a decomposição trouxer benefício verificável. | [Multi-Agent Systems and Orchestration](https://learn.microsoft.com/en-us/training/modules/multi-agent-systems-orchestration/), [custom agents e subagentes](https://docs.github.com/en/copilot/how-tos/copilot-sdk/features/custom-agents) |
| aplicação | Observabilidade, recuperação e ciclo de vida | Produzir logs, artefatos, decisões e handoffs auditáveis; detectar execuções travadas, parciais ou degradadas; aplicar rollback e human-in-the-loop; atualizar ou retirar agentes sem perder continuidade. | [Multi-Agent Systems and Orchestration](https://learn.microsoft.com/en-us/training/modules/multi-agent-systems-orchestration/), [Governance, Guardrails, and Operations](https://learn.microsoft.com/en-us/training/modules/governance-guardrails-operations/) |
| aplicação | Autonomia, guardrails e accountability | Classificar ações por risco, aplicar least privilege, exigir aprovação para ações irreversíveis ou sensíveis e evitar aprovações de baixo valor; usar rulesets, CODEOWNERS, checks e environments como controles. | [Construir guardrails para o cloud agent](https://docs.github.com/en/copilot/tutorials/cloud-agent/build-guardrails), [riscos e mitigações](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/risks-and-mitigations), [Governance, Guardrails, and Operations](https://learn.microsoft.com/en-us/training/modules/governance-guardrails-operations/) |
| prática | CI/CD e operação do pipeline | Criar, revisar e documentar GitHub Actions para build, testes e publicação; usar permissões mínimas, ambientes protegidos, artefatos e diagnóstico de falhas. | [GitHub Actions](https://docs.github.com/en/actions), [segurança no GitHub Actions](https://docs.github.com/en/actions/security-for-github-actions/security-guides/security-hardening-for-github-actions), [deploy de .NET](https://learn.microsoft.com/en-us/dotnet/core/deploying/) |
| panorama | Workflows agênticos, automações e recursos em transição | Reconhecer automações baseadas em eventos ou agenda, seus riscos operacionais e o ciclo de vida dos recursos. Agentic Workflows e outros recursos em preview não devem ser dependência única de labs essenciais. O Spark deixa de aceitar novos usuários e novos aplicativos a partir de 4 de agosto de 2026 e entra apenas como exemplo de mudança de produto. | [GitHub Agentic Workflows](https://docs.github.com/en/copilot/concepts/agents/about-github-agentic-workflows), [automações do cloud agent](https://docs.github.com/en/copilot/concepts/agents/cloud-agent/about-automations), [GitHub Spark](https://docs.github.com/en/copilot/concepts/spark) |

## Cobertura dos guias de referência

| Guia | Domínio | Cobertura principal |
| --- | --- | --- |
| GH-300 | Uso responsável do GitHub Copilot | Módulos 1 e 2 |
| GH-300 | Recursos do GitHub Copilot no VS Code, CLI, GitHub.com, GitHub Copilot App e agentes | Módulos 1, 2 e 3 |
| GH-300 | Dados e arquitetura do Copilot | Módulo 2 |
| GH-300 | Engenharia de prompts e construção de contexto | Módulo 2 |
| GH-300 | Produtividade, qualidade, testes, segurança e performance | Módulos 1 e 4 |
| GH-300 | Privacidade, exclusões e salvaguardas | Módulo 2 |
| GH-600 | Arquitetura de agentes e processos do SDLC | Módulo 3 |
| GH-600 | Ferramentas e interação com o ambiente | Módulo 3 |
| GH-600 | Memória, estado e execução | Módulo 3 |
| GH-600 | Avaliação, análise de erros e tuning | Módulo 4 |
| GH-600 | Coordenação multiagente | Módulo 4 |
| GH-600 | Guardrails e accountability | Módulo 4 |

## Decisões de escopo

- **GitHub Spark:** não integra o núcleo prático. Embora apareça no guia GH-300 vigente, deixou de aceitar novos usuários e a criação de novos aplicativos em 4 de agosto de 2026; não deve sustentar objetivos ou labs essenciais. Consultar a [documentação vigente do Spark](https://docs.github.com/en/copilot/concepts/spark) antes de qualquer menção.
- **Administração corporativa:** políticas, auditoria, subscriptions e MCP registries entram como panorama para apoiar decisões de desenvolvedores e lideranças; não constituem um curso de administração do GitHub Enterprise.
- **MCP:** cobre uso seguro pelo Copilot e governança essencial, não desenvolvimento completo de servidores nem toda a especificação do protocolo.
- **Microsoft Agent Framework:** pode ilustrar integração avançada, mas não faz parte do núcleo das quatro aulas. Quando usado, tratar a integração como opcional e verificar seu status na [documentação oficial](https://docs.github.com/en/copilot/how-tos/copilot-sdk/integrations/microsoft-agent-framework).
- **Segurança:** CodeQL, secret scanning, Dependabot e supply chain security aparecem como fontes de sinais e controles; seu uso completo pertence a um treinamento específico de segurança.
- **GitHub Actions:** o curso cobre o necessário para CI/CD da aplicação e controle de agentes, sem substituir um treinamento dedicado à plataforma.
- **Recursos em preview:** Copilot Memory, Agentic Workflows e outros recursos marcados como preview podem aparecer em demonstrações com alternativa estável, nunca como único caminho para concluir um lab.

## Referências estruturantes

- [Study guide GH-300: GitHub Copilot](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-300)
- [GitHub Copilot Fundamentals — Parte 1](https://learn.microsoft.com/en-us/training/paths/copilot/)
- [GitHub Copilot Fundamentals — Parte 2](https://learn.microsoft.com/en-us/training/paths/gh-copilot-2/)
- [Study guide GH-600: Developing in Agentic AI Systems](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-600)
- [Developing Agentic AI Systems — Parte 1](https://learn.microsoft.com/en-us/training/paths/gh-developing-agentic-systems-1/)
- [Developing Agentic AI Systems — Parte 2](https://learn.microsoft.com/en-us/training/paths/github-agentic-systems-part-two/github-agentic-systems-part-two/)
- [GitHub Copilot documentation](https://docs.github.com/en/copilot)
