# Projeto Final

Projeto de setup profissional de Python desenvolvido durante a Pós Tech, demonstrando o uso de **uv** para gerenciamento de ambiente, dependências e variáveis de ambiente seguras.

> 💡 **Sobre o projeto:** esta é a simulação de um ambiente real de engenharia de dados. Use o código como uma aula para entender como configurar um setup profissional e subir no GitHub.

## Tecnologias

- **Python** >= 3.12
- **[uv](https://github.com/astral-sh/uv)** — gerenciador de ambiente e dependências
- **pandas** — análise de dados
- **requests** — requisições HTTP
- **python-dotenv** — carregamento de variáveis de ambiente

## Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/Mssvargas/Projeto_Final.git
cd Projeto_Final
```

### 2. Instale as dependências

O `uv` cria o ambiente virtual e instala tudo a partir do `pyproject.toml`/`uv.lock`:

```bash
uv sync
```

### 3. Configure as variáveis de ambiente

Copie o arquivo de exemplo e preencha com seus valores:

```bash
cp .env.example .env
```

Edite o `.env` com suas credenciais:

```
DB_HOST=servidor.banco.com
DB_USER=seu-usuario
DB_PASSWORD=sua-senha
API_KEY=sua-chave
```

> ⚠️ O arquivo `.env` **não** é versionado (está no `.gitignore`). Nunca suba suas credenciais para o repositório.

### 4. Execute o projeto

```bash
uv run main.py
```

Saída esperada:

```
Conectando em servidor.banco.com com usuário seu-usuario
Credenciais carregadas com sucesso!
```

## Estrutura

```
Projeto_Final/
├── .env.example      # modelo das variáveis de ambiente (seguro)
├── .gitignore        # ignora .env, .venv e caches
├── .python-version   # versão do Python (pyenv)
├── main.py           # script principal
├── pyproject.toml    # metadados e dependências
├── uv.lock           # versões travadas das dependências
└── README.md
```
