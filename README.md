# Resumo AWS Certified AI Practitioner (AIF-C01)
### esse resumo é a tradução de um resumo em ingles dessa conta https://github.com/vicsz/aif-c01-study-notes

## Links Úteis
- [Guia Oficial do Exame](https://d1.awsstatic.com/training-and-certification/docs-ai-practitioner/AWS-Certified-AI-Practitioner_Exam-Guide.pdf)
- [Preparação Oficial para o Exame - Amazon Skill Builder](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19554/exam-prep-standard-course-aws-certified-ai-practitioner-aif-c01) - recomendado assistir em 1.5x
- [Questões Práticas Oficiais do Exame](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19790/exam-prep-official-practice-question-set-aws-certified-ai-practitioner-aif-c01-english) - Aproximadamente no nível do exame real.
- [Canvas com as questões](https://www.canva.com/design/DAGiSovb11k/p9QsrmmeMQ7jzZsSJY_SvQ/edit) - Questões igual ao do exame. Acima o pdf com as respostas
- [Simulados + mini simulados + Flash Cards](https://simuladoclf.s3.amazonaws.com/index.html)
- [ Mapa mental do Sage Maker + post-it de assuntos para estudar](https://miro.com/app/board/uXjVINTLH8E=/) 

## Visão Geral

### Inteligência Artificial Geral
- **Definição**: Refere-se a um conceito mais amplo de inteligência artificial, com o objetivo de construir sistemas capazes de realizar qualquer tarefa intelectual que um humano possa executar. É frequentemente usado para descrever metas de longo prazo de criar sistemas de IA altamente autônomos e flexíveis.
- **Conceito-Chave**: IA com capacidade ampla para executar múltiplas tarefas em diferentes domínios, ao contrário de sistemas de IA especializados.
- **Exemplos**: **Sistemas Especialistas**, **Mecanismos de Regras** (ex., MYCIN), que utilizam lógica e regras predefinidas para tomar decisões.

### Aprendizado de Máquina (ML)
- **Definição**: Um subconjunto de IA que permite que sistemas aprendam a partir de dados e façam previsões ou tomem decisões sem programação explícita ou regras.
- **Conceito-Chave**: IA que opera por meio de padrões de dados e treinamento, em vez de instruções codificadas explicitamente.
- **Exemplos**: **Regressão Linear**, **Árvores de Decisão**, **Máquinas de Vetores de Suporte**—algoritmos de aprendizado supervisionado usados para tarefas preditivas.

### Aprendizado Profundo
- **Definição**: Um subconjunto do aprendizado de máquina que utiliza redes neurais com múltiplas camadas (daí o termo "profundo") para modelar padrões complexos em dados.
- **Conceito-Chave**: Eficaz para tarefas como reconhecimento de imagens, processamento de linguagem natural e sistemas autônomos.
- **Exemplos**: **Redes Neurais Convolucionais (CNNs)** para processamento de imagens, **Redes Neurais Recorrentes (RNNs)** para dados sequenciais, como séries temporais ou modelos de linguagem.

### Inteligência Artificial Generativa
- **Definição**: Um subconjunto do aprendizado profundo focado em criar novos conteúdos (como texto, imagens ou música) a partir de dados aprendidos. Modelos de IA generativa são geralmente baseados em **modelos de fundação**, que são modelos grandes e pré-treinados que podem ser adaptados para uma ampla gama de tarefas.
- **Conceito-Chave**: Sistemas de IA que geram saídas novas com base em padrões aprendidos durante o treinamento. Modelos de fundação proporcionam a versatilidade necessária para ajustes em tarefas específicas.
- **Exemplos**: **ChatGPT** para geração de texto, **DALL·E** para geração de imagens, **DeepDream** para geração visual artística.

### Modelos de Linguagem de Grande Escala (LLMs)
- **Definição**: Um tipo de **IA Generativa** focado em entender e gerar texto semelhante ao humano. LLMs são treinados em grandes quantidades de dados de texto para aprender padrões de linguagem, gramática e contexto.
- **Conceito-Chave**: LLMs geram texto coerente e de alta qualidade com base em prompts de entrada e são capazes de realizar tarefas como resumo, tradução e resposta a perguntas.
- **Exemplos**: **GPT-4**, **BERT**, **T5**, **Claude 2**—usados para tarefas como geração de texto, análise de sentimentos, resumo e compreensão de linguagem natural.

---

## Conceitos

### Aprendizado no Contexto
- **Definição**: Um método para aprimorar modelos de IA generativa ao adicionar dados e exemplos adicionais ao prompt, ajudando o modelo a resolver tarefas de forma mais eficaz.

### Tipos de Prompt
- **Prompt de Poucos Exemplos (Few-Shot)**: Fornece alguns exemplos no prompt para guiar o comportamento do modelo.
- **Prompt sem Exemplos (Zero-Shot)**: Não fornece exemplos no prompt, solicitando que o modelo execute a tarefa sem orientação.
- **Prompt com Um Exemplo (One-Shot)**: Fornece exatamente um exemplo para guiar o comportamento do modelo.
- **Modelo de Prompt**: Um formato ou estrutura predefinida para prompts, a fim de padronizar e melhorar a interação com modelos de IA.
- **Prompt de Cadeia de Pensamento**: Um método onde o prompt incentiva o modelo a dividir o raciocínio em etapas.
- **Ajuste de Prompt**: O processo de ajustar prompts para melhorar o desempenho do modelo em tarefas específicas.

### Espaço Latente
- **Definição**: O conhecimento codificado ou padrões capturados por modelos de linguagem de grande escala (LLMs) que armazenam relações entre dados.
- **Uso**: Representa a compreensão interna da linguagem ou dados que os modelos de IA usam para gerar saídas.

### Embeddings
- **Definição**: Representações numéricas e vetoriais de tokens (palavras, frases, etc.) que capturam seu significado semântico.
- **Caso de Uso**: Usado para tarefas como busca semântica, onde o significado de uma palavra ou token é importante.
- **Armazenamento**: Pode ser armazenado em um banco de dados vetorial para busca e recuperação eficiente.

### Tokens
- **Definição**: As unidades básicas de texto (ex., palavras, subpalavras ou caracteres) processadas por modelos de linguagem. No contexto de LLMs, tokens são usados para representar tanto as entradas (texto fornecido) quanto as saídas (texto gerado).

### Janela de Contexto
- **Definição**: A quantidade máxima de tokens que um modelo LLM pode processar de uma vez, incluindo tanto o prompt de entrada quanto a saída gerada pelo modelo. Se o número de tokens exceder a janela de contexto do modelo, partes anteriores do texto podem ser truncadas.
- **Uso**: A janela de contexto é um fator-chave para determinar quanta informação pode ser fornecida ao modelo de uma vez e afeta tarefas como geração de texto de longa duração, análise de documentos ou conversas de múltiplas interações.

### Alucinações
- **Definição**: Alucinações ocorrem quando um modelo de linguagem gera informações incorretas ou sem sentido que podem parecer plausíveis, mas não são fundamentadas em dados factuais ou na entrada fornecida.
- **Mitigações**:
  - Geração Aumentada por Recuperação (RAG): Mitiga alucinações ao recuperar dados externos relevantes durante o processo de geração, garantindo que o modelo gere respostas baseadas em informações precisas.
  - Ajuste Fino: Treinar o modelo com dados mais relevantes e precisos pode ajudar a reduzir alucinações, alinhando a saída do modelo com conhecimento factual.
  - Humano no Loop (HITL): Incorporar revisão humana em áreas de baixa confiança pode evitar que saídas alucinadas sejam usadas em aplicações críticas.

### Modelos Multimodais
- **Definição**: Modelos que trabalham com múltiplos tipos de dados, incorporando texto, imagens ou até áudio em um espaço compartilhado. Esses modelos são comumente usados para tarefas de geração multimodal, como criar legendas para imagens ou gerar visuais a partir de descrições textuais, aproveitando diferentes tipos de entrada para produzir saídas mais ricas e contextualmente conscientes.

---

### Métodos de Busca
- **Busca por Palavras-Chave**: Corresponde a termos exatos na consulta de busca.
- **Busca Semântica**: Usa embeddings para entender o significado por trás da consulta de busca, permitindo resultados mais precisos e significativos.

---

### Bancos de Dados Vetoriais
- **Definição**: Um tipo de banco de dados projetado para armazenar e consultar vetores (embeddings), útil para tarefas como busca semântica.

#### Opções de Bancos de Dados Vetoriais na AWS
- **Amazon OpenSearch Service**: Suporta busca k-vizinhos mais próximos (k-NN) para bancos de dados vetoriais. Útil para análise de logs, monitoramento de aplicativos em tempo real e busca.
- **Amazon Aurora PostgreSQL-Compatible Edition & Amazon RDS for PostgreSQL**: Suporta a extensão **pgvector**, permitindo armazenamento eficiente de embeddings e buscas por similaridade.
- **Amazon Neptune ML**: Usa Redes Neurais de Grafos (GNNs) para fazer previsões baseadas em dados de grafos, suportando dados vetorizados em bancos de dados de grafos.
- **Amazon MemoryDB**: Suporta armazenamento e recuperação de vetores em alta velocidade com tempos de consulta em milissegundos e dezenas de milhares de consultas por segundo (QPS).
- **Amazon DocumentDB**: Suporta busca vetorial com compatibilidade MongoDB, permitindo armazenamento, indexação e busca de milhões de vetores com tempos de resposta em milissegundos.

---

## O Pipeline de Aprendizado de Máquina (ML)

O Pipeline de ML é um processo sistemático usado para construir, treinar e implantar modelos de aprendizado de máquina. Ele garante que cada etapa, desde a identificação de metas de negócios até o monitoramento de modelos implantados, seja gerenciada adequadamente e otimizada para desempenho. As etapas típicas do pipeline são as seguintes:

**Etapas:**
1. Identificar a Meta de Negócios
2. Enquadrar o Problema de ML
3. Coletar Dados
4. Pré-processar Dados
5. Projetar Recursos
6. Treinar, Ajustar, Avaliar
7. Implantar
8. Monitorar

---

### 1. Identificar a Meta de Negócios
- **Descrição**: Definir critérios de sucesso e alinhar as partes interessadas para garantir que o projeto de ML atenda aos objetivos de negócios.
- **Atividades-Chave**:
  - Estabelecer métricas de sucesso claras.
  - Alinhar com as partes interessadas em toda a organização.

### 2. Enquadrar o Problema de ML
- **Descrição**: Definir o problema de ML, entradas, saídas e métricas, considerando viabilidade e análise de custo-benefício.
- **Atividades-Chave**:
  - Identificar entradas, saídas, requisitos e métricas de desempenho.
  - Realizar análise de custo-benefício para avaliar a viabilidade.
  
- **Opções de Modelo**:
  - **Serviço de IA/ML Hospedado** (ex., AWS Comprehend, Forecast, Personalize): Não requer treinamento.
  - **Modelos Pré-treinados** (ex., Amazon Bedrock, SageMaker JumpStart): Ajuste fino com seus dados.
  - **Modelo Totalmente Personalizado**: Construir e treinar do zero.

### 3. Coletar Dados

- **Descrição**: Coletar e preparar os dados necessários para o treinamento do modelo.

- **Atividades-Chave**:
  - Identificar fontes de dados (ex., bancos de dados, data lakes, APIs externas).
  - Ingerir e rotular dados.

- **Onde os Dados são Armazenados**:  
  - Dados coletados para aprendizado de máquina são tipicamente armazenados no **Amazon S3**. Isso se aplica tanto a dados provenientes de sistemas internos quanto a conjuntos de dados de terceiros acessados por meio do **AWS Data Exchange**.

- **Ferramentas**:
  - **AWS Glue**: Para processos **ETL (Extrair, Transformar, Carregar)**, movendo e transformando dados em um formato utilizável antes do armazenamento no **Amazon S3**.
  - **SageMaker Ground Truth**: Para rotulagem humana de dados ambíguos, com dados rotulados armazenados no **Amazon S3**.
  - **AWS Data Exchange**: Permite acesso seguro a conjuntos de dados de terceiros. Esses conjuntos podem ser usados como fontes adicionais de dados de treinamento, e os dados ingeridos são armazenados no **Amazon S3**.
  - **Amazon S3**: Serviço de armazenamento primário onde os dados coletados são armazenados de forma segura antes de serem processados ou usados para treinamento.

### 4. Pré-processar Dados

- **Descrição**: Limpar e preparar os dados, garantindo que sejam adequados para o treinamento.

- **Atividades-Chave**:
  - Realizar **Análise Exploratória de Dados (EDA)**.
  - Limpar os dados, removendo duplicatas, preenchendo valores ausentes e anonimizando **PII**.
  - Dividir os dados frequentemente em proporções de **treinamento (80%)**, **validação (10%)** e **teste (10%)**.

- **Como Limpar os Dados**:
  - **Transformações do AWS Glue**: O Glue possui transformações integradas para tarefas como remover duplicatas ou preencher valores ausentes, e permite transformações personalizadas usando Python ou Spark.
  - **Macie para PII**: O AWS Macie detecta e anonimiza dados **PII**, trabalhando com o **Amazon S3** para escanear e mascarar informações sensíveis.
  - **AWS Glue DataBrew**: Permite preparação e limpeza de dados por meio de uma interface visual. Você pode aplicar **regras de qualidade de dados**, como preencher valores ausentes, e salvar essas transformações como **receitas** para reutilização.
  - **SageMaker Canvas**: Facilita a importação, transformação e visualização de dados sem exigir conhecimento técnico profundo. Usa transformações integradas que são adicionadas passo a passo para preparar os dados para treinamento, e cada etapa pode ser rastreada visualmente no fluxo.

- **Ferramentas**:
  - **AWS Glue**: Um serviço ETL com transformações integradas para limpeza de dados.
  - **AWS Glue DataBrew**: Uma ferramenta visual de preparação de dados onde você pode definir e aplicar regras de transformação (chamadas **receitas**), com verificações de qualidade de dados integradas.
  - **SageMaker Canvas**: Uma ferramenta para importar, preparar e transformar dados com uma interface visual sem código. Cada etapa de transformação faz parte de um fluxo claro, tornando a preparação de dados mais acessível.

### 5. Projetar Recursos
- **Descrição**: Selecionar e projetar recursos que melhorarão o desempenho do modelo.
- **Atividades-Chave**:
  - Seleção de Recursos: Identificar os recursos mais relevantes do seu conjunto de dados com base no conhecimento do domínio, reduzindo a dimensionalidade e melhorando a eficiência do modelo.
  - Criação de Recursos: Transformar dados brutos em novos recursos (ex., escalonamento, codificação de variáveis categóricas e derivação de novas métricas a partir das existentes).
  - Transformação de Recursos: Aplicar transformações matemáticas ou estatísticas (ex., normalização, padronização) para melhorar a convergência e o desempenho do modelo.
- Engenharia de Recursos Automatizada: Considere usar o SageMaker Autopilot, que pode gerar e classificar automaticamente recursos que poderiam melhorar o desempenho do modelo.
- Redução de Dimensionalidade: Técnicas como Análise de Componentes Principais (PCA) podem ser aplicadas para reduzir o número de recursos, mantendo as informações mais importantes.
- Escalonamento de Recursos: Ferramentas como AWS Glue ou SageMaker DataBrew podem ser usadas para aplicar técnicas de escalonamento (ex., normalização ou padronização), garantindo que os recursos contribuam igualmente para o treinamento do modelo.
- Codificação Categórica: Converter variáveis categóricas em valores numéricos usando técnicas como codificação one-hot ou codificação de alvo, usando SageMaker Data Wrangler ou AWS Glue.
  
- **Ferramentas**:
  - **SageMaker Feature Store**: Armazena e gerencia recursos como uma única fonte de verdade.

### 6. Treinar, Ajustar e Avaliar o Modelo
- **Descrição**: Treinar o modelo, ajustá-lo e avaliar o desempenho.
- **Atividades-Chave**:
  - Treinar o modelo iterativamente e ajustar parâmetros.
  - Ajustar hiperparâmetros (ex., época, tamanho do lote, taxa de aprendizado) e realizar experimentos.
  - Avaliar o modelo usando métricas e comparar o desempenho.

- **Parâmetros**:
  - **Parâmetros de Inferência** (suportados pelo Amazon Bedrock):
    - **Aleatoriedade e Diversidade**:
      - Temperatura:
        - Controla a aleatoriedade—valores mais altos levam a saídas mais diversas e criativas; valores mais baixos produzem resultados mais previsíveis e determinísticos.
      - Top K:
        - Limita o modelo a selecionar entre os K tokens mais prováveis; valores menores de K resultam em escolhas mais seguras e previsíveis.
        - Top K não é um parâmetro muito útil - use Temperatura ou Top-P em vez disso.
      - Top P:
        - Usa probabilidade cumulativa para escolher tokens, focando no menor conjunto de tokens com uma probabilidade combinada de P, equilibrando aleatoriedade e diversidade.
        - Valores mais altos de Top P (mais próximos de 1) reduzem a aleatoriedade ao restringir o conjunto de tokens apenas às escolhas mais prováveis.
      - Top-K vs. Top-P: Top K fixa o número de tokens considerados, enquanto Top P usa um número variável de tokens com base em sua probabilidade combinada, tornando Top P mais adaptável e flexível no equilíbrio da aleatoriedade.
      - Temperatura vs. Top P: A temperatura ajusta a aleatoriedade geral ao escalonar probabilidades, permitindo mais ou menos aleatoriedade em todos os tokens possíveis. Top P restringe as escolhas de tokens àqueles que somam um certo limiar de probabilidade, equilibrando aleatoriedade com precisão.
      - Casos de Uso:
        - Use Top-P quando desejar diversidade adaptativa, mas ficar mais próximo de resultados mais prováveis.
        - Use Temperatura quando precisar de controle consistente de aleatoriedade em geral.
    - Comprimento da Resposta:
      - Especifica o comprimento máximo da saída gerada, afetando o quão verbose ou concisa é a resposta.
    - Penalidades:
      - Aplica penalidades a tokens ou sequências repetidas para incentivar variedade no texto gerado.
    - Sequências de Parada:
      - Define sequências específicas onde o modelo interromperá a geração de texto, garantindo um comprimento ou formato de saída controlado.
  - **Parâmetros de Treinamento do Modelo** (Hiperparâmetros):
    - **Época**: O número de iterações pelo conjunto de dados completo.
      - Aumentar as épocas geralmente melhora o aprendizado do modelo, mas pode levar a overfitting se for muito alto. Mais épocas ajudam o modelo a aprender melhor, mas podem resultar em retornos decrescentes após certo ponto.
    - **Tamanho do Lote**: Número de amostras antes de atualizar os parâmetros do modelo.
      - Tamanhos de lote menores fornecem atualizações mais frequentes, o que pode ajudar na convergência rápida, mas pode introduzir mais ruído. Tamanhos de lote maiores são mais estáveis, mas podem exigir mais computação e memória.
    - **Taxa de Aprendizado**: Controla a velocidade com que o modelo aprende.
      - Uma taxa de aprendizado alta acelera o treinamento, mas pode pular soluções ótimas, enquanto uma taxa de aprendizado baixa leva a uma convergência mais lenta, mas mais precisa, embora corra o risco de ficar preso em mínimos locais.
        
- **Métricas de Erro**:

  - **MSE (Erro Quadrático Médio)**: Durante a avaliação do modelo, o MSE calcula a diferença quadrática média entre os valores previstos e os valores reais, dando mais peso a erros maiores. Um MSE mais baixo indica melhor desempenho, tornando-o útil para comparar diferentes modelos ou ajustar hiperparâmetros.
    - **Caso de Uso**: Útil em problemas de regressão, como previsão de preços de casas ou valores de ações.
    - **Regra Geral**: Quanto menor, melhor, pois significa que as previsões do modelo estão mais próximas dos valores reais.
    
  - **RMSE (Raiz do Erro Quadrático Médio)**: RMSE é a raiz quadrada do MSE e fornece uma medida de erro na mesma unidade dos valores previstos, tornando-o mais interpretável. O RMSE é usado para ver quanto erro é esperado por previsão.
    - **Caso de Uso**: Frequentemente usado junto com o MSE em problemas de regressão para facilitar a interpretação.
    - **Regra Geral**: Um RMSE mais baixo significa melhor desempenho do modelo.
  
  - **Perplexidade**: A perplexidade mede quão bem um modelo prevê uma sequência de tokens (ex., palavras). Uma perplexidade mais baixa indica melhor desempenho, pois significa que o modelo é melhor em prever a próxima palavra em uma sequência.
    - **Caso de Uso**: Comumente usado para modelos de linguagem, como avaliar quão bem um modelo prevê a próxima palavra em uma frase.
    - **Regra Geral**: Uma perplexidade mais baixa significa melhor desempenho preditivo.
  
  - **Precisão**: A precisão é a proporção de verdadeiros positivos em relação ao total de previsões positivas (verdadeiros positivos + falsos positivos). É usada quando minimizar falsos positivos é importante.
    - **Caso de Uso**: Frequentemente usado em tarefas de classificação, como detecção de spam, onde evitar falsos positivos é crítico.
    - **Regra Geral**: Maior precisão é melhor quando o custo de falsos positivos é alto.
  
  - **Recall (Taxa de Verdadeiros Positivos)**: O recall (Taxa de Verdadeiros Positivos) é a proporção de verdadeiros positivos em relação ao total de positivos reais (verdadeiros positivos + falsos negativos). É usado quando minimizar falsos negativos é crucial.
    - **Caso de Uso**: Comumente usado em testes médicos (ex., triagem de doenças) para evitar perder casos positivos.
    - **Regra Geral**: Maior recall é melhor quando perder casos positivos é caro.
  
  - **Taxa de Falsos Positivos (FPR)**: A FPR é a proporção de falsos positivos em relação ao total de negativos (falsos positivos + verdadeiros negativos). É usada para medir com que frequência são feitas previsões positivas incorretas.
    - **Caso de Uso WELL**: Frequentemente usado em aplicações de segurança, como detecção de fraudes ou alarmes, onde falsos positivos devem ser minimizados.
    - **Regra Geral**: Uma FPR mais baixa é melhor, pois significa menos falsos alarmes.
  
  - **Especificidade (Taxa de Verdadeiros Negativos)**: A especificidade (Taxa de Verdadeiros Negativos) é a proporção de verdadeiros negativos em relação ao total de negativos reais (verdadeiros negativos + falsos positivos). Ela mede quão bem o modelo identifica instâncias negativas.
    - **Caso de Uso**: Usada em testes médicos para identificar corretamente pacientes não doentes.
    - **Regra Geral**: Maior especificidade é melhor quando identificar verdadeiros negativos é importante.
  
  - **Acurácia**: A acurácia é a proporção de previsões corretas (verdadeiros positivos e verdadeiros negativos) em relação ao total de previsões. É usada quando previsões positivas e negativas são igualmente importantes.
    - **Caso de Uso**: Tipicamente usada em tarefas de classificação equilibradas, como classificação de imagens.
    - **Regra Geral**: Maior acurácia é melhor para correção geral.
  
  - **Pontuação F1**: A pontuação F1 é a média harmônica de precisão e recall, usada quando há necessidade de equilibrar precisão e recall.
    - **Caso de Uso**: Usada em classificação de documentos ou tarefas onde falsos positivos e falsos negativos são importantes.
    - **Regra Geral**: Uma pontuação F1 mais alta significa melhor equilíbrio entre precisão e recall.
  
  - **Curva ROC**: A curva ROC (Característica de Operação do Receptor) plota a taxa de verdadeiros positivos (recall) contra a taxa de falsos positivos em vários níveis de limiar. É usada para avaliar o trade-off entre sensibilidade e especificidade.
    - **Caso de Uso**: Comumente usada em problemas de classificação binária para visualizar o desempenho do modelo em diferentes limiares.
    - **Regra Geral**: Uma área maior sob a curva ROC (AUC) indica melhor desempenho do modelo.
  
- **Problemas de Treinamento do Modelo**:
  - **Overfitting**: Treinamento excessivo nos mesmos dados, fazendo com que o modelo seja excessivamente específico.
    - Solução: Usar dados mais diversos durante o treinamento.
  - **Underfitting**: O modelo não aprende padrões suficientes dos dados.
    - Solução: Treinar o modelo por mais épocas ou com mais dados.
  - **Viés e Equidade**: Falta de diversidade nos dados de treinamento levando a previsões enviesadas.
    - Solução: Garantir dados de treinamento diversos e representativos; incluir restrições de equidade.

- **Ajuste Fino** (BedRock e SageMaker):
  - Ajustar os pesos de um modelo pré-treinado com seus dados específicos e **rotulados** para adaptá-lo a novas tarefas.
  - Esteja ciente de que, se você fornecer instruções para uma única tarefa, o modelo pode perder sua capacidade de propósito geral e sofrer **esquecimento catastrófico**.
  - **Ajuste Fino de Adaptação de Domínio** (SageMaker): Adapta um modelo de fundação pré-treinado a um domínio específico (ex., jurídico, médico) usando uma pequena quantidade de dados específicos do domínio. Isso ajuda o modelo a ter melhor desempenho em tarefas relacionadas a esse domínio particular.
  - **Ajuste Fino Baseado em Instruções** (SageMaker): Envolve fornecer exemplos rotulados de tarefas específicas (ex., resumo, classificação) para melhorar o desempenho do modelo nessa tarefa específica. Esse tipo de ajuste fino é útil para tornar o modelo melhor em tarefas onde saídas precisas são necessárias.
 
- **Pré-treinamento Continuado** (BedRock):
  - Usar dados **não rotulados** para expandir o conhecimento geral do modelo sem restringir seu escopo a uma tarefa específica.
 
- **Transferência de Aprendizado**:
  - Ajustar um modelo existente que aprendeu características gerais e aplicá-lo a um novo problema, acelerando o treinamento e melhorando a precisão.
     
- **Ferramentas**:
  - **SageMaker Training Jobs**: Gerenciar processos de treinamento, especificar dados de treinamento, hiperparâmetros e recursos computacionais.
  - **SageMaker Experiments**: Rastrear execuções de modelos e ajuste de hiperparâmetros.
  - **Ajuste Automático de Modelo (AMT)**: Ajustar automaticamente hiperparâmetros usando a métrica especificada.

### 7. Implantar o Modelo
- **Descrição**: Implantar o modelo treinado para fazer previsões.
    
- Opções de Implantação do SageMaker:
  - **Inferência em Tempo Real**: Para previsões de baixa latência e tráfego sustentado com capacidades de autoescalonamento.
  - **Transformação em Lote**: Para processar grandes lotes de dados de forma assíncrona.
  - **Inferência Assíncrona**: Para solicitações de inferência de longa duração com grandes payloads, tratadas sem respostas imediatas.
  - **Inferência sem Servidor**: Para tráfego intermitente, onde o modelo escala automaticamente sem gerenciamento de infraestrutura.
- Mecanismos de Implantação do Bedrock:
  - **Inferência Sob Demanda**: Inferência com pagamento por uso com base no número de tokens de entrada/saída. Ideal para uso baixo ou esporádico.
  - **Provisionamento de Throughput**: Necessário para modelos personalizados ou ajustados, fornecendo capacidade garantida para inferência consistente e de alto throughput.
  - **Agentes BedRock**: Implantar agentes para fluxos de trabalho de várias etapas, integrando modelos com ferramentas como Amazon Kendra e AWS Lambda para lidar com tarefas complexas.
  
- **Ferramentas**:
  - **AWS API Gateway**: Expor o modelo como um endpoint de API para integração com aplicações.

- **Ferramentas**:
  - **AWS API Gateway (Opcional)**: Usado para expor modelos como APIs RESTful, permitindo integração perfeita com outras aplicações ou microsserviços. É opcional e geralmente usado quando você deseja que aplicações externas interajam com o endpoint do seu modelo.
  - Implantação do SageMaker: Modelos são implantados por meio de imagens Docker armazenadas no Amazon ECR e implantadas no Lambda (para Inferência sem Servidor), EC2, EKS (Elastic Kubernetes Service) ou ECS (Elastic Container Service), dependendo dos casos de uso.
  - Tipos de Instâncias:
    - Inf1: Otimizado para inferência de aprendizado profundo de alto desempenho e custo-benefício usando chips AWS Inferentia.
    - P4: Alimentado por GPUs NVIDIA A100, ideal para inferência em larga escala e de alto desempenho com latência muito baixa.
    - G5: Projetado para cargas de trabalho baseadas em GPU, otimizado para gráficos e inferência de aprendizado de máquina com GPUs NVIDIA.
    - Graviton2 (C6g, M6g): Instâncias baseadas em ARM, eficientes em energia, para tarefas de inferência de aprendizado de máquina de propósito geral.
  - Endpoints do SageMaker: Após a implantação, os modelos são servidos por meio de Endpoints do SageMaker para inferência em tempo real ou tarefas de transformação em lote.
  - Implantação do Bedrock:
    - AWS Lambda: Frequentemente integrado com o Bedrock para Agentes Bedrock para permitir automação em fluxos de trabalho de várias etapas.
    - Amazon Kendra: Quando implantar Agentes Bedrock, o Amazon Kendra é frequentemente usado para busca de documentos e tarefas baseadas em conhecimento.
    - Ferramentas de Provisionamento de Throughput: Provisionamento de capacidade de inferência para aplicações de alto throughput por meio do Console de Gerenciamento da AWS ou da API do Bedrock.

### 8. Monitorar o Modelo
- **Descrição**: Monitorar continuamente o desempenho do modelo e detectar qualquer deriva de dados ou conceito.
- **Atividades-Chave**:
  - Monitorar o modelo em tempo real para deriva de dados e conceito.
  - Configurar alertas e automatizar ações corretivas se o desempenho diminuir.

- **Tipos de Deriva**:
  - Deriva de Dados: Os dados de entrada mudam, mas a relação entre entradas e saídas permanece a mesma (ex., uma demografia diferente).
  - Deriva de Conceito: A relação entre entradas e saídas muda, significando que os padrões aprendidos pelo modelo não se aplicam mais (ex., novos padrões de fraude que o modelo não foi treinado para reconhecer).

- **Ferramentas**:
  - **SageMaker Model Monitor**: Agendar e monitorar deriva de dados, enviar resultados para o CloudWatch e automatizar medidas corretivas.

---

### MLOps e Automação
- **Descrição**: Aplicar princípios de DevOps para gerenciar modelos de aprendizado de máquina ao longo de seu ciclo de vida, focando em automação, controle de versão e monitoramento.
- **Atividades-Chave**:
  - Automatizar implantação, monitoramento e retreinamento de modelos.
  - Garantir integração e entrega contínuas (CI/CD) para atualizações de modelos.
  - Implementar controle de versão para gerenciar múltiplas versões de modelos.
- **Ferramentas**:
  - **SageMaker Pipelines**: Automatizar e gerenciar o fluxo de trabalho de ML de ponta a ponta.
  - **AWS CodePipeline**: Automatizar as fases de construção, teste e implantação para modelos.
  - **SageMaker Model Registry**: Gerenciar e rastrear versões de modelos e metadados.
  - **Amazon S3**: Usado para armazenar artefatos de modelos treinados após o treinamento para SageMaker e Bedrock. Saídas de modelos, incluindo pesos e artefatos, são exportadas para o S3 para fácil acesso durante a implantação e avaliação.

---

### Governança e Explicabilidade de Modelos
- **Descrição**: Garantir transparência, responsabilidade e conformidade regulatória para modelos de ML, tornando seu comportamento interpretável para as partes interessadas.
- **Atividades-Chave**:
  - Implementar estruturas de governança para rastrear o uso e a linhagem do modelo.
  - Usar ferramentas para detectar e mitigar vieses, garantir equidade e explicar previsões.
  - Fornecer documentação clara do histórico e desempenho do modelo para auditorias.
- **Ferramentas**:
  - **SageMaker Clarify**: **Detectar vieses**, explicar previsões do modelo e aumentar a transparência.
  - **SageMaker Model Cards**: Criar documentação para modelos treinados, incluindo métricas de desempenho e uso pretendido.
  - **Governança de ML do SageMaker**: Fornece ferramentas para maior controle e visibilidade sobre modelos de ML, ajudando a rastrear informações do modelo e monitorar comportamentos como vieses.
  - **Rastreamento de Linhagem de ML do SageMaker**: Captura todo o fluxo de trabalho, rastreando a linhagem do modelo para reprodutibilidade e governança.
  - **Glue DataBrew**: Simplifica a governança de dados com preparação de dados visual e regras de qualidade.
  - **AWS Audit Manager**: Automatiza a auditoria de serviços AWS, garantindo conformidade contínua e prontidão para auditoria para regulamentos da indústria.
  - **AWS Artifact**: Fornece acesso sob demanda a relatórios de conformidade e acordos, ajudando as organizações a atender aos requisitos de conformidade.
  - **Cartões de Serviço de IA da AWS**: Aumentam a transparência fornecendo informações sobre casos de uso, limitações, práticas de IA responsável e melhores práticas de desempenho para serviços e modelos de IA.

---

### Otimização de Custo e Desempenho
- **Descrição**: Otimizar o uso de recursos e o desempenho do modelo sem inflar os custos.
- **Atividades-Chave**:
  - Usar treinamento de spot gerenciado para trabalhos de treinamento de baixo custo.
  - Selecionar tipos de instâncias apropriados para o trabalho e aproveitar as capacidades de autoescalonamento.
  - Usar monitoramento de recursos para detectar ineficiências no uso de recursos.
- **Ferramentas**:
  - **AWS Trusted Advisor**: Fornece recomendações para melhorias de custo e desempenho.
  - **SageMaker Managed Spot Training**: Reduz os custos de treinamento usando capacidade sobressalente do AWS EC2.
  - **SageMaker Profiler**: Identifica uso ineficiente de recursos durante o treinamento do modelo.
  - **Amazon Inspector**: Automatiza avaliações de segurança de aplicações de ML, identificando vulnerabilidades que podem levar à degradação de desempenho ou problemas de segurança.

---

### Aprendizado Contínuo e Retreinamento
- **Descrição**: Retreinar continuamente os modelos para levar em conta novos dados e condições em mudança, evitando a degradação de desempenho.
- **Atividades-Chave**:
  - Agendar retreinamento regular do modelo com base em novos dados.
  - Usar ferramentas para detectar quedas de desempenho e iniciar fluxos de trabalho de retreinamento automáticos.
  - Lidar com deriva do modelo monitorando deriva de conceito e dados.
- **Ferramentas**:
  - **SageMaker Model Monitor**: Detectar deriva de dados e acionar fluxos de trabalho de retreinamento.
  - **SageMaker Pipelines**: Automatizar processos de retreinamento de ponta a ponta.

---

### Segurança
- **Descrição**: Implementar as melhores práticas de segurança para proteger modelos de aprendizado de máquina, dados e infraestrutura relacionada.
  
- **Atividades-Chave**:
  - **Princípio do Menor Privilégio**: Garantir que papéis e políticas do IAM concedam apenas as permissões necessárias para tarefas ou funções específicas.
  - **PrivateLink e Endpoints VPC**: Bloquear o **SageMaker** para evitar exposição à internet. Usar **PrivateLink** e **endpoints VPC** para acessar recursos com segurança dentro de sua rede privada.
  - **Criptografia em Repouso e em Trânsito**: Por padrão, o **SageMaker** criptografa dados em repouso e em trânsito usando o **KMS** (Key Management Service).
  - **Papéis e Políticas do IAM**: Criar e gerenciar papéis e políticas do IAM para garantir acesso seguro aos dados e recursos do modelo.
  - **S3 Block Public Access**: Impedir que os dados do modelo sejam expostos garantindo que as configurações de **Bloqueio de Acesso Público do S3** substituam qualquer acesso público potencial.
  - **AWS IAM Identity Center**: Centralizar o gerenciamento de identidade, permitindo acesso a várias contas AWS e integrar com o Active Directory para gerenciamento de identidade.
  
- **Ferramentas**:
  - **AWS Config**: Monitora e registra continuamente alterações de configuração em recursos AWS para garantir conformidade e segurança.
  - **AWS CloudTrail**: Registra chamadas de API e rastreia atividades do usuário para auditoria e conformidade.
  - **Amazon Inspector**: Escaneia automaticamente por vulnerabilidades em ambientes de aprendizado de máquina para garantir que os modelos implantados sejam seguros.
  - **AWS Audit Manager**: Automatiza a auditoria e garante conformidade com regulamentos da indústria, gerando relatórios de auditoria para validação.
  - **AWS Artifact**: Fornece acesso a documentos de conformidade e relatórios de segurança para garantir que seus ambientes de ML atendam aos padrões de segurança e regulatórios.
  - **SageMaker Role Manager**: Simplifica o gerenciamento de permissões e papéis para recursos e serviços do SageMaker.

---

## Serviços

### Serviços de IA Gerenciados da AWS

A AWS oferece uma gama de serviços de IA gerenciados projetados para serem facilmente integrados em aplicações, fornecendo capacidades poderosas de IA sem a necessidade de conhecimento profundo em aprendizado de máquina. Aqui está uma visão geral dos principais serviços:

#### Visão Computacional
- **AWS Rekognition**
  - Comparação e análise facial, detecção de objetos e texto, moderação de conteúdo. Bom para **triagem de conteúdo**, como identificar material violento ou inadequado.

#### Análise de Texto e Documentos
- **AWS Textract** (OCR)
  - Converte imagens digitalizadas em texto, permitindo o gerenciamento de conteúdo digital.
- **Amazon Comprehend** (NLP)
  - Extrai frases-chave, entidades e sentimentos de textos. Útil para analisar **sentimentos de feedback** e detectar **dados PII**.
- **AWS Intelligent Document Processing** (IDP)
  - Um grupo de serviços AWS que, juntos, automatizam a extração, classificação e processamento de dados de vários tipos de documentos. Ele utiliza tecnologias de IA, como Reconhecimento Óptico de Caracteres (OCR), Processamento de Linguagem Natural (NLP) e Aprendizado de Máquina (ML), para lidar com dados não estruturados encontrados em documentos como PDFs, faturas e contratos legais.

#### IA de Linguagem
- **Amazon Lex**
  - Constrói interfaces conversacionais para voz e texto, ideal para criar **chatbots**.
- **Amazon Transcribe**
  - Serviço de conversão de fala em texto, perfeito para criar **legendas para áudio**.
- **Amazon Polly**
  - Converte texto em fala realista, melhorando o engajamento do usuário por meio de voz.

#### Experiência do Cliente
- **Amazon Kendra**
  - Fornece capacidades de busca inteligente de documentos.
- **Amazon Personalize**
  - Oferece recomendações personalizadas de produtos, semelhante a recursos de "você também pode gostar".
- **Amazon Translate**
  - Facilita a tradução de idiomas, suportando interação global com usuários.

#### Métricas de Negócios
- **Amazon Forecast**
  - Prevê pontos futuros em dados de séries temporais, como **níveis de estoque**.
- **Amazon Fraud Detection**
  - Detecta possíveis fraudes em vários cenários, incluindo transações online e criação de novas contas.

#### Amazon Q

- **Amazon Q Business**
  - Um assistente alimentado por IA generativa que ajuda com tarefas como responder perguntas, gerar conteúdo e automatizar fluxos de trabalho, acessando fontes de dados corporativos como S3, SharePoint e Salesforce.
- **Amazon Q Developer**
  - Uma ferramenta para desenvolvedores que inclui recursos como geração de código e varredura de segurança para ajudar a automatizar tarefas relacionadas ao desenvolvimento e teste.
- **Amazon Q no QuickSight**
  - Integrado ao Amazon QuickSight para consultas em linguagem natural, permitindo que os usuários façam perguntas relacionadas à inteligência de negócios e gerem insights a partir de seus dados do QuickSight com IA.
- **Amazon Q no Connect**
  - Integrado ao Amazon Connect, o Amazon Q ajuda a melhorar o atendimento ao cliente respondendo a perguntas, automatizando respostas e gerenciando tickets usando IA de linguagem natural.
- **Amazon Q na Cadeia de Suprimentos da AWS**
  - Integrado à Cadeia de Suprimentos da AWS, o Amazon Q auxilia na otimização e automação do gerenciamento da cadeia de suprimentos, gerando insights a partir de dados da cadeia de suprimentos, otimizando o gerenciamento de estoque e prevendo a demanda.

---

### Amazon SageMaker

O Amazon SageMaker é um serviço integrado de aprendizado de máquina que permite a desenvolvedores e cientistas de dados construir, treinar e implantar modelos de aprendizado de máquina em escala. Os usuários podem criar modelos personalizados do zero ou usar e ajustar modelos existentes por meio do SageMaker JumpStart. Esta plataforma oferece mais controle do que serviços de IA de alto nível, como o AWS Rekognition, permitindo personalização e otimização detalhadas para atender aos requisitos específicos do projeto.

#### SageMaker Studio

O SageMaker Studio é um ambiente de desenvolvimento integrado (IDE) para aprendizado de máquina, fornecendo uma interface única para preparar dados, construir modelos, treinar, ajustar e implantá-los. Ele oferece recursos como notebooks Jupyter para desenvolvimento de código, ferramentas de depuração integradas e gerenciamento de experimentos, tudo dentro de um ambiente colaborativo baseado em nuvem. O Studio também suporta colaboração em tempo real e acesso fácil a várias capacidades do SageMaker, incluindo monitoramento de modelos e preparação de dados.

#### Processo de Treinamento

O processo típico de treinamento do SageMaker inclui vários elementos-chave que ajudam a configurar e gerenciar os trabalhos de treinamento:

- **Locais de Dados de Treinamento**: Os dados são tipicamente armazenados no Amazon S3 e acessados por meio de URLs do S3.
- **Instâncias de Computação de ML**: O SageMaker utiliza instâncias EC2 (instâncias ECR) para poder computacional escalável.
- **Imagens de Treinamento**: O processo de treinamento é executado usando imagens de contêiner Docker projetadas especificamente para aprendizado de máquina.
- **Hiperparâmetros**: Parâmetros que guiam o processo de aprendizado (ex., taxa de aprendizado, tamanho do lote).
- **Bucket de Saída do S3**: Os artefatos do modelo treinado são armazenados em um bucket do S3 para uso posterior.

#### Recursos
- **SageMaker Feature Store**  
  - Repositório central para armazenar, recuperar e compartilhar recursos de aprendizado de máquina.
- **SageMaker Model Registry**  
  - Gerencia diferentes versões de modelos e seus metadados.
- **SageMaker Pipelines**  
  - Fornece um serviço de orquestração de fluxo de trabalho para construir, treinar e implantar modelos com fluxos de trabalho repetíveis.
- **SageMaker Model Monitor**  
  - Utiliza regras integradas para detectar deriva de dados ou criar regras personalizadas, os resultados de monitoramento podem ser enviados para o CloudWatch e automatizar medidas corret VERIFY: Utiliza regras integradas para detectar deriva de dados ou criar regras personalizadas, os resultados de monitoramento podem ser enviados para o CloudWatch e automatizar medidas corretivas.
- **SageMaker Ground Truth**  
  - Utiliza humanos reais para rotular dados, garantindo conjuntos de dados de treinamento de alta qualidade.
- **SageMaker Canvas**  
  - Uma ferramenta visual sem código que permite aos usuários construir modelos com base em seus dados com menos experiência técnica.
- **SageMaker JumpStart**  
  - Acesso a Modelos Pré-treinados e um hub para implantação fácil de soluções de aprendizado de máquina.
- **SageMaker Clarify**  
  - Ferramentas para ajudar a detectar vieses e explicar previsões para aumentar a transparência.
- **SageMaker Role Manager**  
  - Gerencia permissões para recursos e serviços do SageMaker.
- **SageMaker Model Cards**  
  - Cria documentação transparente para modelos treinados.
- **SageMaker ML Lineage Tracking**  
  - Rastreia a linhagem de modelos de ML para estabelecer governança, reproduzir fluxos de trabalho e manter o histórico de trabalho.
- **SageMaker Model Dashboard**  
  - Fornece uma interface unificada para gerenciar e monitorar todas as atividades relacionadas ao modelo.
- **SageMaker Data Wrangler**  
  - Simplifica o processo de preparação de dados para aprendizado de máquina, permitindo limpeza, transformação e visualização de dados de forma rápida e fácil.
- **SageMaker Experiments (Agora chamado MLflow com Amazon SageMaker)**  
  - Rastreia, organiza, visualiza, analisa e compara experimentações iterativas de ML.
- **SageMaker Autopilot**  
  - Constrói, treina e ajusta automaticamente modelos de aprendizado de máquina, oferecendo total visibilidade e controle sobre o processo.
- **Amazon Augmented AI (A2I)**  
  - Permite adicionar revisão humana para previsões de baixa confiança ou amostras aleatórias, garantindo resultados mais precisos.
- **SageMaker Managed Spot Training**  
  - Reduz o custo de treinamento de modelos usando capacidade sobressalente do AWS EC2.
- **SageMaker Profiler**  
  - Identifica ineficiências de recursos em trabalhos de treinamento para minimizar custos sem sacrificar velocidade ou precisão.

---

### Amazon Bedrock

O Amazon Bedrock é um serviço gerenciado e sem servidor que fornece acesso a modelos de fundação (FMs) de alto desempenho de empresas líderes em IA por meio de uma única API. Ele é projetado para facilitar a criação de aplicações de IA generativa, priorizando segurança, privacidade e IA responsável.

#### Preços
- **Pagamento por Uso**: O Amazon Bedrock cobra com base no número de **tokens de entrada e saída** usados durante a inferência. Isso significa que você paga apenas pelos tokens processados ao usar os modelos de fundação.
- **Modelos Ajustados**: Se você estiver usando um **modelo personalizado ou ajustado**, encargos adicionais se aplicam para **Provisionamento de Throughput**, que garante desempenho consistente e capacidade reservada para inferência.

#### Recursos
- **Escolha de Modelo**  
  - Acesse uma variedade de modelos de fundação da AI21 Labs, Anthropic, Cohere, Meta, Mistral AI, Stability AI e Amazon, permitindo a seleção ideal do modelo com base nas necessidades específicas da aplicação.
  - Modelos Amazon Titan
    - Exclusivos do Amazon Bedrock, os modelos Amazon Titan são modelos de fundação pré-treinados de alto desempenho criados pela AWS, projetados para uma ampla gama de casos de uso com práticas de IA responsável.
- **Personalização**  
  - Personalize modelos de fundação privadamente com seus dados usando técnicas como ajuste fino e Geração Aumentada por Recuperação (RAG), aumentando a relevância e precisão do modelo.
- **Avaliação de Modelo de Fundação**  
  - A Avaliação de Modelo no Amazon Bedrock permite avaliar, comparar e selecionar os melhores modelos de fundação para seu caso de uso específico. Você pode avaliar modelos com base em métricas personalizadas, como precisão, robustez e toxicidade, garantindo que atendam aos seus requisitos de desempenho. A integração com o Amazon SageMaker Clarify e o fmeval suporta ainda mais a avaliação de modelos, verificando viés e explicabilidade.
- **Bases de Conhecimento do Bedrock**  
  - Usa Geração Aumentada por Recuperação (RAG) para buscar dados de fontes privadas, fornecendo respostas mais relevantes e precisas com suporte completo para o fluxo de trabalho RAG—gerenciando ingestão, recuperação e aumento de prompts.
  - Melhora as saídas integrando processos de recuperação que trazem conhecimento externo relevante para o modelo generativo.
- **Agentes Bedrock**  
  - Crie agentes capazes de planejar e executar tarefas de várias etapas usando sistemas e fontes de dados da empresa—otimizando tarefas complexas, como consultas de clientes e processamento de pedidos.
- **Sem Servidor**  
  -

  Elimina a necessidade de gerenciamento de infraestrutura, simplificando a implantação e escalonamento de capacidades de IA.
- **Guardrails de Segurança e Privacidade**  
  - Apresenta controles robustos para restringir as saídas de IA, impedindo a geração de conteúdo inadequado e restringindo conselhos sensíveis, como recomendações financeiras, garantindo uso ético e compatível de IA.
- **PartyRock**  
  - Um playground de construção de aplicativos de IA prático alimentado pelo Amazon Bedrock, onde os usuários podem construir rapidamente aplicativos de IA generativa e experimentar modelos sem escrever código.

---

### AWS Glue

O AWS Glue é um serviço ETL (Extrair, Transformar, Carregar) gerenciado e otimizado para a nuvem que ajuda a preparar e carregar dados para análises e modelos de IA.

#### Recursos

- **Serviço ETL do AWS Glue**  
  - Serviço ETL baseado em nuvem para preparação de dados com transformações integradas, como remover duplicatas e preencher valores ausentes.
  - Exemplo de Fluxo de Trabalho: AWS Kinesis Data Streams -> Trabalho ETL do AWS Glue -> CSV para Parquet -> S3 Data Lake.
- **Catálogo de Dados do AWS Glue**  
  - Repositório centralizado para gerenciar e monitorar trabalhos ETL, armazenando metadados (esquemas, não dados) com classificadores integrados.
- **AWS Glue DataBrew**  
  - Ferramenta visual para preparação de dados, definindo regras de qualidade de dados e salvando transformações como "receitas".
- **Qualidade de Dados do AWS Glue**  
  - Detecta anomalias e recomenda regras de qualidade de dados para garantir dados limpos e de alta qualidade para modelos de IA.

---

## Tabelas

### ML Tradicional vs. Aprendizado Profundo

| Categoria          | ML Tradicional                                      | Aprendizado Profundo                          |
|-------------------|-----------------------------------------------------|-----------------------------------------------|
| **Complexidade da Tarefa** | Tarefas bem definidas                             | Tarefas complexas                             |
| **Tipo de Dados** | Dados Estruturados / Rotulados                     | Dados Não Estruturados (Imagens, Vídeos, Texto) |
| **Metodologia**   | Resolve problemas por meio de estatísticas e matemática | Utiliza redes neurais                      |
| **Manipulação de Recursos** | Seleção e extração manual de recursos             | Recursos são aprendidos automaticamente pelo modelo |
| **Custo**         | Menos custoso                                       | Custos mais altos devido a demandas computacionais |

### Tipos de Aprendizado de Máquina

| Tipo de Aprendizado         | Descrição                                          | Desafios                            | Ferramentas AWS              | Casos de Uso Comuns                   |
|-----------------------------|----------------------------------------------------|-------------------------------------|------------------------------|---------------------------------------|
| **Aprendizado Supervisionado** | Usa dados pré-rotulados para treinar modelos.       | Rotular os dados pode ser desafiador. | SageMaker Ground Truth       | Classificação de imagens, detecção de spam |
| **Aprendizado Não Supervisionado** | Trabalha com dados não rotulados para encontrar padrões. | Requer métodos para interpretar padrões. | Nenhum específico            | Agrupamento, detecção de anomalias, LLMs para fases iniciais de treinamento |
| **Aprendizado por Reforço** | Aprende por tentativa e erro para maximizar recompensas. | Requer ambiente para interação do agente. | AWS DeepRacer               | Jogos, robótica, decisões em tempo real |

### Tipos de Modelos de Difusão

| Tipo de Modelo de Difusão | Descrição                                          | Quando Usar                                  | Notas                 |
|---------------------------|----------------------------------------------------|----------------------------------------------|-----------------------|
| **Difusão Direta**        | Adiciona ruído aos dados progressivamente.          | Não é frequentemente usado (adiciona ruído)   |                       |
| **Difusão Reversa**       | Reconstrói dados originais a partir de ruído.      | Criar imagens detalhadas a partir de entradas distorcidas. | Ferramentas de restauração de imagens |
| **Difusão Estável**       | Trabalha em espaço latente reduzido, não diretamente em pixels. | Melhor que a Difusão Reversa                 | Midjourney, DALL-E    |

### Métodos de Inferência do Amazon SageMaker

| Tipo de Inferência     | Implantado Em         | Características                                                         |
|------------------------|-----------------------|-------------------------------------------------------------------------|
| **Lote**               | EC2                   | Custo-benefício para trabalhos grandes e infrequentes                    |
| **Assíncrono**         | EC2                   | Adequado para aplicações não sensíveis ao tempo e com grande payload    |
| **Sem Servidor**       | Lambda                | Tráfego intermitente, períodos sem tráfego, autoescalonamento integrado  |
| **Tempo Real**         | EC2                   | Previsões ao vivo, tráfego sustentado, baixa latência, desempenho consistente |

### Tipos de Dados de Treinamento para Aprendizado de Máquina/IA

| Tipo de Dados       | Exemplo de Fonte de Dados AWS                | Exemplo Real                           |
|---------------------|---------------------------------------------|----------------------------------------|
| **Estruturado**     | Dados SQL armazenados no RDS e depois movidos para o S3 | Informações de clientes em tabelas relacionais |
| **Semi-Estruturado** | Dados no DynamoDB ou DocumentDB e depois movidos para o S3 | Logs JSON de atividade do usuário       |
| **Não Estruturado** | Objetos e arquivos armazenados diretamente no S3 | Imagens, vídeos e documentos PDF        |
| **Séries Temporais** | Dados com carimbo de tempo armazenados no S3 | Dados de dispositivos IoT, dados do mercado de ações |

### Métricas de Desempenho de IA Generativa

| Nome da Métrica                                         | Explicação                                                             |
|---------------------------------------------------------|-------------------------------------------------------------------------|
| **Recall Oriented Understudy for Gisting Evaluation (ROUGE)** | Mede a sobreposição entre texto gerado e referência, bom para resumos. |
| **Bilingual Evaluation Understudy (BLEU)**               | Avalia a precisão da tradução comparando n-gramas entre saídas e referências. |
| **General Language Understanding Evaluation (GLUE)**     | Avalia o desempenho do modelo em várias tarefas de compreensão de linguagem natural. |
| **Holistic Evaluation of Language Models (HELM)**        | Fornece avaliação ampla e específica de tarefas das capacidades do modelo de linguagem. |
| **Massive Multitask Language Understanding (MMLU)**      | Testa o conhecimento do modelo em uma variedade de domínios e tópicos. |
| **Beyond the Imitation Game Benchmark (BIG-bench)**      | Avalia modelos em tarefas de IA criativas e difíceis não cobertas por benchmarks padrão. |
| **Perplexidade**                                        | Mede quão bem um modelo prevê a probabilidade do próximo token ou palavra. |

### Modelos de IA Generativa

| Modelo de IA Generativa                            | Exemplos                               | Caso de Uso/O que é Bom Para                              |
|---------------------------------------------------|----------------------------------------|----------------------------------------------------------|
| **Redes Adversariais Generativas (GANs)**          | StyleGAN, CycleGAN, ProGAN             | Geração de imagens, síntese facial, criação de vídeos      |
| **Autoencoders Variacionais (VAEs)**               | VAE de Kingma & Welling, Beta-VAE      | Redução de ruído em imagens, detecção de anomalias, compressão de imagens |
| **Transformadores**                               | GPT-4, BERT, T5                        | Geração de texto, tradução de idiomas, geração de conteúdo |
| **Redes Neurais Recorrentes (RNNs)**              | LSTMs, GRUs                            | Dados sequenciais, previsão de séries temporais, modelos de linguagem |
| **Aprendizado por Reforço para Tarefas Generativas** | AlphaGo, DQN, OpenAI Five              | IA para jogos, controle autônomo, otimização de tarefas generativas |
| **Difusão**                                      | Stable Diffusion, DALL·E 2, Imagen     | Geração de imagens e texto-para-imagem                    |
| **Modelos Baseados em Fluxo**                     | Glow, RealNVP                          | Geração de imagens de alta qualidade, estimativa de densidade |

### Folhas de Estudo

| **Termo/Conceito**                    | **Descrição**                                                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Top-P**                           | Valor de 0 a 1 — probabilidade cumulativa, equilibra aleatoriedade e precisão, 1 é menos aleatório.                                                                    |
| **Temperatura**                     | Controla a aleatoriedade—valores mais altos levam a saídas mais diversas e criativas; valores mais baixos tornam os resultados mais determinísticos.                   |
| **Épocas**                          | Número de iterações no treinamento de um modelo—mais é geralmente melhor, mas muitas podem levar a overfitting.                                                       |
| **AWS Rekognition**                 | Visão computacional/reconhecimento de imagens, usado para detecção de objetos, análise facial e moderação de conteúdo.                                              |
| **AWS Textract**                    | Serviço **OCR** — converte imagens digitalizadas em texto, extração de dados estruturados de documentos.                                                              |
| **Amazon Comprehend**               | Extrai frases-chave, entidades, sentimentos e dados PII de textos.                                                                                                  |
| **AWS Intelligent Document Processing (IDP)** | Automatiza o processamento de documentos não estruturados (ex., PDFs, faturas) usando Textract, Comprehend e A2I.                                              |
| **Amazon Lex**                      | Serviço para **construção de chatbots** com interfaces conversacionais de texto ou voz naturais.                                                                      |
| **Amazon Transcribe**               | Serviço de **conversão de fala em texto**, incluindo legendagem de áudio.                                                                                             |
| **Amazon Polly**                    | Serviço de **conversão de texto em fala** para converter texto escrito em palavras faladas.                                                                            |
| **Amazon Kendra**                   | Motor de busca inteligente de documentos com compreensão semântica.                                                                                                 |
| **Amazon Personalize**              | Serviço para **recomendações personalizadas de produtos**.                                                                                                            |
| **Amazon Translate**                | Serviço de **tradução de idiomas**.                                                                                                                                  |
| **Amazon Forecast**                 | Fornece **previsão de séries temporais**, ex., previsão de níveis de estoque.                                                                                        |
| **Amazon Fraud Detection**          | Detecta atividades fraudulentas, incluindo transações online e tomadas de conta.                                                                                    |
| **Amazon Q Business**               | Assistente alimentado por IA generativa para processamento de dados corporativos e tarefas.                                                                           |
| **Amazon Macie**                    | Serviço de **detecção e anonimização de dados PII** para segurança de dados.                                                                                          |
| **SageMaker Clarify**               | **Detecção de vieses** e explicabilidade para modelos de aprendizado de máquina.                                                                                       |
| **SageMaker Ground Truth**          | Fornece **rotulagem humana** para conjuntos de dados de **treinamento de modelo**.                                                                                      |
| **Amazon Augmented AI (A2I)**       | **Revisão humana** para previsões de baixa confiança durante **inferência**.                                                                                           |
| **AWS Data Exchange**               | Acessa conjuntos de dados de **terceiros** com segurança.                                                                                                            |
| **Transformações do AWS Glue**       | Transformações ETL, como remover duplicatas e preencher valores ausentes.                                                                                           |
| **Amazon SageMaker JumpStart**      | Hub com modelos pré-treinados e implantações com um clique.                                                                                                         |
| **Amazon SageMaker Canvas**         | Ferramenta sem código para construir e treinar modelos de aprendizado de máquina.                                                                                    |
| **Ajuste Fino**                     | **Ajuste de pesos do modelo** usando **dados rotulados** para melhorar o desempenho em tarefas.                                                                       |
| **Ajuste Fino de Adaptação de Domínio** | Adapta um modelo para um **domínio específico**, como jurídico ou médico, usando pequenos conjuntos de dados.                                                        |
| **Ajuste Fino Baseado em Instruções** | Ajusta um modelo para **melhorar o desempenho em tarefas específicas**, ex., classificação.                                                                          |
| **Pré-treinamento Continuado**      | Usa **dados não rotulados** para **expandir a base de conhecimento do modelo**.                                                                                      |
| **Ajuste Automático de Modelo (AMT)** | Ajusta automaticamente hiperparâmetros para melhorar o desempenho do modelo.                                                                                        |
| **Deriva de Dados**                 | Os dados de entrada mudam, mas a relação entre entradas e saídas permanece a mesma (ex., nova demografia).                                                          |
| **Deriva de Conceito**              | A relação entre entradas e saídas muda, significando que os padrões aprendidos pelo modelo não se aplicam mais (ex., novos padrões de fraude).                      |
| **AWS Trusted Advisor**             | Fornece recomendações para melhorias de custo, desempenho e segurança.                                                                                              |
| **Amazon Inspector**                | Avaliações de segurança automatizadas para cargas de trabalho de aplicações.                                                                                        |
| **AWS PrivateLink**                 | Conexões privadas seguras entre VPCs e serviços AWS.                                                                                                                |
| **AWS Config**                      | Monitora e registra alterações de configuração em recursos AWS para conformidade.                                                                                   |
| **AWS CloudTrail**                  | Registra e rastreia chamadas de API para auditoria.                                                                                                                  |
| **GuardRails do BedRock**           | Impede saídas inadequadas de modelos de fundação e restringe conteúdo arriscado.                                                                                     |
| **Postgres (Aurora ou RDS)**        | Banco de dados SQL com suporte a banco de dados vetorial para busca por similaridade.                                                                                |
| **Amazon DocumentDB**               | Armazenamento JSON, compatível com MongoDB, com suporte a banco de dados vetorial.                                                                                   |
| **Amazon Neptune**                  | Banco de dados de grafos com capacidades de busca vetorial.                                                                                                         |
| **Amazon Neptune ML**               | Usa Redes Neurais de Grafos (GNNs) para prever resultados a partir de dados de grafos.                                                                               |
| **Amazon MemoryDB**                 | Banco de dados em memória com capacidades de busca vetorial rápida.                                                                                                 |
| **Amazon OpenSearch Service**       | Serviço de busca com suporte a banco de dados vetorial para busca por similaridade.                                                                                  |
| **MSE (Erro Quadrático Médio)**     | Diferença quadrática média entre valores previstos e reais, menor MSE indica melhor desempenho do modelo.                                                           |
| **RMSE (Raiz do Erro Quadrático Médio)** | Raiz quadrada do MSE, mais interpretável; menor RMSE é melhor.                                                                                                     |
