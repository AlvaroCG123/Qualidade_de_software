# Atividade 3: Estratégia e Projeto de Testes

## Tarefa 1: Planejamento dos testes
**1.1 Objetivo dos testes:** Verificar se o fluxo principal de pedidos funciona corretamente, garantindo que usuários consigam selecionar restaurantes, adicionar itens e finalizar pedidos sem erros.

**1.2 Escopo:**
| Integrante | Funcionalidade incluída | O que será verificado |
|---|---|---|
| Alvaro Cantos Garcia | Fazer pedido | Seleção de itens, cálculo de totais e finalização com sucesso. |
| Funcionalidade não incluída | Justificativa |
| Criar conta | O foco principal deste ciclo de testes é o fluxo de vendas (pedidos). |

**1.3 Abordagem:**
| Item | Decisão da equipe | Justificativa |
|---|---|---|
| Níveis de teste | Teste de Sistema | Avaliar a aplicação inteira integrada (Front e Back). |
| Tipos de teste | Funcional | Validar as regras de negócio do pedido. |
| Perspectiva | Caixa-preta | Testar como usuário final, pela interface. |
| Técnicas de teste | Tabela de decisão e Valor limite | Adequadas para regras de carrinho e totais. |

**1.4 Ambiente e responsabilidades:**
| Item | Definição |
|---|---|
| Ambiente necessário | Navegador Chrome, URL de homologação, usuário teste logado. |
| Responsáveis pelo planejamento | Alvaro Cantos Garcia |
| Responsáveis pela especificação | Alvaro Cantos Garcia |
| Responsáveis pela execução | Alvaro Cantos Garcia |

**1.5 Critérios:**
| Critério | Definição da equipe |
|---|---|
| Entrada | Aplicação no ar e banco de dados populado com 1 restaurante de teste. |
| Saída | 100% dos casos de teste executados. |
| Suspensão | Tela de pedido retornar erro 500 ou banco de dados cair. |

## Tarefa 2: Riscos e técnicas de teste
**2.1 Análise dos riscos**
| ID | Integrante | Funcionalidade | Risco | Consequência | Probabilidade | Impacto | Prioridade | Justificativa |
|---|---|---|---|---|---|---|---|---|
| R01 | Alvaro | Fazer pedido | Usuário finalizar pedido sem itens. | Erro no banco de dados do restaurante. | Baixa | Alto | Média | Regra básica que quebra o fluxo de negócio. |
| R02 | Alvaro | Fazer pedido | Preço total calculado errado. | Prejuízo financeiro. | Média | Alto | Alta | Afeta diretamente a receita do LocalEats. |

**2.2 Aplicação da técnica**
**Nome:** Alvaro Cantos Garcia | **Funcionalidade:** Fazer pedido | **Risco:** R01 | **Técnica:** Tabela de Decisão
**Por que a técnica foi escolhida?** Porque a finalização do pedido depende da combinação de duas condições: estar logado e ter itens no carrinho.
**Aplicação da técnica:**
Regra 1: Logado (Sim) + Carrinho > 0 (Sim) = Pedido Finalizado
Regra 2: Logado (Sim) + Carrinho vazio = Bloquear botão
Regra 3: Deslogado + Carrinho > 0 = Pedir login
**Casos derivados:** CT01, CT02, CT03.

## Tarefa 3: Casos de teste e rastreabilidade
**CT01: Finalizar pedido com sucesso**
Integrante: Alvaro | Func.: Fazer pedido | Risco: R02 | Técnica: Tabela de decisão
*Pré-condição:* Usuário logado, restaurante aberto.
*Passos:* 1. Adicionar 1 item ao carrinho. 2. Clicar em Fazer Pedido. 3. Confirmar dados.
*Resultado esperado:* Tela de sucesso com o resumo do pedido.

**CT02: Impedir pedido com carrinho vazio**
Integrante: Alvaro | Func.: Fazer pedido | Risco: R01 | Técnica: Tabela de decisão
*Pré-condição:* Usuário logado.
*Passos:* 1. Esvaziar carrinho. 2. Ir para tela de checkout.
*Resultado esperado:* Botão de finalizar pedido deve estar desabilitado.

**CT03: Redirecionar para login ao pedir deslogado**
Integrante: Alvaro | Func.: Fazer pedido | Risco: R01 | Técnica: Tabela de decisão
*Pré-condição:* Usuário anônimo.
*Passos:* 1. Adicionar item ao carrinho. 2. Clicar em Fazer Pedido.
*Resultado esperado:* Sistema exibe a tela de login antes do checkout.

**3.2 Matriz de rastreabilidade**
| Integrante | Funcionalidade | Risco ou requisito | Técnica utilizada | Casos de teste |
|---|---|---|---|---|
| Alvaro | Fazer pedido | R01 e R02 | Tabela de Decisão | CT01, CT02 e CT03 |

## Uso de inteligência artificial
**Ferramenta utilizada:** Gemini
**Como foi utilizada:** Para redigir e formatar os casos de teste a partir da tabela de decisão.
**Como as respostas foram verificadas:** Validei se os passos descritos são possíveis na interface atual do Vercel do LocalEats.
