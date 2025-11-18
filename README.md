# talent-pilot

Copilot designado a validar área, cidade e posições disponíveis com base em dados fornecidos de forma atualizada. Respondendo sempre sim ou não para informações solicitadas.

# Objetivo do Projeto 🚀

Este copiloto foi desenvolvido para:

- Acelerar consultas internas;

- Evitar erros humanos em filtros por sede/área/posição;

- Automatizar decisões simples com base em um documento fixo;

- Servir como base para copilotos mais complexos no futuro.

# Visão Geral 🧠

Este copiloto foi criado no AI Foundry com o objetivo de responder perguntas sobre vagas disponíveis no processo de Relocation 2026 da empresa, usando exclusivamente os dados contidos na planilha:

Relocation – 2026.csv

O modelo utiliza RAG (Retrieval-Augmented Generation) para buscar informações reais da planilha, garantindo respostas objetivas, confiáveis e sem alucinações.

O output do copiloto é sempre:

- sim

- não

não encontrado na planilha

# Fonte de Dados (RAG) 🗂️

A planilha contém as seguintes colunas:

- Área

- Sede 1

- Sede 2

- Sede 3

- Posição

Qtd

Cada linha representa um conjunto de vagas para uma posição específica, podendo operar em até três sedes diferentes.

# Como o Copilot Funciona 🧩

O copilot:

1. Recebe perguntas do usuário.

2. Consulta o RAG para localizar registros relevantes.

3. Compara as perguntas com os dados da planilha.

Retorna somente:

- sim → quando a informação existe claramente na planilha

- não → quando a planilha mostra que NÃO existe

- não encontrado na planilha → quando o dado não está presente ou a pergunta foge do escopo

Para múltiplas perguntas, responde em lista, mantendo a ordem do usuário.

# Prompt 


