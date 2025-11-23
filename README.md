# Trabalho-Final-Proposta-de-Experimento-para-TCC

## 1. Identificação Básica

 Título do experimento:
**Código com Comentários vs. Código Auto-explicativo: Impacto na Manutenibilidade e Compreensão por Desenvolvedores**

 Autores
 [Renato Cazzoletti] - Engenharia de Software - [renato.cazzoletti7@gmail.com]

 Projeto / produto / iniciativa relacionada
Trabalho de Conclusão de Curso (TCC) - Análise de práticas de documentação e legibilidade de código em engenharia de software

---

# Plano de Experimento – Código Comentado vs Auto-explicativo

## 1. Template do Escopo (Goal Template - GQM)

**Analisar** diferentes estratégias de documentação de código (código com comentários abundantes, código auto-explicativo com nomes descritivos, e código mal documentado)

**com o propósito de** avaliar e comparar seu impacto na manutenibilidade de software

**com respeito a** tempo de compreensão do código, eficiência na implementação de modificações, taxa de erros introduzidos, carga cognitiva percebida e satisfação do desenvolvedor

**do ponto de vista de** desenvolvedores de software com experiência prática em programação

**no contexto de** tarefas típicas de manutenção de software (compreensão de funcionalidade, modificação evolutiva e correção de bugs) em sistemas orientados a objetos escritos em Python.

---

## 2. Objetivos Específicos

**O1 - Compreensão de Código:** Avaliar o impacto das diferentes estratégias de documentação (comentários vs. nomes descritivos vs. código mal documentado) no tempo necessário para desenvolvedores compreenderem a funcionalidade do código-fonte e na precisão dessa compreensão.

**O2 - Eficiência em Modificações:** Determinar qual estratégia de documentação resulta em modificações de código mais rápidas, eficientes e de maior qualidade estrutural durante tarefas de manutenção evolutiva e corretiva.

**O3 - Carga Cognitiva e Experiência do Desenvolvedor:** Identificar a influência das diferentes estratégias de documentação na carga cognitiva percebida, no nível de confiança dos desenvolvedores em suas modificações e no nível de frustração experimentado durante as tarefas.

**O4 - Qualidade e Correção das Modificações:** Comparar a taxa de erros (lógicos, de sintaxe e regressões funcionais) introduzidos durante modificações de código sob as três diferentes estratégias de documentação.

---

## 3. Tabela GQM - Goal/Question/Metric

| **Objetivo** | **Pergunta de Pesquisa** | **Métricas Associadas** |
|--------------|--------------------------|-------------------------|
| **O1: Compreensão de Código**<br><br>Avaliar impacto no tempo e precisão da compreensão | **Q1.1:** Qual estratégia de documentação permite aos desenvolvedores identificar mais rapidamente a funcionalidade principal do código? | **M1:** Tempo de primeira compreensão (minutos)<br>**M2:** Taxa de acerto na identificação de funcionalidade (%) |
| | **Q1.2:** Quantas releituras do código são necessárias para atingir compreensão completa da funcionalidade em cada estratégia? | **M3:** Número de releituras do código (contagem)<br>**M4:** Tempo total de análise (minutos) |
| | **Q1.3:** Qual estratégia resulta em maior precisão e completude na descrição verbal/escrita da funcionalidade do código? | **M5:** Score de precisão na descrição (0-10)<br>**M2:** Taxa de acerto na identificação (%) |
| **O2: Eficiência em Modificações**<br><br>Avaliar rapidez e qualidade das modificações | **Q2.1:** Qual estratégia de documentação permite aos desenvolvedores implementar modificações funcionais em menor tempo total? | **M6:** Tempo de modificação completa (minutos)<br>**M7:** Produtividade em modificações (LOC/minuto) |
| | **Q2.2:** Em qual estratégia os desenvolvedores conseguem localizar mais rapidamente os pontos exatos do código que precisam ser modificados? | **M8:** Tempo para localizar ponto de modificação (minutos)<br>**M4:** Tempo total de análise (minutos) |
| | **Q2.3:** Qual estratégia resulta em código modificado com melhor qualidade estrutural e menor complexidade? | **M9:** Complexidade ciclomática do código final (número)<br>**M10:** Score de qualidade de código (0-100) |
| **O3: Carga Cognitiva**<br><br>Identificar impacto na experiência do desenvolvedor | **Q3.1:** Qual estratégia de documentação resulta em menor esforço mental percebido pelos desenvolvedores durante as tarefas? | **M11:** NASA-TLX score - carga mental (0-100)<br>**M12:** Escala de esforço subjetivo (1-7) |
| | **Q3.2:** Em qual estratégia os desenvolvedores demonstram maior confiança na correção e qualidade de suas modificações? | **M13:** Escala de confiança auto-reportada (1-5)<br>**M14:** Taxa de verificação/revisão do código (contagem) |
| | **Q3.3:** Qual estratégia de documentação causa menor nível de frustração nos desenvolvedores durante as tarefas de manutenção? | **M15:** Escala de frustração (NASA-TLX) (0-100)<br>**M11:** NASA-TLX score - carga mental (0-100) |
| **O4: Qualidade das Modificações**<br><br>Comparar taxa de erros introduzidos | **Q4.1:** Qual estratégia de documentação resulta em menor quantidade de erros lógicos introduzidos nas modificações? | **M16:** Número de erros lógicos detectados (contagem)<br>**M17:** Taxa de defeitos por 100 LOC (defeitos/100 LOC) |
| | **Q4.2:** Em qual estratégia os desenvolvedores cometem menos erros de sintaxe durante a implementação das modificações? | **M18:** Número de erros de sintaxe durante codificação (contagem)<br>**M6:** Tempo de modificação (minutos) |
| | **Q4.3:** Qual estratégia leva a modificações que causam menos quebras de funcionalidades existentes (regressões)? | **M19:** Número de testes unitários falhados (contagem)<br>**M20:** Score de regressão funcional (%) |

