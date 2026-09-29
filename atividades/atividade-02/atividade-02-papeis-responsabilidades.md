# Atividade 2: Organização da Qualidade no LocalEats

## Tarefa 1: Diagnóstico da situação
| Problema identificado | Possível consequência para o produto ou para a equipe |
|---|---|
| Funcionalidades chegam aos usuários com defeitos. | Perda de credibilidade do app e insatisfação dos clientes e restaurantes. |
| Alguns acreditam que somente o QA deve testar. | Sobrecarga no QA, gerando gargalos e atrasando as entregas. |
| Ninguém sabe quem aprova a nova versão. | Versões incompletas podem ir para o ar sem a validação do negócio. |

**A qualidade deve ser responsabilidade exclusiva do QA?** Não. A qualidade deve ser construída desde o levantamento dos requisitos (Analista), passando pelas boas práticas de código e testes unitários (Desenvolvedor), até a validação final (QA). Se só o QA testar, os defeitos são descobertos muito tarde, custando mais caro para corrigir.

## Tarefa 2: Papéis e competências
| Integrante | Papel analisado | Responsabilidades relacionadas à qualidade | Competências técnicas | Competências comportamentais |
|---|---|---|---|---|
| Alvaro Cantos Garcia | Desenvolvedor | Criar testes unitários, seguir padrões de código, revisar código de colegas. | Lógica de programação, frameworks de teste unitário. | Atenção a detalhes, comunicação, trabalho em equipe. |

## Tarefa 3: Matriz de responsabilidades (RACI)
| Atividade de qualidade | Analista de Negócio | Desenvolvedor | QA | Liderança Técnica |
|---|---|---|---|---|
| Definir critérios de aceitação | R, A | C | C | I |
| Implementar a funcionalidade | I | R, A | I | C |
| Criar testes unitários | I | R | C | A |
| Planejar e executar testes do sistema | C | I | R, A | I |
| Registrar e acompanhar defeitos | I | C | R | A |
| Aprovar a disponibilização da versão | A | I | C | R |

**Lacuna ou conflito encontrado:** 'Aprovar a disponibilização da versão' corria o risco de não ter um aprovador (A) claro focado no negócio. Foi definido que o Analista de Negócio assume o papel de aprovação final.

**Práticas recomendadas:**
| Prática recomendada | Problema que ajuda a resolver | Papéis envolvidos |
|---|---|---|
| Code Review (Revisão de Código) | Reduz defeitos antes de chegar ao QA. | Desenvolvedor, Liderança Técnica |
| Definição de 'Ready' e 'Done' (DoR/DoD) | Esclarece os critérios para considerar uma funcionalidade pronta. | Todos (Analista, Dev, QA) |

## Uso de inteligência artificial
**Ferramenta utilizada:** Gemini
**Como foi utilizada:** Auxílio na montagem da Matriz RACI.
**Como as respostas foram verificadas:** Conferência das letras R, A, C, I para garantir que cada linha tivesse pelo menos um Responsável e apenas um Aprovador.
