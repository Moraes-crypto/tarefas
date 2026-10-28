# Gerenciador de Tarefas

Este projeto servirá para aprimorarmos nossa lógica de programação ao mesmo tempo em que exploramos conceitos e técnicas de programção back-end e fullstack. Vamos utlizar e desenvolver o conceito de MVC (Model-View-Controller), algumas particularidades da Progrmação Orienta a Objetos, Programação Funcional, persistência de dados, microframework Flask e gerenciador de pacotes do Python (Astral uv).

### Alguns passos iniciais para preparar o projeto:

1. Caso não esteja instalado, prepare o uv no seu OS. Você encontra o script de intalação no site <https://docs.astral.sh/uv/#installation>:
```bash
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

2. Faça a inicialização do projeto com o comando:
```bash
uv init
```
Até então utilizavamos um layout de Pacote (Package Layout) denominando *flat-layout*. O uv adota uma estruturação mais moderna chamada *src-layout*, que previne erros de importação comuns chamados `import shadowing` (impotações mascaradas).

3. Crie um ambiente Virtual do Python:
```bash
uv venv
```

### Ative o ambiente Virtual:
```powershell
.venv\Scripts\activate.ps1 # no Powershell do Windows
```
ou
```bash
source .venv/Scripts/activate # no Git Bash do Windows
```
ou
```bash
source .venv/bin/activate # no Bash do Linux
```

4. Instal o Flask
```bash
uv add flask
```
Será criado um arquivo `uv.lock` contendo as dependências (requerimentos) e versões dos pacotes do seu projeto.

5. Crie um arquivo `app.py` contendo o código inicial do projeto
```python
from flask import Flask

app = Flask(__name__)

@app.route('/test')
def test():
    return "Servidor online!"
```

6. Teste a aplicação iniciando o servidor do Flask
```bash
uv run flask run
```

7. Conector entre o MYSQL com PYTHON
```bash
uv add mysql-connector-python
```