---

## 4. Tabela Completa de Métricas

| **ID** | **Nome da Métrica** | **Descrição Detalhada** | **Unidade de Medida** |
|--------|---------------------|-------------------------|----------------------|
| **M1** | Tempo de primeira compreensão | Tempo decorrido desde o momento em que o participante inicia a leitura do código até o momento em que ele indica verbalmente ou por escrito que compreendeu a funcionalidade principal do sistema. Medido através de timestamp na interface experimental. | minutos |
| **M2** | Taxa de acerto na identificação de funcionalidade | Percentual de funcionalidades corretamente identificadas pelo participante em relação ao total de funcionalidades principais esperadas (checklist de 10 funcionalidades-chave). Calculado como: (funcionalidades corretas / total esperado) × 100. | percentual (%) |
| **M3** | Número de releituras do código | Quantidade de vezes que o participante retorna para reler seções específicas do código durante a fase de compreensão. Medido através de rastreamento de scroll e eye-tracking simulado (auto-relato ou observação). | contagem (número inteiro) |
| **M4** | Tempo total de análise | Tempo total gasto pelo participante analisando e estudando o código antes de iniciar qualquer modificação. Inclui leitura inicial, releituras e formação do modelo mental. Medido desde início da tarefa até primeira linha de código modificada. | minutos |
| **M5** | Score de precisão na descrição | Pontuação atribuída por avaliadores à descrição verbal ou escrita fornecida pelo participante sobre a funcionalidade do código. Rubrica de 0-10 pontos avaliando: completude (4 pontos), correção técnica (3 pontos), clareza (3 pontos). | pontos (0 a 10) |
| **M6** | Tempo de modificação | Tempo total decorrido desde o momento em que o participante inicia a implementação da modificação solicitada até a finalização completa, incluindo testes e validação. Medido através de timestamps no ambiente experimental. | minutos |
| **M7** | Produtividade em modificações | Número de linhas de código efetivamente modificadas (adicionadas + alteradas) dividido pelo tempo total de modificação. Calculado como: LOC modificadas / tempo de modificação. Mede eficiência bruta de codificação. | LOC/minuto (linhas de código por minuto) |
| **M8** | Tempo para localizar ponto de modificação | Tempo decorrido desde a leitura completa da tarefa de modificação até o participante posicionar o cursor na primeira localização exata onde fará mudanças no código. Indica eficiência na navegação e localização. | minutos |
| **M9** | Complexidade ciclomática do código final | Medida quantitativa da complexidade estrutural do código após a modificação, calculada pelo método de McCabe. Conta o número de caminhos independentes através do código. Valores mais baixos indicam código mais simples e manutenível. Calculada usando ferramenta radon ou similar. | número (inteiro, tipicamente 1-50+) |
| **M10** | Score de qualidade de código | Pontuação agregada de qualidade calculada automaticamente através de ferramentas de análise estática (pylint, flake8). Considera: conformidade com PEP8 (40 pts), ausência de code smells (30 pts), duplicação de código (15 pts), coesão (15 pts). Range: 0-100. | pontos (0 a 100) |
| **M11** | NASA-TLX score - carga mental | Pontuação do componente de demanda mental do questionário NASA Task Load Index, aplicado após cada tarefa. Avalia o nível de atividade mental e perceptual requerida. Escala de 0 (muito baixa) a 100 (muito alta). | pontos (0 a 100) |
| **M12** | Escala de esforço subjetivo | Auto-avaliação do participante sobre o esforço mental investido na tarefa, usando escala Likert de 7 pontos: 1 = "muito pouco esforço" a 7 = "esforço extremo". Coletada através de questionário pós-tarefa. | escala Likert (1 a 7) |
| **M13** | Escala de confiança auto-reportada | Nível de confiança do participante na correção e qualidade de suas modificações, medido através de pergunta direta: "Quão confiante você está de que suas modificações estão corretas?". Escala: 1 = "nada confiante" a 5 = "extremamente confiante". | escala Likert (1 a 5) |
| **M14** | Taxa de verificação/revisão do código | Número de vezes que o participante para para revisar, reler ou testar manualmente seu código antes de declarar a tarefa como completa. Indica necessidade de validação repetida devido à incerteza. Medido por observação ou auto-relato. | contagem (número inteiro) |
| **M15** | Escala de frustração (NASA-TLX) | Pontuação do componente de frustração do questionário NASA-TLX, medindo o nível de insegurança, desencorajamento, irritação e estresse experimentado durante a tarefa. Escala de 0 (nenhuma frustração) a 100 (frustração máxima). | pontos (0 a 100) |
| **M16** | Número de erros lógicos detectados | Quantidade de erros de lógica de programação (bugs) detectados através da execução da suíte de testes unitários após a modificação. Inclui: resultados incorretos, exceções não tratadas, comportamentos inesperados. | contagem (número inteiro) |
| **M17** | Taxa de defeitos por 100 LOC | Densidade de defeitos no código modificado, calculada como: (número total de defeitos encontrados / linhas de código modificadas) × 100. Métrica normalizada para comparar qualidade independente do tamanho da modificação. | defeitos por 100 LOC |
| **M18** | Número de erros de sintaxe durante codificação | Quantidade de erros de sintaxe cometidos pelo participante durante a implementação, detectados pelo IDE ou compilador/interpretador. Inclui: erros de indentação, parênteses não fechados, sintaxe incorreta. Coletado através de logs do IDE. | contagem (número inteiro) |
| **M19** | Número de testes unitários falhados | Quantidade de casos de teste da suíte de testes que falharam após a modificação do código. Indica quebras de funcionalidades existentes (regressões). Total de testes na suíte: 25 testes. | contagem (número inteiro, 0 a 25) |
| **M20** | Score de regressão funcional | Percentual de funcionalidades originais que permaneceram funcionando corretamente após a modificação. Calculado como: (testes passados / total de testes) × 100. Valores próximos a 100% indicam modificação sem regressões. | percentual (0 a 100%) |

---

## 5. Contexto das Versões de Código

### Versão A - Código Auto-explicativo
- **Características:** Nomes de variáveis e funções altamente descritivos e semânticos
- **Exemplo:** `calculate_average_completion_time()`, `active_tasks_list`, `user_priority_level`
- **Comentários:** Ausentes ou mínimos (apenas para casos complexos)
- **Filosofia:** O código deve ser auto-explicativo através de naming conventions claras

### Versão B - Código com Comentários Abundantes
- **Características:** Comentários detalhados explicando cada bloco de código
- **Exemplo:** Nomes genéricos (`calc()`, `list1`, `val`) mas com comentários linha a linha
- **Comentários:** Presentes em praticamente todas as funções e blocos lógicos
- **Filosofia:** Documentação via comentários compensa nomes menos descritivos

### Versão C - Código Mal Documentado (Controle Negativo)
- **Características:** Nomes não descritivos e ausência de comentários
- **Exemplo:** `a`, `b`, `x`, `func1()`, `process()`
- **Comentários:** Ausentes
- **Filosofia:** Exemplo de código de baixa qualidade (baseline para comparação)

---
