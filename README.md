# Azure Functions e Logic Apps - Documentação de Aprendizados

## Visão Geral
Este documento resume os principais conceitos aprendidos sobre Azure Functions e Logic Apps, dois serviços essenciais para computação serverless e automação de workflows no Azure.

## Parte 1: Azure Functions

### Introdução ao Azure Functions
- **Definição**: Serviço de computação serverless para execução de pequenos trechos de código (funções)
- **Principais características**:
  - Execução baseada em eventos
  - Escala automática
  - Modelo pay-per-use
  - Suporte a múltiplas linguagens (C#, JavaScript, Python, etc.)

### Modelos de Hospedagem
| Plano | Descrição | Melhor para | Escala | Custo |
|-------|-----------|-------------|--------|-------|
| Consumo | Cobrado por execução | Cargas variáveis | Automática | Pay-per-use |
| Premium | Recursos pré-alocados | Aplicações críticas | Automática | Fixo + execuções |
| Dedicado (App Service) | VM dedicada | Cargas previsíveis | Manual | Fixo |

### Gatilhos e Bindings
- **Gatilhos comuns**:
  - HTTP
  - Timer
  - Blob Storage
  - Service Bus
  - Cosmos DB
- **Bindings**: Conexões declarativas com outros serviços Azure

### Padrões de Escalabilidade
- **Escala horizontal automática** baseada em carga
- **Concorrência** controlável (configurações de lote)
- **Duração máxima de execução** variável por plano

## Parte 2: Desenvolvimento com Azure Functions

### Fluxo de Desenvolvimento
1. Criar projeto Function App
2. Definir função com gatilho específico
3. Configurar bindings de entrada/saída
4. Implementar lógica de negócio
5. Testar localmente (Azure Functions Core Tools)
6. Publicar no Azure

### Melhores Práticas
- **Funções stateless** sempre que possível
- **Tarefas curtas** (max. 10 min no plano Consumo)
- **Tratamento robusto** de erros
- **Logging** adequado
- **Variáveis de ambiente** para configurações

### Monitoramento
- **Application Insights** integrado
- **Métricas** de execução/disponibilidade
- **Log streaming** em tempo real
- **Alertas** configuráveis

## Parte 3: Azure Logic Apps

### Conceitos Fundamentais
- **Serviço de integração** e automação de workflows
- **Modelo baseado em conectores** (500+ disponíveis)
- **Designer visual** para construção de fluxos
- **Execução serverless**

### Componentes Principais
- **Gatilhos**: Iniciam o workflow (ex: quando um email chega)
- **Ações**: Passos executados (ex: salvar anexo no OneDrive)
- **Conectores**: Integrações com serviços externos
- **Condições e loops**: Lógica de controle

### Casos de Uso Típicos
- **Integração entre sistemas**
- **Automação de processos** empresariais
- **Orquestração de microsserviços**
- **Processamento de arquivos**
- **Notificações e alertas**

### Comparativo: Functions vs Logic Apps
| Critério | Azure Functions | Logic Apps |
|----------|----------------|------------|
| Paradigma | Código (imperativo) | Design visual (declarativo) |
| Complexidade | Alta flexibilidade | Mais simples para integrações |
| Custos | Por execução/resource | Por ação executada |
| Debugging | Ferramentas de desenvolvimento | Logs e rastreamento |
| Melhor para | Lógica complexa | Fluxos de integração |

## Conclusão
- **Azure Functions**: Ideal para processamento customizado e microsserviços
- **Logic Apps**: Melhor para workflows de integração e automação
- **Uso combinado**: Solução poderosa para arquiteturas serverless
