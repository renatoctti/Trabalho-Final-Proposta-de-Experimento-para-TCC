# Plano de Experimento – Código Comentado vs Auto-explicativo

## 1. Identificação Básica

### 1.1 Título do Experimento
**Código com Comentários vs. Código Auto-explicativo: Impacto na Manutenibilidade e Compreensão por Desenvolvedores**

### 1.2 ID / Código do Projeto
EXP-CODE-MAINT-2025-001

### 1.3 Versão do Documento
**Versão:** 1.0  
**Data de Criação:** 23/11/2025 
**Última Atualização:** 23/11/2025

### 1.4 Autores
- Nome: [Renato Cazzoletti]
- Área: Engenharia de Software
- E-mail: [renato.cazzoletti7@gmail.com]
- Instituição: [Pontifícia Universidade Católica de Minas Gerais]

### 1.5 Responsável Principal (PI)
[Renato Cazzoletti] - Pesquisador Principal do Experimento

### 1.6 Projeto Relacionado
Trabalho de Conclusão de Curso (TCC) em Engenharia de Software - Linha de pesquisa em Qualidade de Software e Manutenibilidade de Código

---

## 2. Contexto e Problema

### 2.1 Descrição do Problema / Oportunidade

A manutenibilidade de código é reconhecida como um dos principais desafios na engenharia de software moderna. Estudos indicam que desenvolvedores gastam entre 60% a 70% do tempo total de desenvolvimento em atividades de compreensão de código existente, incluindo leitura, análise e navegação em bases de código.

**Problema Central:** Existe um debate contínuo e não resolvido na comunidade de desenvolvimento de software sobre qual abordagem de documentação é mais eficaz:
- **Abordagem 1:** Uso extensivo de comentários explicativos no código
- **Abordagem 2:** Código "auto-explicativo" através de nomes descritivos e estruturas claras (Clean Code)
- **Realidade:** Muitos projetos apresentam código mal documentado com ambas as deficiências

**Sintomas Observados:**
- Tempo excessivo gasto em compreensão de código durante manutenção
- Alta taxa de erros introduzidos durante modificações
- Frustração de desenvolvedores ao trabalhar com código legado
- Debates inconclusivos em code reviews sobre necessidade de comentários

**Oportunidade de Pesquisa:**
Realizar um estudo empírico controlado para identificar, com evidências quantitativas e qualitativas, qual estratégia de documentação resulta em:
- Melhor compreensão do código
- Modificações mais rápidas e corretas
- Menor carga cognitiva para desenvolvedores
- Maior confiança e satisfação

### 2.2 Contexto Organizacional e Técnico

**Ambiente do Experimento:**
- **Tipo:** Ambiente acadêmico e profissional de desenvolvimento
- **Domínio:** Desenvolvimento de software orientado a objetos
- **Tecnologias:** Python 3.x, ambientes de desenvolvimento modernos (VS Code, PyCharm)
- **Tipo de Sistema:** Sistema de gerenciamento de tarefas (To-Do List)
- **Complexidade:** Código de complexidade média (150-200 linhas por versão)
- **Processo:** Simulação de tarefas típicas de manutenção de software

**Contexto Técnico:**
- Código implementado seguindo princípios de programação orientada a objetos
- Presença de testes unitários para validação de modificações
- Uso de ferramentas de análise estática de código (pylint, flake8)
- Ambiente controlado de experimentação

### 2.3 Trabalhos e Evidências Prévias

**Literatura Acadêmica Relevante:**
- **Clean Code (Robert Martin, 2008):** Defende código auto-explicativo com comentários mínimos
- **Code Complete (Steve McConnell, 2004):** Argumenta por uso balanceado e estratégico de comentários
- **Estudos Empíricos:**
  - Buse & Weimer (2010): Métricas de legibilidade de código
  - Scalabrino et al. (2017): Impacto de nomes de identificadores na compreensão
  - Fakhoury & Arnaoudova (2021): Papel dos comentários na manutenibilidade

**Evidências da Indústria:**
- Debates contínuos em plataformas (Stack Overflow, Reddit r/programming)
- Diretrizes conflitantes em diferentes projetos open-source
- Variação significativa em práticas entre organizações

**Lacuna Identificada:**
Poucos estudos empíricos controlados comparando diretamente as três abordagens (comentado, auto-explicativo, mal documentado) em contexto de manutenção real.

---

## 3.  Escopo 

