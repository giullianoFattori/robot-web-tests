# Estrutura de pastas utilizadas

```
robot-web-tests/
├── keywords
│   └── common
│       └── example.robot
├── lib
│   ├── DriverLib.py
│   └── __pycache__
│       ├── BaseLib.cpython-38.pyc
│       ├── BaseLib.cpython-39.pyc
│       ├── DriverLib.cpython-38.pyc
│       ├── DriverLib.cpython-39.pyc
│       ├── Jira.cpython-38.pyc
│       └── Jira.cpython-39.pyc
├── logs
├── page_elements
│   └── common
│       └── example.robot
├── resources
│   ├── credenciais
│   │   └── exemplo-dicionario.robot
│   ├── dependencies
│   │   ├── get-pip.py
│   │   └── requirements.txt
│   ├── environments
│   │   └── exemplo-urls.robot
│   ├── helpers.robot
│   ├── keywords.robot
│   ├── libraries.robot
│   └── page_objects.robot
└── tests
    └── exemplo.robot

# IDE 

### Visual Studio Code
Link para instalação [Visual Studio Code](https://code.visualstudio.com/).
  
<br  />  

#### Step de instalação:
1. Instalar a extensão Python (mantida pela Microsoft).
2. Instalar a extensão Robot Framework (mantida pelo Tomi Turtiainen).

<br  />
<br  />

# Framework

* Python

* Robot Framework

<br  />
<br  />

# Configuração de ambiente Windows
  
### Instalar o Python

Link para instalação [Python](https://www.python.org/downloads/).

<br  />

#### Step de instalação:

1. Na tela **Install Python** selecionar as opções **Install launcher for all users (recommended)**, **Add Python to Path** e clicar na opção **Customize installation**.

2. Na tela **Optional Features** selecionar todas as opções e clicar no botão **Next**.

3. Na tela **Advanced Options** selecionar as opções **Install for all users**, **Associate files with Python (requires the py laucher)**, **Create shortcuts for installed applications**, **Add Python to environment variables** e **Precompile standard library**, definir o local de instalação no `C:\`. Por exemplo, `C:\Python38` e clicar no botão **Install**.

Para ter certeza que o Python e o pip foram instalados com êxito é necessário abrir o prompt de comando do Windows e executar os seguintes comandos:

*  `python --version`

*  `pip --version`

> OBS.: Caso esteja tudo certo será exibido no prompt de comando as versões do Python e pip instaladas.

<br  />
<br  />

# Instalação das libraries necessárias para o projeto

1. Baixar o projeto `robot-web-tests` do BitBucket para a sua máquina.

2. Abrir o Terminal e acessar a pasta do projeto `robot-web-tests`.

2. Executar o comando `pip install -r resources/dependencies/requirements.txt`.

<br  />
<br  />

# Download Driver Browser

Chromedriver: https://chromedriver.chromium.org/downloads <br />
Geckodriver:  https://github.com/mozilla/geckodriver/releases <br />
Edgedriver:   https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/

- Nome dos drivers e dos seus executáveis (os executáveis devem estar no Path da máquina):

    - Chrome      ->      chromedriver.exe
    - Firefox     ->      geckodriver.exe
    - Edge        ->      MicrosoftWebDriver.exe

<br  />
<br  />

# Comando para execução

`robot -d ./logs-v BROWSER:chrome -i name_tag tests\exemplo.robot` 

* `robot` -> comando para executar os cenários de testes.

* `-d` -> é o diretório de saída _(outputdir)_. Todas às vezes que os cenários de testes são executados são gerados arquivos de log e para manter as "boas práticas" é necessário direcionar esses arquivos para uma pasta separada.

* `./logs` -> esta é a pasta que será criada para armazenar os arquivos de log informados acima.

* `BROWSER` -> esta variável indica qual browserdriver será executado, no caso, os valores podem ser **chrome**, **firefox** ou **edge**.
  
* `-i` -> é um selecionador de tags _(include tag)_. Seleciona os casos de testes a serem executados pelo o nome da tag.

* `name_tag` -> nome da tag que será selecionada pelo o comando `-i`, assim todos os casos de testes que conter essa tag serão executados.

* `tests\` -> esta é a pasta que armazena o exemplo.robot que contém o cenário de teste a ser executado.

* `exemplo.robot` -> este é o arquivo que tem descrito o cenário de teste a ser executado.

<br  />
<br  />

# Curiosidades

* Executando o comando `robot --help` no terminal será apresentado todo CLI (Command Line - Linhas de Comando) do robot.

* Nunca ouviu falar sobre Robot Framework? [Click here](https://qaninja.academy/curso/robot-beginner/) para acessar um curso básico sobre essa ferramenta.

<br  />
<br  />

# Links de páginas sobre o Robot Framework

*  [Robot Framework](https://robotframework.org/)

*  [Robot Framework documentation](https://robotframework.org/robotframework/)

*  [Robot Framework User Guide](https://robotframework.org/robotframework/latest/RobotFrameworkUserGuide.html)

*  [Robot Framework SeleniumLibrary](https://robotframework.org/SeleniumLibrary/SeleniumLibrary.html)

* [BuiltIn](https://robotframework.org/robotframework/latest/libraries/BuiltIn.html)
> A BuiltIn é uma library padrão do Robot Framework, ela já é importada automaticamente e, portanto, suas keywords sempre estão disponíveis para serem utilizadas no projeto. 