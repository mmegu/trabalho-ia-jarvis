# JARVIS Acadêmico

Projeto desenvolvido para a disciplina de Inteligência Artificial.

O sistema funciona como um assistente acadêmico capaz de auxiliar estudantes por meio de consulta a materiais de estudo, gerenciamento de agenda, controle de tarefas e planejamento de estudos utilizando técnicas de Inteligência Artificial.

---

## Funcionalidades

### Consulta a materiais de estudo (RAG)

O sistema permite realizar perguntas sobre materiais acadêmicos cadastrados em arquivos `.txt`.

Exemplos:

* "Explique o que é KNN"
* "O que são embeddings?"
* "Resuma o conteúdo sobre Deep Learning"

Para isso, o sistema utiliza:

* embeddings;
* busca vetorial com FAISS;
* recuperação semântica de trechos;
* geração de respostas utilizando uma LLM.

---

### Agenda acadêmica

Permite consultar compromissos acadêmicos cadastrados localmente.

Exemplos:

* "Tenho prova amanhã?"
* "O que tenho hoje?"
* "Quais são minhas aulas esta semana?"

---

### Lista de tarefas

O sistema permite:

* adicionar tarefas;
* listar tarefas;
* concluir tarefas.

---

### Planejamento de estudos

O sistema combina:

* agenda;
* tarefas;
* materiais recuperados pelo RAG.

Exemplos:

* "Monte um plano de estudos para a prova"
* "O que devo priorizar hoje?"

---

### Tool Calling

O sistema possui múltiplas ferramentas integradas.

A escolha da ferramenta é realizada automaticamente pela LLM de acordo com a solicitação do usuário.

Ferramentas implementadas:

* consultar_agenda
* listar_tarefas
* adicionar_tarefa
* concluir_tarefa
* buscar_material_rag
* planejar_estudos
* gerar_exercicios
* recomendar_revisao
* active_recall

---

### Funcionalidades de aprendizado

O sistema implementa funcionalidades voltadas ao aprendizado:

* geração de exercícios;
* recomendação de revisão;
* active recall com avaliação das respostas do usuário.

---

## Dataset

O dataset foi construído utilizando documentos acadêmicos em formato texto, com base nos slides e do ChatGPT.

Temas utilizados:

* Inteligência Artificial
* Redes Neurais
* Deep Learning
* Processamento de Linguagem Natural
* Embeddings
* Clustering
* Overfitting e Underfitting
* Regressão Linear
* Árvores de Decisão
* K-Nearest Neighbors (KNN)

### Origem dos dados

Documentos produzidos com base em materiais acadêmicos estudados durante a disciplina e apoio do ChatGPT.

### Tipo de conteúdo

Arquivos textuais contendo conceitos, definições, aplicações, vantagens, limitações e exemplos.

### Limitações

O dataset possui caráter introdutório e as respostas ficam limitadas ao conteúdo presente nos documentos cadastrados.

### Estratégia de chunking

Os documentos são divididos em pequenos blocos de texto para facilitar a recuperação semântica durante as consultas.

### Impacto no RAG

A divisão em chunks melhora a recuperação de contexto relevante, reduzindo ruídos e aumentando a precisão das respostas.

---

## Avaliação do sistema

O sistema possui um módulo de avaliação que registra:

* pergunta realizada;
* documentos recuperados;
* resposta gerada;
* classificação da resposta.

---

## Análise de erros

Foram identificadas falhas relacionadas a:

* recuperação de documentos;
* geração de respostas;
* ambiguidades na seleção de ferramentas.

Para cada falha são registradas:

* tipo;
* causa;
* possível solução.

---

## Tecnologias utilizadas

* Python
* Sentence Transformers
* FAISS
* OpenAI SDK
* NumPy
* Google Colab
* ChatGPT

---

## IAs utilizadas

Durante o desenvolvimento foI utilizada ferramenta de Inteligência Artificial para:

* revisão de código;
* identificação de bugs;
* sugestões de melhorias;
* apoio na documentação.

Ferramenta utilizada:

* ChatGPT

---

## Estrutura do projeto

```text
data/
├── Inteligência Artificial.txt
├── Redes Neurais.txt
├── Deep Learning.txt
├── Processamento de Linguagem Natural.txt
├── Embeddings.txt
├── Clustering.txt
├── Overfitting e Underfitting.txt
├── Regressão Linear.txt
├── Árvores de Decisão.txt
└── K-Nearest Neighbors (KNN).txt

Trabalho_IA_Jarvis.ipynb
README.md
```
---

## Como executar

1. Instalar dependências:

```bash
pip install sentence-transformers faiss-cpu openai numpy
```

2. Executar inicialmente as células responsáveis por:
- Importações;
- Criação das pastas.

3. Após a criação da pasta `data`, inserir os arquivos `.txt` contendo os materiais acadêmicos.

Exemplo:

```text
data/
├── K-Nearest Neighbors (KNN).txt
├── Árvores de Decisão.txt
├── Inteligência Artificial.txt
```
4. Inserir o token da LLM na célula de configuração da API.

5. Executar as células do notebook em sequência.

6. Utilizar o sistema por meio da função principal `jarvis()`.

---

## Integrantes do trabalho

* Mariana Meguro

