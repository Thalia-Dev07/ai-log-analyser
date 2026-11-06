# AI Log Analyzer & Deploy

Aplicação em Python para análise de logs de infraestrutura utilizando a API do Google Gemini, com execução em ambiente containerizado via Docker.

**Status:** Em desenvolvimento.

## Tecnologias

- Python 3.14
- Google Gemini API
- Google Gen AI SDK
- Docker
- JSON

## Funcionalidades

- Recebimento de logs de infraestrutura.
- Análise de erros utilizando IA generativa.
- Identificação de possíveis causas raiz.
- Classificação de gravidade (BAIXA, MEDIA ou ALTA).
- Geração de recomendações técnicas em JSON.

## Estrutura do projeto
```text
ai-log-analyzer/
├── main.py
├── requirements.txt
├── Dockerfile
├── .dockerignore
└── README.md
```
## Pré-requisitos
- Python 3.14 ou compatível com as dependências.
- Docker instalado.
- Chave de API do Google Gemini.

## 🔍 Passo a Passo Detalhado

### Instalação e execução local

#### Clone o repositório:

```bash
git clone https://github.com/Thalia-Dev07/ai-log-analyzer.git
cd ai-log-analyzer
```

#### Instale as dependências:

```bash
python -m pip install -r requirements.txt
```
#### Configure a variável de ambiente:

```
$env:GEMINI_API_KEY="SUA_CHAVE_API"
```
#### Execute a aplicação:

```
python main.py
```

### Execução com Docker

#### Construa a imagem:

```
docker build -t ai-log-analyzer .
```

#### Execute o container:

```
docker run --rm -e GEMINI_API_KEY=$env:GEMINI_API_KEY ai-log-analyzer
```

#### Exemplo de saída esperada

```json
{
  "causa_raiz": "Limite de conexões simultâneas do banco de dados excedido.",
  "gravidade": "ALTA",
  "solucao_sugerida": "Verificar conexões ativas e revisar as configurações do pool de conexões."
}
```
## Status do projeto

🚧 Em desenvolvimento.

A integração com a API Gemini está em fase de validação devido a erros temporários de disponibilidade (HTTP 503).

## Autor

**Thalia-Dev07**

[GitHub](https://github.com/Thalia-Dev07)
