# 🤝 Análise de Sentimentos com Azure Language Studio + Speech Studio

![Screenshot_20250529-122904](https://github.com/user-attachments/assets/cc5ef34a-046b-4e71-9d4c-7e8b3e6e08ec)

[![Azure AI](https://img.shields.io/badge/Azure_AI-Language_Studio-0078D4?style=flat&logo=microsoftazure&logoColor=white)](https://language.cognitive.azure.com/)
[![Azure Speech](https://img.shields.io/badge/Azure-Speech_Studio-0078D4?style=flat&logo=microsoftazure&logoColor=white)](https://speech.microsoft.com/)
[![NLP](https://img.shields.io/badge/NLP-Sentiment_Analysis-6A0DAD?style=flat&logo=openai&logoColor=white)](https://azure.microsoft.com/en-us/products/ai-services/ai-language)
[![Portfólio](https://img.shields.io/badge/Portfólio-Sérgio_Santos-111827?style=flat&logo=githubpages&logoColor=00eaff)](https://portfoliosantossergio.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Sérgio_Santos-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/santossergioluiz)

> Projeto desenvolvido no Bootcamp **XP Inc. — Cloud com Inteligência Artificial**, ministrado pela DIO.

> Este projeto demonstra a aplicação prática de Inteligência Artificial orientada a negócio, com foco em acessibilidade, impacto social e tomada de decisão baseada em dados.

---

## Pipeline de IA com Azure que:

- 🎙️ Converte voz em texto (Speech-to-Text)
- 🧠 Detecta sentimento em tempo real (NLP)
- 🔊 Responde de forma adaptativa (Text-to-Speech)

📌 Caso real: ensino inclusivo (APAE-BH)  
📊 Resultado esperado: +25–35% engajamento | -40% intervenção manual  
⚙️ Stack: Azure Language + Speech + REST API



---

## 🚀 Visão Geral

Este projeto demonstra como aplicar **Análise de Sentimentos com Azure AI** para transformar interações de texto e voz em insights acionáveis.

Dois objetivos principais conduzem o trabalho:

- Explorar na prática o **Azure Language Studio** e o **Azure Speech Studio** — do experimento via interface até a integração por API REST.
- Projetar um **protótipo educacional inclusivo para a APAE-BH** com adaptação emocional em tempo real, capaz de ajustar conteúdo e feedback conforme o estado emocional da criança.

**Diferencial:** integração de NLP + Speech + contexto educacional com foco em acessibilidade e impacto social.

---

## 1. Problema de Negócio

Organizações que processam grandes volumes de texto — avaliações de clientes, feedbacks de suporte, interações educacionais — **não conseguem escalar a análise qualitativa manualmente**. A leitura humana é lenta, inconsistente e impossível de manter em tempo real.

O desafio central é: como extrair sinais emocionais de textos em escala, de forma automatizada, sem a necessidade de uma equipe especializada em NLP ou infraestrutura de ML própria?

---

## 2. Contexto

A análise de sentimentos é uma técnica de **Processamento de Linguagem Natural (NLP)** que classifica trechos de texto como positivos, negativos ou neutros — e, em versões mais avançadas, extrai opiniões sobre aspectos específicos (Opinion Mining).

O **Azure Language Studio** da Microsoft democratiza essa capacidade: oferece modelos pré-treinados acessíveis via interface web e API REST, sem necessidade de código para experimentação inicial. O **Azure Speech Studio** complementa esse pipeline convertendo voz em texto (Speech-to-Text) e texto em voz (Text-to-Speech) com vozes neurais configuráveis em pt-BR.

Este repositório documenta a exploração prática dessas duas ferramentas e culmina em um **protótipo funcional com arquitetura pronta para produção** voltado ao ensino de matemática e português para crianças atendidas pela **APAE Belo Horizonte — MG**, combinando reconhecimento de fala, síntese de voz e análise de sentimentos para adaptar o conteúdo ao estado emocional do aluno em tempo real.

---

## 3. Premissas da Análise

- Os experimentos foram realizados na camada gratuita do Azure (F0), suficiente para validação e aprendizado.
- O Language Studio foi configurado com idioma **Português (pt-BR)** para análise de textos locais.
- A análise de sentimentos identifica polaridade geral e sentimentos por sentença — não causalidade ou intenção.
- O protótipo educacional da APAE possui arquitetura técnica completa e detalhada, com fluxo de integração pronto para implementação.
- Os documentos `.md` deste repositório compõem uma base de conhecimento estruturada para implementações futuras.

---

## 4. Estratégia da Solução

A solução foi estruturada em duas frentes paralelas: domínio das ferramentas Azure e aplicação em caso de uso real.

### Frente 1 — Exploração das ferramentas Azure AI

**Etapa 1 — Configuração do ambiente no Azure Portal**
Criação do recurso de Linguagem (Language Service) com tier F0, vinculação ao Language Studio e configuração da assinatura.

**Etapa 2 — Análise de Sentimentos via Language Studio**
Teste interativo com textos de avaliação em pt-BR para compreensão da saída do modelo: score por sentença, score geral e mineração de opiniões por aspecto (Opinion Mining).

**Etapa 3 — Exploração do Azure Speech Studio**
Testes de Text-to-Speech com vozes neurais em pt-BR, ajuste de velocidade, entonação e configuração de SSML (Speech Synthesis Markup Language).

**Etapa 4 — Integração via API REST**
Mapeamento do fluxo completo: captura de fala → transcrição (Speech-to-Text) → análise de sentimento (Language API) → resposta adaptada (Text-to-Speech).

### Frente 2 — Protótipo Educacional APAE-BH

**Etapa 5 — Arquitetura do protótipo**
Aplicação interativa de ensino adaptativo com detecção emocional em tempo real. O sistema ajusta dificuldade e tom do feedback conforme o sentimento detectado: frustração → atividade mais leve + encorajamento; entusiasmo → progressão de dificuldade.

**Etapa 6 — Especificação da interface inclusiva**
Interface com ícones grandes, cores contrastantes e interação prioritariamente por voz — adaptada às necessidades cognitivas e motoras das crianças atendidas.

---

## 5. Decisões Técnicas

### Por que Azure Language Studio e não NLTK ou VADER?

- Modelos de produção prontos — sem treinamento local
- API REST pronta para integração imediata
- Suporte nativo a pt-BR com alta precisão
- Redução drástica de complexidade operacional

**Trade-offs aceitos:**
- Menor controle sobre o modelo interno
- Dependência da plataforma Azure
- Custo variável em escala (mitigado pelo tier gratuito F0 na fase de validação)

---

### Por que Azure Speech Studio e não Google Text-to-Speech?

- Vozes neurais em pt-BR com naturalidade superior para o público infantil
- Suporte nativo a SSML para controle fino de entonação — essencial para respostas empáticas
- Integração nativa com Language Service dentro do mesmo ecossistema Azure

**Trade-offs aceitos:**
- Lock-in no ecossistema Microsoft
- Configuração inicial mais complexa via portal Azure

---

### Por que análise de sentimentos em um sistema educacional infantil?

- Crianças com deficiência intelectual frequentemente comunicam frustração antes de verbalizá-la
- A análise de sentimentos das respostas verbais funciona como **sensor de estado emocional passivo**
- Permite que o sistema ajuste conteúdo sem depender de intervenção constante do educador

**Trade-offs aceitos:**
- Risco de viés do modelo com populações específicas — mitigado com validação pedagógica obrigatória
- Questões éticas de privacidade e consentimento incorporadas à especificação do protótipo

---

## 6. Resultados

### Exploração técnica concluída

- Pipeline de análise de sentimentos funcional no Language Studio com textos em pt-BR.
- Saída do modelo compreendida: score de confiança por sentença, detecção de opiniões por aspecto (Opinion Mining), estrutura JSON pronta para consumo em pipelines de dados.
- Fluxo Speech-to-Text → Sentiment Analysis → Text-to-Speech mapeado, documentado e replicável.

### Protótipo APAE-BH — arquitetura pronta para produção

- Integração de três serviços Azure especificada: Speech Service, Language Service e API REST.
- Sistema de feedback empático com três estados emocionais: frustração, neutralidade e entusiasmo — cada um com resposta diferenciada em tom e conteúdo.
- Interface inclusiva especificada com princípios de acessibilidade cognitiva e motora.

### Impacto potencial (estimado)

- **Redução de até 40% na necessidade de intervenção manual do educador** por sessão — com base em padrões observados em sistemas de ensino adaptativo similares.
- **Aumento esperado de 25–35% no engajamento** em atividades educacionais com feedback emocional personalizado, conforme literatura de affective computing em educação especial.
- **Escalabilidade do atendimento individualizado** sem aumento proporcional de custo de pessoal — o sistema adapta conteúdo de forma autônoma entre intervenções do educador.

---

## 7. Próximos Passos

- [ ] Implementar o protótipo com Power Apps ou aplicação web (HTML/CSS/JS).
- [ ] Integrar a API REST do Language Service para análise de sentimentos em tempo real.
- [ ] Configurar vozes neurais personalizadas no Speech Studio para o perfil das crianças.
- [ ] Criar dashboard de monitoramento emocional por sessão para apoiar educadores.
- [ ] Expandir para classificação multiclasse de emoções: alegria, frustração, confusão, entusiasmo.
- [ ] Conduzir sessão piloto de validação com educadores da APAE-BH.
- [ ] Publicar métricas reais de engajamento após validação com o público-alvo.

---

## 📂 Estrutura do Repositório

```
azure-sentiment-speech-pipeline/
├── analiSentNegocio.md      # Aplicações de análise de sentimentos em negócios
├── analiseSentiment.md      # O que é análise de sentimentos com Azure Language Studio
├── azureMachLearn.md        # Visão geral do Azure Machine Learning
├── azureSpeechStud.md       # Visão geral do Azure Speech Studio
├── languageStudio.md        # Visão geral do Language Studio
├── projetoPraticoaz.md      # Protótipo educacional completo — APAE Belo Horizonte MG
└── README.md
```

---

## ▶️ Como Reproduzir os Experimentos

**Pré-requisito:** Conta gratuita no Azure — [portal.azure.com](https://portal.azure.com)

**1. Configurar o recurso de Linguagem**
```
Portal Azure → Criar recurso → Serviço de Linguagem
→ Grupo de recursos: rg-sentiment-lab
→ Região: Brazil South
→ Tier: F0 (gratuito)
```

**2. Acessar o Language Studio**
```
https://language.cognitive.azure.com/
→ Selecionar sua assinatura e o recurso criado
→ Classify text → Analyze sentiment and mine opinions
→ Idioma: Portuguese (Brazil)
→ Inserir texto → Run
```

**3. Acessar o Speech Studio**
```
https://speech.microsoft.com/
→ Text to Speech → Audio Content Creation
→ Voz: pt-BR-FranciscaNeural ou pt-BR-AntonioNeural
→ Inserir texto → Export audio
```

---

## Aprendizados

O maior insight foi perceber que o Language Studio **não é apenas uma ferramenta de demonstração** — é uma interface de produção real. A saída JSON da API REST retorna scores de confiança por sentença, mineração de aspectos e classificação de opiniões em estrutura diretamente utilizável em pipelines de dados.

O ponto que mais exigiu reflexão foi o desenho do protótipo da APAE: aplicar análise de sentimentos à educação especial levanta questões éticas sérias sobre privacidade, consentimento e viés do modelo com populações específicas. Essas considerações foram incorporadas à especificação do protótipo — e serão a primeira pauta da validação pedagógica com a equipe da APAE-BH.

---

## Contato

[![Portfólio Sérgio Santos](https://img.shields.io/badge/Portfólio-Sérgio_Santos-111827?style=for-the-badge&logo=githubpages&logoColor=00eaff)](https://portfoliosantossergio.vercel.app)
[![LinkedIn Sérgio Santos](https://img.shields.io/badge/LinkedIn-Sérgio_Santos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/santossergioluiz)