**Analisar** diferentes estratégias de documentação de código (código com comentários abundantes, código auto-explicativo com nomes descritivos, e código mal documentado)

**com o propósito de** avaliar e comparar seu impacto na manutenibilidade de software

**com respeito a** tempo de compreensão do código, eficiência na implementação de modificações, taxa de erros introduzidos, carga cognitiva percebida e satisfação do desenvolvedor

**do ponto de vista de** desenvolvedores de software com experiência prática em programação

**no contexto de** tarefas típicas de manutenção de software (compreensão de funcionalidade, modificação evolutiva e correção de bugs) em sistemas orientados a objetos escritos em Python.

---

## 4. Escopo e Contexto do Experimento

### 4.1 Escopo Funcional / de Processo 

**Atividades:**
- Tarefa de compreensão de código (leitura e interpretação)
- Tarefa de modificação evolutiva (adicionar nova funcionalidade)
- Tarefa de correção de bugs (identificar e corrigir defeito)

**Artefatos:**
- Código-fonte Python (3 versões do mesmo sistema)
- Testes unitários pré-existentes
- Descrições de tarefas padronizadas
- Questionários de avaliação subjetiva (NASA-TLX, escalas Likert)

**Métricas:**
- Métricas de tempo (compreensão, modificação, localização)
- Métricas de qualidade (complexidade, score de código)
- Métricas de erros (lógicos, sintaxe, testes falhados)
- Métricas subjetivas (carga cognitiva, confiança, frustração)

**Participantes:**
- Desenvolvedores com experiência mínima de 1 ano em Python
- Estudantes de pós-graduação em Computação
- Profissionais júnior a pleno

**Fora do Escopo:**
- Sistemas completos de larga escala (apenas módulos de 150-200 linhas)
- Arquitetura de microsserviços ou sistemas distribuídos
- Código legado extremamente complexo (> 1000 linhas)
- Documentação externa ao código (README, wikis, diagramas)
- Múltiplas linguagens de programação (apenas Python)
- Código em domínios altamente especializados (ex: sistemas embarcados, real-time)
- Trabalho colaborativo em equipe (apenas trabalho individual)
- Ambientes de produção reais
- Desenvolvedores sênior/especialistas (> 7 anos de experiência)
- Desenvolvedores iniciantes (< 1 ano de experiência)

### 4.2 Contexto do Estudo

**Tipo de Organização:**
- Ambiente acadêmico (universidade) para coleta de dados
- Simulação de contexto profissional de desenvolvimento

**Tipo de Projeto:**
- Sistema de gerenciamento de tarefas (To-Do List)
- Domínio: aplicação web comum, familiar à maioria dos desenvolvedores
- Complexidade: média (estruturas de dados, lógica de negócio, persistência simulada)

**Criticidade:**
- Baixa - ambiente controlado sem impacto em sistemas reais
- Sem pressão de prazos de produção
- Foco em aprendizado e coleta de dados

**Perfil de Experiência dos Participantes:**
- **Júnior:** 1-3 anos de experiência em desenvolvimento
- **Pleno:** 3-7 anos de experiência em desenvolvimento
- Conhecimento obrigatório: Python, OOP, testes unitários
- Familiaridade com IDEs modernas (VS Code, PyCharm)

**Ambiente de Execução:**
- Laboratório de computação ou ambiente remoto supervisionado
- Sessões individuais de 90-120 minutos
- Supervisão de pesquisador durante execução

### 4.3 Premissas

**Premissas Técnicas:**
1. **P1:** Todos os participantes possuem conhecimento básico de Python (mínimo 6 meses de experiência prática)
2. **P2:** Ambiente de desenvolvimento (IDE + Python + bibliotecas) está configurado e funcional
3. **P3:** Testes unitários fornecidos são corretos, completos e representativos das funcionalidades
4. **P4:** Ferramentas de coleta de métricas automáticas funcionam corretamente
5. **P5:** Código de 150-200 linhas é representativo de tarefas reais de manutenção

**Premissas de Disponibilidade:**
6. **P6:** Participantes têm disponibilidade de 2-3 horas contínuas para o experimento
7. **P7:** Recursos computacionais (laboratório ou equipamento pessoal) estarão disponíveis
8. **P8:** Não haverá interrupções significativas durante as sessões experimentais
9. **P9:** Conexão de internet estável (se sessões remotas)

