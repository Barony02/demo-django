# Demo Django

Projeto de demonstração desenvolvido com Django, framework Python para criação de aplicações web seguras, organizadas e escaláveis.

## Visão geral

Este projeto serve como base para estudar e desenvolver uma aplicação Django. A estrutura pode ser expandida com novas aplicações, modelos, páginas, APIs, autenticação e integrações com serviços externos.

## Pré-requisitos

- Python 3.10 ou superior;
- `pip`;
- Git (opcional, para versionamento);
- Um banco de dados compatível com a configuração do projeto.

## Instalação

No Windows, execute no terminal:

```powershell
git clone <url-do-repositorio>
cd demo-django
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Caso o arquivo `requirements.txt` ainda não exista, instale o Django diretamente:

```powershell
pip install django
```

## Configuração

1. Crie um arquivo `.env` para variáveis de ambiente, se o projeto utilizar esse recurso.
2. Configure a chave secreta, o modo de depuração, os hosts permitidos e o banco de dados.
3. Nunca publique credenciais ou chaves secretas no repositório.

Exemplo de configurações comuns:

```env
DEBUG=True
SECRET_KEY=chave-de-desenvolvimento
ALLOWED_HOSTS=localhost,127.0.0.1
```

## Banco de dados

Aplique as migrações antes de iniciar a aplicação:

```powershell
python manage.py makemigrations
python manage.py migrate
```

Para criar um usuário administrador:

```powershell
python manage.py createsuperuser
```

## Executando o projeto

Inicie o servidor de desenvolvimento com:

```powershell
python manage.py runserver
```

Acesse `http://127.0.0.1:8000/`. O painel administrativo, quando habilitado, fica disponível em `http://127.0.0.1:8000/admin/`.

## Comandos úteis

```powershell
python manage.py check
python manage.py test
python manage.py collectstatic
python manage.py shell
```

- `check`: identifica problemas comuns na configuração.
- `test`: executa os testes automatizados.
- `collectstatic`: reúne arquivos estáticos para publicação.
- `shell`: abre um terminal interativo com o ambiente Django carregado.

## Estrutura esperada

```text
demo-django/
├── manage.py              # Utilitário de linha de comando do Django
├── <projeto>/              # Configurações, URLs e WSGI/ASGI
├── <aplicacao>/            # Regras de negócio da aplicação
├── templates/              # Templates HTML
├── static/                 # CSS, JavaScript e imagens
├── tests/                  # Testes automatizados
├── requirements.txt        # Dependências Python
└── .env                    # Configurações locais (não versionar)
```

## Boas práticas

- Mantenha configurações sensíveis em variáveis de ambiente.
- Separe responsabilidades em aplicações Django pequenas e coesas.
- Escreva testes para modelos, views, formulários e endpoints.
- Use migrações para versionar alterações no banco de dados.
- Desative `DEBUG` e configure `ALLOWED_HOSTS` antes da publicação.
- Use HTTPS, proteção CSRF e autenticação adequada em produção.

## Licença

Defina aqui a licença do projeto quando ela for escolhida.
