# Atividade 1: Fundamentos e Características da Qualidade

## Tarefa 1: Fundamentos da qualidade
| Tipo | Necessidade | Interessado | Consequência se não for atendida |
|---|---|---|---|
| Explícita | Pesquisar restaurantes por especialidade | Usuário final | O usuário não consegue encontrar a comida que deseja e abandona o app |
| Explícita | Fazer pedido | Usuário final | O sistema perde seu propósito principal e o restaurante não vende |
| Implícita | Segurança dos dados (senhas criptografadas) | Usuário final / Negócio | Vazamento de dados, perda de confiança e processos legais |
| Implícita | Desempenho (tempo de resposta rápido) | Usuário final | Frustração com a lentidão, levando à desinstalação do app |

**Justificativa sobre qualidade:** Sim, um sistema pode ter todas as funcionalidades explícitas e ainda ter baixa qualidade. Por exemplo, o LocalEats pode permitir fazer pedidos (explícito), mas se demorar 2 minutos para carregar o cardápio (falha na necessidade implícita de desempenho), o usuário considerará o aplicativo ruim.

## Tarefa 2: Exploração da aplicação
| Integrante | Funcionalidade | O que foi realizado | O que foi observado | Evidência |
|---|---|---|---|---|
| Alvaro Cantos Garcia | Fazer pedido | Tentei finalizar um pedido com o carrinho vazio. | O sistema desabilitou o botão de concluir ou exibiu alerta de carrinho vazio. | alvaro-pedido-carrinho-vazio.png |

## Tarefa 3: Requisitos e características de qualidade
| Integrante | Requisito de Qualidade | Característica ou subcaracterística | Justificativa | Como avaliar |
|---|---|---|---|---|
| Alvaro Cantos Garcia | O sistema deve processar a confirmação do pedido em menos de 3 segundos. | Eficiência de Desempenho (Comportamento em relação ao tempo) | A velocidade é crucial em apps de delivery para evitar que o usuário ache que travou e clique duas vezes. | Medir o tempo de resposta do clique no botão 'fazer pedido' até a tela de sucesso. |

## Uso de inteligência artificial
**Ferramenta utilizada:** ChatGPT / Gemini
**Como foi utilizada:** Para geração de ideias de necessidades implícitas e formatação das tabelas.
**Como as respostas foram verificadas:** Revisão manual garantindo que faziam sentido no contexto de um app de delivery de comida.