**Premissas Comportamentais:**
10. **P10:** Participantes estarão suficientemente motivados para realizar as tarefas com seriedade
11. **P11:** Participantes seguirão as instruções fornecidas
12. **P12:** Participantes fornecerão respostas honestas nos questionários

**Premissas Regulatórias:**
13. **P13:** Aprovação do comitê de ética será obtida antes da execução
14. **P14:** Participantes concordarão com termo de consentimento informado

### 4.4 Restrições

**Restrições de Tempo:**
- **R1:** Experimento completo deve ser concluído em até 10 semanas (da preparação à coleta final)
- **R2:** Cada sessão individual limitada a 120 minutos (restrição de atenção/fadiga)
- **R3:** Coleta de dados deve ocorrer no período letivo (disponibilidade de participantes acadêmicos)

**Restrições de Recursos:**
- **R4:** Orçamento limitado - sem possibilidade de incentivos financeiros significativos
- **R5:** Número limitado de participantes disponíveis (pool estimado de 40-50 pessoas)
- **R6:** Disponibilidade de 1-2 pesquisadores para conduzir sessões

**Restrições Tecnológicas:**
- **R7:** Experimento limitado a uma única linguagem (Python 3.x)
- **R8:** Dependência de ferramentas específicas (limitação de licenças de IDEs profissionais)
- **R9:** Impossibilidade de eye-tracking real (uso de aproximações)
- **R10:** Coleta de métricas automáticas depende de logs da IDE

**Restrições Organizacionais:**
- **R11:** Acesso limitado a desenvolvedores profissionais sênior
- **R12:** Necessidade de aprovação institucional (comitê de ética, coordenação)
- **R13:** Restrições de LGPD para coleta e armazenamento de dados pessoais

**Restrições Metodológicas:**
- **R14:** Não é possível randomizar completamente todos os fatores de confusão
- **R15:** Impossibilidade de controlar completamente ambiente doméstico (sessões remotas)

### 4.5 Limitações Previstas

**Limitações de Validade Externa:**

**L1 - Contexto Artificial:**
- Ambiente de laboratório difere significativamente de ambientes de produção reais
- Ausência de pressão de prazos, interruções e contexto organizacional real
- **Impacto:** Resultados podem não se aplicar totalmente a contextos de alta pressão

**L2 - Tamanho e Complexidade do Código:**
- Código de 150-200 linhas é menor que sistemas reais (geralmente milhares de linhas)
- Complexidade média pode não representar código legado altamente complexo
- **Impacto:** Efeitos podem ser diferentes em sistemas maiores e mais complexos

