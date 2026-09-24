# Da Desinformação à Decisão

### Protocolo de Gestão para a Expansão Internacional

Trabalho da unidade curricular **Gestão e Visualização da Informação (GVI)**, turma **PL2, Grupo H**, Faculdade de Ciências da Universidade do Porto.

O projeto diagnostica um problema de gestão da informação numa empresa de dispositivos médicos em expansão (a **Company X**) e propõe um protocolo de gestão integrado. O foco do trabalho é **usar visualização de dados para diagnosticar, justificar e comunicar decisões**: cada slide apresenta uma visualização e justifica porque foi escolhida.

📄 **Apresentação completa (20 slides):** [`docs/Grupo_H_PL2_report.pdf`](docs/Grupo_H_PL2_report.pdf)

---

## Índice

1. [O caso](#o-caso)
2. [Solução proposta](#solução-proposta)
3. [Resultados principais](#resultados-principais)
4. [Fundamentos de visualização de dados aplicados](#fundamentos-de-visualização-de-dados-aplicados)
5. [Técnicas usadas em cada visualização](#técnicas-usadas-em-cada-visualização)
6. [Ferramentas](#ferramentas)
7. [Pressupostos e limitações](#pressupostos-e-limitações)
8. [Estrutura do repositório](#estrutura-do-repositório)
9. [Autores](#autores)

---

## O caso

A Company X é uma empresa portuguesa, sediada no Porto, que desenvolve e distribui dispositivos médicos. Tem certificação CE e ISO 13485, opera em 4 mercados (Portugal, Espanha, França em piloto e Brasil em expansão) e regista 98% de satisfação.

O crescimento rápido criou um desfasamento entre a velocidade de entrada em novos mercados e a capacidade de manter as equipas alinhadas. A informação sobre produtos, regulamentação e estratégias comerciais está dispersa, desatualizada ou inacessível, o que leva a decisões baseadas em premissas falsas.

**Problema central:** o escasso conhecimento das equipas internas sobre o produto e as estratégias comerciais, o que as impede de atuar de forma eficaz nos diferentes mercados.

---

## Solução proposta

Um protocolo assente em quatro pilares:

| Pilar | O que inclui |
|---|---|
| **Cloud Service** | Drive hierárquica, website com base de dados e autenticação MFA por perfil |
| **Programa de Mentoria** | Formação de equipas, adaptação cultural e linguística, avaliação pós-formação, parceria com distribuidores |
| **Estudos Comerciais** | Análise de mercados regionais, competidores e margens de retorno |
| **Palestras de Divulgação** | Regulamentos e protocolos internos, cultura empresarial, divulgação de produtos e serviços |

A implementação decorre em 4 fases ao longo de 12 meses: Preparação (mês 1–2), Implementação (mês 3–5), Capacitação (mês 6–8) e Expansão (mês 9–12).

---

## Resultados principais

**Diagnóstico**
- Apenas **16%** dos departamentos usam corretamente os sistemas de informação da empresa.
- No Infomap, **6 de 11** tipos de informação têm risco *Alto*, sobretudo por causa da forma como são armazenados.

**Estado atual dos KPIs face às metas**

| KPI | Meta trimestral | Atual |
|---|---|---|
| Índice de obsolescência | < 5% | 40% |
| Contactos para o suporte (via website) | < 300 | 2000 |
| Taxa de erro da informação | 0% | 20% |
| Tempo de latência | < 30 min | 5 h |
| Acessos inseguros | 0 | 8 |

**Investimento e retorno**
- Investimento total entre **€1.150** e **€3.050**.
- ROI positivo a partir do **2.º ano**, no cenário de implementação total (projeção a 5 anos, com os pressupostos indicados [abaixo](#pressupostos-e-limitações)).

---

## Fundamentos de visualização de dados aplicados

Estes são os princípios que sustentam as escolhas de design do trabalho.

**1. Começar pela pergunta, não pelo gráfico.**
Cada visualização responde a uma pergunta de decisão (onde está a informação? quem a usa? o que causa o problema? quanto custa e quanto rende? o que pode correr mal?). Todos os slides incluem uma **"Justificação de escolha"**, por exemplo porque se usaram *use cases* em vez de BPMN: para mostrar de forma imediata quem faz o quê.

**2. Codificação visual adequada ao tipo de dado.**
Posição, comprimento, cor e símbolo comunicam coisas diferentes. A investigação em perceção gráfica (Cleveland e McGill, 1984) mostra que comparamos posições e comprimentos com mais precisão do que cores ou áreas. Por isso os valores **quantitativos** (a projeção a 5 anos) usam barras alinhadas a uma linha de base, e a **cor** fica reservada a estados e categorias.

**3. Cor semântica com codificação redundante.**
O esquema tipo semáforo (verde, amarelo, vermelho) aparece no Infomap, na matriz comportamental, no orçamento e na matriz de risco. No Infomap, a cor é reforçada com símbolos (✓ existe · ~ existe mal estruturado · ✗ inexistente) e legenda, para que a mensagem não dependa só da cor, por exemplo para leitores daltónicos.

**4. Matrizes e mapas de calor para comparações cruzadas.**
Quando se cruzam duas dimensões (departamento × sistema, probabilidade × impacto), a matriz permite ver padrões e concentrações de uma só vez.

**5. Hierarquia e causalidade.**
As árvores organizam o problema por níveis (causa raiz, causas, problema-chave, consequências, impacto final), com um eixo vertical que rotula cada nível. A árvore de objetivos é a **inversão causal** da árvore de problemas, o que dá rastreabilidade entre diagnóstico e solução.

**6. Modelação de papéis e processos.**
Os diagramas de casos de uso (UML) mostram atores, funcionalidades, relações `include` / `extend` e a fronteira do sistema.

**7. Comparação de cenários com pressupostos explícitos.**
O gráfico de projeção compara três cenários com barras agrupadas e eixo em torno do zero, e declara os pressupostos no rodapé. Mostrar de onde vêm os números é uma questão de integridade gráfica (Tufte, 1983).

**8. Formatação condicional para acompanhar metas.**
As tabelas de ROI e KPIs colorem o desvio face à meta, de modo a destacar o que exige ação.

**9. Narrativa e consistência visual.**
A apresentação segue um fio condutor (introdução → diagnóstico → solução → objetivos → milestones → investimento → risco → conclusão), com uma mensagem por slide, hierarquia tipográfica clara e uma paleta consistente.

### Conceitos de gestão da informação que as visualizações servem

- **Mapeamento da informação** (Infomap): quem produz, quem usa e onde se guarda cada tipo de informação.
- **Governação multi-departamental**: perfis hierárquicos e controlo de acessos (MFA).
- **Qualidade da informação**: KPIs como obsolescência, taxa de erro e latência.
- **Gestão do risco**: probabilidade × impacto, com mitigação associada.

---

## Técnicas usadas em cada visualização

| Visualização | Slide | Pergunta a que responde | Técnica e escolhas de design |
|---|---|---|---|
| **Infomap de diagnóstico** | 6 | Que informação existe, quem a cria e usa, onde está guardada e com que risco? | Matriz de mapeamento com símbolos (✓ ~ ✗) e nível de risco a cores (Baixo, Médio, Alto). Conclusão: o maior problema está no *armazenamento* da informação. |
| **Matriz de análise comportamental** | 7 | De que sistemas depende cada departamento e como os usa? | Matriz departamento × sistema com cores por estado (já existe, mal estruturado, inexistente) e legenda. Compara o real com o ideal da solução. |
| **Árvore de problemas** | 8 | Quais são as causas e as consequências do problema-chave? | Diagrama hierárquico por níveis, com causas coloridas ligadas às dimensões Produto, Leis, Cultura e Língua. |
| **Árvore de objetivos** | 10 | Como a solução responde às causas? | Inversão da árvore de problemas: meios → departamentos → objetivo geral → resultados → ganho de faturação. |
| **Casos de uso (3)** | 11–13 | Quem faz o quê em cada componente do protocolo? | UML com atores, `include` / `extend` e fronteira do sistema: Cloud Service, Estudos Comerciais e Programa de Mentoria. |
| **Milestones** | 14 | Quando e por que ordem se implementa? | Linha temporal em 4 fases com código de cor e marcos (M1–M4). |
| **InfoMap Budget** | 15 | Quanto custa cada recurso e que retorno tem? | Tabela de investimento (mín./máx.), ROI, payback e KPIs, com formatação condicional. |
| **Projeção a 5 anos** | 16 | O que acontece com e sem implementação? | Barras agrupadas por ano, eixo divergente em torno do zero e três cenários (sem implementação, parcial e total). |
| **Matriz de risco** | 17 | Que riscos merecem mais atenção? | Mapa de calor 5×5 (probabilidade × impacto), com a exposição ao risco dada pela cor da célula. |
| **Registo de riscos** | 18 | Que riscos existem e como se mitigam? | Tabela de 12 riscos, agrupados por componente (Cloud Service, Estudos Comerciais, Capacitação), com probabilidade, impacto, nível e mitigação. |

---

## Ferramentas

- **Power BI:** análise e visualização de dados (gráficos e KPIs).
- **Canva:** design da apresentação e dos elementos gráficos.
- **Draw.io:** criação de diagramas de case studys e infomaps.  

---

## Pressupostos e limitações

- A **projeção a 5 anos** parte de uma faturação de base de **€250.000/ano**, com **+15% ao ano** (anos 2–5) na implementação total e **−20% ao ano** sem implementação. Os valores são estimativas de cenário, não dados reais.
- Os **valores de custo e ROI** são intervalos estimados para o caso de estudo.
- **Company X** é o nome usado no caso de estudo.

---


## Autores

Afonso Marcos · Henrique Teixeira · Iara Ferreira · Miguel Lopes

Gestão e Visualização da Informação (GVI), PL2 Grupo H, Faculdade de Ciências da Universidade do Porto.

---

## Referências

- Cleveland, W. S., & McGill, R. (1984). *Graphical Perception: Theory, Experimentation, and Application to the Development of Graphical Methods.* Journal of the American Statistical Association.
- Tufte, E. R. (1983). *The Visual Display of Quantitative Information.* Graphics Press.
