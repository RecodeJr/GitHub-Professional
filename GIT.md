# Guia de `.gitignore`

O arquivo `.gitignore` é utilizado para informar ao Git quais arquivos ou diretórios não devem ser rastreados pelo sistema de controle de versão. Este guia explica como utilizar o arquivo `.gitignore` para configurar e ignorar arquivos ou diretórios indesejados em seu repositório Git.

## Funcionalidades e Sintaxes do `.gitignore`

### 1. Ignorar Arquivos e Diretórios

- **Ignorar arquivos específicos**: 
  Para ignorar um arquivo específico, basta escrever o nome do arquivo:

  ```gitignore
  arquivo.txt

- **Ignorar diretórios:** Para ignorar um diretório, adicione uma barra (/) no final do nome do diretório:

    ```gitignore
    pasta/

### 2. Ignorar Arquivos ou Diretórios com Padrões

- Usar caracteres curingas ```*```: O asterisco ```*``` pode ser usado para corresponder a qualquer sequência de caracteres:

    ```gitignore
    *.log     # Ignora todos os arquivos .log
    *.txt     # Ignora todos os arquivos .txt