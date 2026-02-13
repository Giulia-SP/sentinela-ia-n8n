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

Prompt usado no nó da IA escolhida no n8n (Gemini):

Atue como Analista de IA. Analise o feedback abaixo e retorne APENAS um JSON.
Feedback: {{ $json.Feedback }}
Formato de Saída (JSON):
{
"sentimento": "Positivo, Neutro ou Negativo",
"justificativa": "Explique em uma frase curta",
"acao": "Sugestão de ação prática"
}
"Responda APENAS o JSON. Não use marcações como ```json ou texto explicativo."

Anexos: 
Legenda: Arquitetura do pipeline de dados desenvolvido. O fluxo contempla a extração (Google Sheets), inteligência (Gemini API), tratamento de erros (Wait/Delay) e transformação de dados (JavaScript/Code Node).
<img width="1847" height="815" alt="image" src="https://github.com/user-attachments/assets/cc2e31c2-c7c4-4156-85a3-ae3906df9163" />

Legenda: Visualização final do Banco de Dados após o processamento da IA. As colunas de Sentimento, Justificativa e Ação foram populadas automaticamente via integração n8n + Gemini.
<img width="1812" height="422" alt="image" src="https://github.com/user-attachments/assets/f06569ef-378b-41dc-9446-5f5489438aa2" />

Legenda: Planilha após intervenção manual para garantir a continuidade do serviço (SLA) durante instabilidade de API externa.
<img width="1822" height="357" alt="image" src="https://github.com/user-attachments/assets/e4f7e172-31af-41a4-a260-ef4eb50a4cdf" />



