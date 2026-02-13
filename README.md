🚀 Projeto Sentinela: Automação de Feedback com IA
Descrição: Sistema de automação que lê feedbacks de alunos em uma planilha Google, processa o sentimento e a justificativa usando a API do Google Gemini e devolve a análise estruturada para a planilha.

Tecnologias Utilizadas:

n8n (Orquestração de Workflow)

Google Gemini API (Inteligência Artificial)

JavaScript (Tratamento de JSON via nó de código)

Google Sheets API (Banco de dados)

Desafios de Engenharia Superados:

Tratamento de Dados: Implementação de script em JS para fazer o parsing de respostas da IA.

Resiliência e Escalabilidade: Configuração de nós de Wait e gestão de Rate Limiting da API.

Gestão de Incidentes: Intervenção manual para garantir a continuidade do serviço (SLA) durante instabilidade de API externa.