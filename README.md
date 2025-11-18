# talent-pilot

Copilot designado a validar área, cidade e posições disponíveis com base em dados fornecidos de forma atualizada. Respondendo sempre sim ou não para informações solicitadas.

# Objetivo do Projeto 🚀

Este copilot foi desenvolvido para:

- Acelerar consultas internas;

- Evitar erros humanos em filtros por sede/área/posição;

- Automatizar decisões simples com base em um documento fixo;

- Servir como base para copilotos mais complexos no futuro.

# Visão Geral 🧠

Este copilot foi criado no AI Foundry com o objetivo de responder perguntas sobre vagas disponíveis no processo de Relocation 2026 da empresa, usando exclusivamente os dados contidos na planilha:

[Relocation – 2026.pdf](https://github.com/viajagabs/talent-pilot/blob/main/Relocation%20-%202026.pdf)

O modelo utiliza RAG (Retrieval-Augmented Generation) para buscar informações reais da planilha, garantindo respostas objetivas, confiáveis e sem alucinações.

O output do copiloto é sempre:

- sim

- não

- não encontrado na planilha

# Fonte de Dados (RAG) 🗂️

A planilha contém as seguintes colunas:

- Área

- Sede 1

- Sede 2

- Sede 3

- Posição

- Qtd

Cada linha representa um conjunto de vagas para uma posição específica, podendo operar em até três sedes diferentes.

# Como o Copilot Funciona 🧩

O copilot:

1. Recebe perguntas do usuário;

2. Consulta o RAG para localizar registros relevantes;

3. Compara as perguntas com os dados da planilha.

Retorna somente:

- sim → quando a informação existe claramente na planilha

- não → quando a planilha mostra que NÃO existe

- não encontrado na planilha → quando o dado não está presente ou a pergunta foge do escopo

Para múltiplas perguntas, responde em lista, mantendo a ordem do usuário.

# Prompt ⚙️

˜Você é um copiloto especializado em responder estritamente com base no pdf anexado, que contém as seguintes colunas:
Sua função é analisar os dados indexados via RAG e responder a perguntas do usuário com base exclusivamente no conteúdo do pdf.
Resposta obrigatória, apenas: 

• “sim”  
• “não”  
• ou “não encontrado na planilha”
Quando o usuário fizer múltiplas perguntas na mesma mensagem, responda em formato de lista, mantenha a ordem das perguntas, use apenas “sim”, “não” ou “não encontrado na planilha”

Regras
1. Use sempre o RAG para buscar evidências na planilha
2. Responda “sim” apenas quando houver correspondência explícita nos dados da planilha
3. Responda “não” quando a pergunta for clara, mas a planilha mostrar que aquilo NÃO existe
4. Use “não encontrado na planilha” quando: O conceito não existir na planilha, a pergunta envolver informação externa, não for possível confirmar apenas com os dados disponíveis, não forneça explicações, justificativas, análises ou textos adicionais
6. Não traga valores da planilha, apenas sim ou não.
7. Caso necessário, considere correspondência parcial de texto quando for evidente (ex.: “engenheiro” para “Software Engineer II/III”).
8. Perguntas sobre quantidade só podem ser respondidas se a planilha trouxer números suficientes
9. Nunca invente, assuma ou complemente informações.˜

# Exemplos de perguntas que o copilot responde:

Perguntas válidas:

“Existe Software Engineer III em Campinas?”

“Há vagas na área Global?”

“Tem Tech Lead em Belo Horizonte?”

“Existem mais de 2 vagas de Software Engineer II?”

# Boas Práticas ao Usar o Copilot ✍️

- Faça perguntas diretas e objetivas;

- Especifique área, posição ou sede quando possível;

- Evite perguntas abertas que não podem ser respondidas com sim/não.

# Passo a passo da criação do Copilot 🧪

- Criação de recurso no AI Foundry;
- [Criação do projeto;](https://github.com/viajagabs/talent-pilot/blob/main/talent-pilot%20passo%201.png)
- [Escolha do agente;](https://github.com/viajagabs/talent-pilot/blob/main/talent-pilot%20passo%202.png)
- [Inclusão de  documento;](https://github.com/viajagabs/talent-pilot/blob/main/talent-pilot%20passo%204.png)
- [Inclusão de prompt e descrição;](https://github.com/viajagabs/talent-pilot/blob/main/talent-pilot%20passo%205.png)
- [Testando o copilot](https://github.com/viajagabs/talent-pilot/blob/main/teste%203%20ai.png)


  # Referências 📚
  
  - [AI Foundry na prática](https://github.com/Miyake-Diogo/AzureFrontierGirls-AI-Challenge/blob/main/Aula%201/Azure_AI_Foundry_na_Pratica.md)

  

  
