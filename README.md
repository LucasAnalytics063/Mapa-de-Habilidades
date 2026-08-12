# Mapa de Habilidades — Inteligência de Carreira com IA
> Mapeie suas competências. Leia o mercado. Monetize com estratégia.

## Visão Geral

A maioria dos profissionais ou subestima seu valor de mercado ou investe no conjunto de habilidades errado. O **Mapa de Habilidades** resolve isso combinando auto avaliação estruturada com análise de mercado orquestrada por um framework de engenharia de prompts projetado para extrair sinal do ruído.

O projeto entrega um pipeline conversacional reutilizável que qualquer LLM (Claude, GPT-4, Gemini) consegue executar para gerar um relatório completo de inteligência profissional: do inventário bruto de competências até os caminhos de monetização priorizados.

## O Problema

Decisões de carreira tomadas sem dados estruturados são caras. Profissionais tipicamente:
- Permanecem em posições abaixo do seu teto de mercado, sem clareza sobre seu valor transferível
- Pivotam para áreas de baixa demanda, desperdiçando meses de capacitação
- Monetizam o conjunto de habilidades errado enquanto ignoram oportunidades adjacentes de alto valor

Este projeto resolve o **problema de clareza** antes que ele se torne um problema de carreira.

## Como Funciona

O motor central é um **prompt com gates sequenciais** o LLM não pode pular etapas nem fabricar dados. Cada fase só avança após o usuário fornecer um input estruturado.

**Fase 1 — Inventário**
Levantamento estruturado de habilidades técnicas, competências comportamentais, experiência profissional e conhecimentos latentes que o usuário possui mas ainda não articulou.

**Fase 2 — Mapeamento de Mercado**
Cruzamento do stack identificado com a demanda atual — identificando quais habilidades estão comoditizadas, quais são escassas e onde de fato está o poder de precificação.

**Fase 3 — Estratégia de Monetização**
Geração de caminhos priorizados: posicionamento freelance, ângulos de consultoria, oportunidades de produtização ou reposicionamento estratégico — com justificativa para cada recomendação.

## Arquitetura do Prompt

O prompt segue um conjunto de restrições aplicadas em nível de design:

|                        Restrição                    |                        Justificativa                       |
|-----------------------------------------------------|------------------------------------------------------------|
| Uma pergunta por etapa (máx. 3 subperguntas)        | Evita sobrecarga cognitiva e melhora a qualidade dos dados |
| Gate sequencial sem pular etapas                    | Garante que a Fase 2 seja fundamentada nos dados da Fase 1 |
| Política anti-alucinação `[PREENCHER]` para lacunas | Mantém a integridade do relatório                          |
| Justificativa obrigatória para cada recomendação    | Constrói confiança do usuário no output gerado             |

## Entregáveis

Uma execução completa produz quatro outputs estruturados:

**Log da Sessão** — Q&A completo organizado por fase, auditável e reutilizável

**Diagnóstico Profissional** — Competências centrais, pontos de alavancagem e lacunas de habilidade com contexto de mercado

**Matriz de Monetização** — Caminhos priorizados com exemplos reais: consultoria, produtização, posicionamento freelance ou reposicionamento interno

**Critérios de Ação** — Próximos passos concretos com critérios de aceitação definidos, não conselhos genéricos

## Casos de Uso

Esta não é uma ferramenta genérica de carreira. Foi construída para momentos específicos de decisão:

- **Transição de carreira** — quantificar valor transferível antes de dar o movimento
- **Negociação de remuneração** — entender posicionamento de mercado antes de uma conversa salarial
- **Arquitetura de renda paralela** — identificar quais habilidades podem gerar receita em paralelo ao emprego principal
- **Priorização de capacitação** — decidir onde investir tempo de aprendizado com base em demanda, não em tendência

## Como Usar

1. Copie o prompt disponível em `/prompt/skill-map.md`
2. Cole na interface do LLM de sua preferência
3. Responda cada pergunta com o máximo de especificidade possível a qualidade do output é diretamente proporcional à profundidade do input
4. Exporte o relatório final para referência

## Licença

MIT — Uso, fork e adaptação livres. Créditos são apreciados.

## Autor
**Lucas Beserra Ribeiro**  
Analista de Business Intelligence | Sicoob Tocantins  
[GitHub: LucasAnalytics063](https://github.com/LucasAnalytics063)
