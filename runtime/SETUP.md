# Configuração local do runtime Teamwork (Windows)

## Pré-requisitos
- Python 3.11 ou superior.
- Acesso ao repositório Teamwork clonado no computador.
- Uma chave de API de um provedor de modelo compatível com o formato OpenAI Chat Completions. A chave deve ser criada no site oficial do provedor e guardada somente no arquivo local `runtime/.env`.

## Instalação
Abra PowerShell na pasta raiz do repositório:

```powershell
py -3 -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install --upgrade pip
py -m pip install -r runtime/requirements.txt
Copy-Item runtime/.env.example runtime/.env
```

Edite `runtime/.env` e configure o OpenRouter:
- `LLM_BASE_URL=https://openrouter.ai/api/v1`
- `LLM_API_KEY`: sua chave privada criada no painel do OpenRouter.
- `LLM_MODEL=openrouter/free`: roteador que seleciona modelos gratuitos compatíveis.
- `TEAMWORK_API_TOKEN`: obrigatório para proteger os endpoints locais. Gere um token forte no PowerShell com `py -c "import secrets; print(secrets.token_urlsafe(32))"` e cole o resultado apenas no arquivo local.

Não compartilhe a chave OpenRouter nem o token do Teamwork. O runtime envia os cabeçalhos de identificação do aplicativo e mantém as credenciais fora do código.

Não envie a chave ou o conteúdo do arquivo .env nesta conversa ou ao GitHub.

## Inicialização
Na pasta raiz do repositório:

```powershell
py -m uvicorn app:app --app-dir runtime --host 127.0.0.1 --port 8000
```

Abra `http://127.0.0.1:8000/docs` para a documentação local da API. O serviço deve permanecer vinculado a `127.0.0.1`; não o exponha à internet.

## Primeiro teste
Consulte `GET /health`, depois `GET /agents`. Envie uma tarefa para um agente habilitado por `POST /tasks`, com JSON como:

```json
{
  "agent_id": "PMO-ATEI-001",
  "objective": "Analise esta ideia de projeto e devolva objetivo, escopo inicial, riscos e perguntas em aberto: criar um aplicativo de organização de estudos."
}
```

Envie o cabeçalho `X-Teamwork-Token` em todas as chamadas protegidas. O endpoint `/health` não exige token; os demais endpoints protegidos retornam erro até que `TEAMWORK_API_TOKEN` esteja configurado. Consulte o resultado com `GET /tasks/{task_id}`.

## Limitações desta primeira versão
Esta versão oferece identidades isoladas, carregamento de Skills, inferência por API, fila simples em background e memória episódica privada por agente. Ainda não implementa delegação automática entre agentes, memória semântica compartilhada, ferramentas reais, aprovação interativa, autenticação de usuários, painel web, limites financeiros por tarefa ou execução de ações externas. Não classifique o Teamwork como plenamente autônomo até que essas camadas sejam implementadas e testadas.