**L3 - Linguagem Específica:**
- Experimento limitado a Python
- Resultados podem não generalizar para linguagens fortemente tipadas (Java, C#) ou funcionais (Haskell)
- **Impacto:** Conclusões são específicas para linguagens dinâmicas similares

**L4 - Domínio do Problema:**
- Sistema To-Do List é domínio comum e familiar
- Domínios especializados (financeiro, médico, científico) podem ter resultados diferentes
- **Impacto:** Generalização limitada para domínios com vocabulário técnico específico

**L5 - Perfil dos Participantes:**
- Amostra de conveniência (estudantes + voluntários)
- Viés de auto-seleção: participantes interessados em qualidade de código
- Exclusão de desenvolvedores iniciantes (< 1 ano) e muito experientes (> 7 anos)
- **Impacto:** Resultados mais aplicáveis a desenvolvedores júnior-pleno

**L6 - Tarefas Específicas:**
- Apenas 3 tipos de tarefas (compreensão, modificação evolutiva, correção de bug)
- Não inclui: refatoração completa, otimização de performance, debug complexo
- **Impacto:** Resultados podem variar para outros tipos de manutenção

**L7 - Efeito Hawthorne:**
- Participantes sabem que estão sendo observados/medidos
- Podem se comportar de forma diferente do dia-a-dia normal
- **Impacto:** Performance pode ser artificialmente elevada

**L8 - Comparação Binária:**
- Apenas 3 estratégias testadas (comentado, auto-explicativo, mal documentado)
- Não testa combinações híbridas ou níveis intermediários
- **Impacto:** Prática real pode envolver estratégias mistas

---

## 5. Objetivos Específicos

**O1 - Compreensão de Código:** Avaliar o impacto das diferentes estratégias de documentação (comentários vs. nomes descritivos vs. código mal documentado) no tempo necessário para desenvolvedores compreenderem a funcionalidade do código-fonte e na precisão dessa compreensão.

**O2 - Eficiência em Modificações:** Determinar qual estratégia de documentação resulta em modificações de código mais rápidas, eficientes e de maior qualidade estrutural durante tarefas de manutenção evolutiva e corretiva.

**O3 - Carga Cognitiva e Experiência do Desenvolvedor:** Identificar a influência das diferentes estratégias de documentação na carga cognitiva percebida, no nível de confiança dos desenvolvedores em suas modificações e no nível de frustração experimentado durante as tarefas.

**O4 - Qualidade e Correção das Modificações:** Comparar a taxa de erros (lógicos, de sintaxe e regressões funcionais) introduzidos durante modificações de código sob as três diferentes estratégias de documentação.

---

## 6. Tabela GQM - Goal/Question/Metric

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

## 7. Tabela Completa de Métricas

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

## 8. Stakeholders e Impacto Esperado

### 7.1 Stakeholders Principais

**Stakeholder 1 - Pesquisadores e Acadêmicos**
- **Interesse:** Avanço do conhecimento científico sobre manutenibilidade de código
- **Expectativa:** Dados empíricos robustos e publicação de resultados
- **Impacto:** Contribuição para área de Engenharia de Software Experimental

**Stakeholder 2 - Desenvolvedores Participantes**
- **Interesse:** Aprendizado sobre melhores práticas de documentação
- **Expectativa:** Experiência educacional e feedback sobre suas habilidades
- **Impacto:** 2-3 horas de tempo investido, possível ganho de conhecimento

**Stakeholder 3 - Líderes Técnicos e Gerentes de Desenvolvimento**
- **Interesse:** Evidências para embasar decisões sobre padrões de código
- **Expectativa:** Diretrizes práticas baseadas em dados para suas equipes
- **Impacto:** Possível mudança em políticas de documentação e code review

**Stakeholder 4 - Educadores e Instrutores**
- **Interesse:** Material didático sobre qualidade de código
- **Expectativa:** Resultados que possam ser ensinados a estudantes
- **Impacto:** Influência em currículo de disciplinas de engenharia de software

**Stakeholder 5 - Comunidade de Desenvolvimento de Software**
- **Interesse:** Resolução de debate histórico sobre comentários
- **Expectativa:** Resposta baseada em evidências, não em opiniões
- **Impacto:** Influência em práticas e cultura de desenvolvimento

### 7.2 Interesses e Expectativas Detalhados

| Stakeholder | Interesse Principal | Expectativa de Resultado | Nível de Impacto |
|-------------|---------------------|--------------------------|------------------|
| Pesquisadores | Publicação científica | Dados válidos e análises rigorosas | Alto |
| Desenvolvedores | Aprendizado pessoal | Experiência prática e feedback | Médio |
| Líderes Técnicos | Diretrizes práticas | Recomendações aplicáveis | Alto |
| Educadores | Material didático | Casos de ensino baseados em evidências | Médio |
| Comunidade | Esclarecimento técnico | Resolução de controvérsia | Baixo-Médio |

### 7.3 Impactos Potenciais no Processo e Produto

**Durante a Execução do Experimento:**
- **Tempo dos participantes:** Investimento de 2-3 horas por participante
- **Recursos computacionais:** Uso de laboratórios ou ambientes remotos
- **Curva de aprendizado:** Possível ganho de conhecimento para participantes
- **Impacto emocional:** Possível frustração temporária com código mal documentado (Versão C)

**Após a Conclusão do Experimento:**
- **Políticas de código:** Possível revisão de guidelines de documentação em organizações
- **Práticas de code review:** Mudanças em critérios de avaliação de qualidade
- **Treinamento:** Incorporação de resultados em programas de capacitação
- **Ferramentas:** Possível desenvolvimento de ferramentas baseadas nos achados
- **Pesquisas futuras:** Base para estudos subsequentes e replicações

---

## 9. Riscos de Alto Nível, Premissas e Critérios de Sucesso

### 8.1 Riscos de Alto Nível

#### Riscos de Negócio/Acadêmicos
| ID | Risco | Probabilidade | Impacto | Mitigação |
|----|-------|---------------|---------|-----------|
| R1 | Resultados estatisticamente não significativos | Média | Alto | Cálculo de poder estatístico a priori, amostra adequada |
| R2 | Baixa taxa de recrutamento de participantes | Média | Alto | Múltiplos canais de divulgação, incentivos apropriados |
| R3 | Viés de seleção (apenas participantes motivados) | Alta | Médio | Documentar características da amostra, análise de sensibilidade |
| R4 | Impossibilidade de publicação dos resultados | Baixa | Alto | Pré-registro do experimento, protocolo rigoroso |

#### Riscos Técnicos
| ID | Risco | Probabilidade | Impacto | Mitigação |
|----|-------|---------------|---------|-----------|
| R5 | Falhas no ambiente de execução durante sessões | Média | Alto | Ambiente de backup, testes prévios, piloto |
| R6 | Perda de dados coletados | Baixa | Muito Alto | Backup automático, redundância de armazenamento |
| R7 | Instrumentação inadequada (métricas incorretas) | Média | Alto | Piloto para validar instrumentos, revisão por pares |
| R8 | Problemas com gravação de métricas automáticas | Média | Médio | Logs redundantes, coleta manual como backup |

#### Riscos Operacionais
| ID | Risco | Probabilidade | Impacto | Mitigação |
|----|-------|---------------|---------|-----------|
| R9 | Desistência de participantes durante experimento | Média | Médio | Sessões curtas, ambiente confortável, comunicação clara |
| R10 | Tempo insuficiente para completar tarefas | Baixa | Médio | Piloto para calibrar tempo, tarefas ajustadas |
| R11 | Variabilidade excessiva entre participantes | Alta | Médio | Bloqueio por experiência, coleta de covariáveis |
| R12 | Problemas éticos não previstos | Baixa | Alto | Revisão por comitê de ética, consentimento informado |

**Nota sobre Premissas:** As premissas detalhadas estão descritas na Seção 4.3 acima.

### 9.2 Critérios de Sucesso Globais

#### Critérios Quantitativos (Go/No-Go)


 **Critério 1 - Tamanho de Amostra:**
- Mínimo de 24 participantes completam o experimento (8 por grupo)
- Meta ideal: 30 participantes (10 por grupo)

 **Critério 2 - Completude de Dados:**
- Pelo menos 80% dos participantes fornecem dados completos para todas as métricas principais
- Taxa de perda de dados inferior a 20%

 **Critério 3 - Significância Estatística:**
- Identificação de diferenças estatisticamente significativas (p < 0.05) em pelo menos 3 das métricas principais (M1, M6, M16, M11)
- Poder estatístico observado ≥ 0.70

 **Critério 4 - Taxa de Conclusão:**
- Pelo menos 75% dos participantes completam todas as três tarefas (compreensão, modificação, correção)
- Taxa de desistência inferior a 25%

 **Critério 5 - Validade do Instrumento:**
- Feedback dos participantes indica que instruções foram claras (score médio ≥ 4 em escala 1-5)
- Ausência de problemas técnicos críticos que invalidem dados

#### Critérios Qualitativos

 **Critério 6 - Consistência Interna:**
- Métricas relacionadas apresentam correlações esperadas (ex: tempo e erros)
- Ausência de contradições graves nos dados

 **Critério 7 - Relevância Prática:**
- Diferenças observadas têm magnitude praticamente relevante (effect size médio ou grande: d ≥ 0.5)
- Resultados são interpretáveis e acionáveis

### 9.4 Critérios de Parada Antecipada (Stop Criteria)

 **Critério de Parada 1 - Taxa de Desistência Crítica:**
- Taxa de desistência ultrapassa 40% dos participantes recrutados
- Indica problemas sérios no desenho ou execução

 **Critério de Parada 2 - Falhas Técnicas Recorrentes:**
- Mais de 30% das sessões são comprometidas por problemas técnicos
- Instrumentação se mostra fundamentalmente defeituosa

 **Critério de Parada 3 - Questões Éticas:**
- Comitê de ética identifica riscos não previstos aos participantes
- Participantes relatam desconforto ou estresse excessivo (score médio de frustração > 80)

 **Critério de Parada 4 - Mudança de Contexto:**
- Mudanças organizacionais ou tecnológicas tornam o experimento irrelevante
- Recursos críticos se tornam indisponíveis por período prolongado (> 4 semanas)

 **Critério de Parada 5 - Invalidação dos Dados:**
- Descoberta de viés sistemático que compromete todos os dados coletados
- Contaminação entre grupos (participantes compartilham informações sobre as versões)

---

## 10. Contexto das Versões de Código

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
