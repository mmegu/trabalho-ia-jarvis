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

- embeddings
- busca vetorial com FAISS
- recuperação semântica de trechos
- geração de respostas utilizando a Gemma 12B

---

### Agenda acadêmica

Permite consultar compromissos acadêmicos cadastrados localmente.

Exemplos:

- "Tenho prova amanhã?"
- "O que tenho hoje?"

---

### Lista de tarefas

O sistema permite:

- adicionar tarefas
- listar tarefas
- concluir tarefas

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
├── Embeddings.txt
├── Redes Neurais.txt
├── Regressão Linear.txt

Trabalho_IA_Jarvis.ipynb
README.md
```

---

## Funcionamento do RAG

Breve explicação de como está ocorrendo o funcionamento nesta primeira entrega.
O sistema utiliza a técnica RAG para responder perguntas sobre os materiais acadêmicos cadastrados.

Fluxo utilizado:

1. Os arquivos `.txt` são carregados da pasta `data`
2. Os textos são divididos em pequenos trechos (chunks)
3. Os chunks são convertidos em embeddings vetoriais
4. Os embeddings são armazenados no índice vetorial FAISS
5. A pergunta do usuário também é convertida em embedding
6. O sistema recupera os trechos semanticamente mais próximos
7. Os trechos recuperados são enviados para a Gemma 12B gerar a resposta final

Permitindo realizar consultas semânticas utilizando os conteúdos cadastrados localmente.

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
├── Embeddings.txt
├── Redes Neurais.txt
├── Regressão Linear.txt
```

4. Inserir o token da API da Gemma na célula de configuração da API.

5. Executar o restante das células em sequência.

---

## Observações

Os materiais foram convertidos para `.txt` para reduzir ruídos de leitura e melhorar a recuperação semântica dos trechos utilizados pelo sistema RAG.

---

## Integrante do trabalho

- Mariana Meguro
