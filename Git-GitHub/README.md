# Git e GitHub

### Capacitação resumida em Git e GitHub

## Introdução

Logo após criar uma conta no Git-Hub você pode ter um pouco de dificuldade pra se familiarizar com essa ferramenta, porém você ficaria impressionado com quantas funcionalidades são possíveis aqui.

## Repositórios

Ao criar um repositório, podemos armazenar diversos tipos de arquivos de código e versioná-los usando os conceitos de *branchs* do Git

## Git

O Git é uma ferramenta que permite controle do versionamento do código e organização em repositórios, sejam eles remotos (Git-Hub, Git-Lab) ou locais

É assim que se cria um repositório

    # Digite isso no prompt de comando com o git instalado
    
    # Cria o repositório
    git init

    # Adiciona todos os arquivos da pasta atual para a área de confirmação
    git add * 

    # Cria um commit com uma mensagem
    git commit -m "início"

    # Renomeia a branch selecionada (geralmente master) para main
    git branch -m main

    # Seleciona o repositório remoto
    git remote add main https://github.com/ThiagoSousa81/Server-Express.git

    # Faz o primeiro push
    git push --set-upstream main main

    # Baixar atualizações do remoto
    git pull

    # Enviar do local para remoto
    git push


## Readme

O `README.md` é um tipo de arquivo especial para documentar dados dos repositórios do Git-Hub. Ele utiliza uma linguagem de marcação chamada Markdown.

Todos os exemplos de código Markdown presente em repositórios do Git-Hub são abertos. São bem amplas as atividades que podem ser feitas com ele, mas é ideal para ser usado em documentação de projetos.

## Pull-Requests

Um `Pull-Request` no Git-Hub é uma contribuição registrada em um repositório de outra pessoa.

Para criar um `Pull-Request` você pode fazer o seguinte:

1. Vá no repositório que quer editar o código e clique no botão [`Fork`](https://github.com/ThiagoSousa81/Server-Express/fork)
2. Prossiga usando as instruções para realizar o fork do repositório
3. Com o repositório na sua conta, faça as alterações, registre com alguns commits e clique no botão **Contribute** e **Open Pull-Request**
4. Ao abrir o Pull-Request poderá informar o título dela e dados das suas alterações usando a linguagem Markdown. 
5. Após terminar se não houver conflitos, clique em Create Pull-Request

Sua `Pull-Request` já foi criada. Só falta esperar o dono do repositório revisar e fazer Merge (mesclar as alterações)

## Codespaces

O **Git-Hub Codespace** é uma ferramenta que permite trabalhos detalhados no projeto utilizando um Visual Studio Code numa máquina do Git-Hub. 

> Isso pode gastar uma pequena cota de processamento na sua conta mas não é nada com que deva se preocupar. 

1. Em um repositório seu, clique em Code e em Codespaces
2. Clique em Create Codespace on main
3. Ao abrir o painel com o Visual Studio Code, baixe as extensões e faça as configurações necessárias
4. Faça testes e depuração em seu projeto
5. Após isso é preciso desligar a Codespace. Vá no seu repositório, na mesma área onde criou a Codespace e desligue-a

Pronto, agora você sabe como usar o GitHub Codespace

## Workflows

Um workflow (fluxo de trabalho) é uma forma de realizar automações no Git-Hub. Ele pode ser usado para:

- CI/CD Integração Contínua e Deploy Contínuo
- Testes de validação
- Gerar builds de aplicações
- Automações diversas

A linguagem básica de configuração de um arquivo de Workflow no Git-Hub é YAML. No repositório abaixo temos alguns exemplos

> Vale resaltar que o Git-Hub fornece uma cota gratuita de 2000 minutos de workflow, sendo renovados a cada mês por conta

[![YAML-Templates](https://github-readme-stats.vercel.app/api/pin/?username=ThiagoSousa81&repo=YAML-Templates&theme=chartreuse-dark&show_owner=true&PAT_1=thiagosousa81)](https://github.com/ThiagoSousa81/YAML-Templates)