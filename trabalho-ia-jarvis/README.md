# JARVIS Acadêmico

Projeto desenvolvido para a disciplina de Inteligência Artificial.

O sistema funciona como um assistente acadêmico simples, permitindo consulta a materiais de estudo, gerenciamento de agenda e controle de tarefas.

---

## Funcionalidades

### Consulta a materiais de estudo (RAG)

O sistema permite realizar perguntas sobre materiais acadêmicos cadastrados em arquivos `.txt`.

Exemplos:

- "Explique o que é KNN"
- "O que são árvores de decisão?"

Para isso, o sistema utiliza:

- embeddings;
- busca vetorial com FAISS;
- recuperação semântica de trechos;
- geração de respostas utilizando a Gemma 12B.

---

### Agenda acadêmica

Permite consultar compromissos acadêmicos cadastrados localmente.

Exemplos:

- "Tenho prova amanhã?"
- "O que tenho hoje?"

---

### Lista de tarefas

O sistema permite:

- adicionar tarefas;
- listar tarefas;
- concluir tarefas.

---

## Tecnologias utilizadas

- Python
- Sentence Transformers
- FAISS
- OpenAI SDK
- Gemma 12B
- Google Colab
- ChatGPT

---

## Estrutura do projeto

```text
data/
├── K-Nearest Neighbors (KNN).txt
├── Árvores de Decisão.txt
├── Inteligência Artificial.txt

Trabalho_IA_Jarvis.ipynb
README.md
```

---

## Como executar

1. Instalar dependências:

```bash
pip install sentence-transformers faiss-cpu openai
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

4. Inserir o token da API da Gemma na célula de configuração da API.

5. Executar o restante das células em sequência.

---

## Observações

Os materiais foram convertidos para `.txt` para reduzir ruídos de leitura e melhorar a recuperação semântica dos trechos utilizados pelo sistema RAG.

---

## Integrante do trabalho

- Mariana Meguro
