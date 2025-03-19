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

- Usar o ponto de interrogação ```?```: O ponto de interrogação ```?``` substitui um único caractere:

    ```gitignore
    file?.txt  # Ignora arquivos como file1.txt, fileA.txt, etc.

- Usar colchetes ```[]```: Colchetes podem ser usados para definir uma correspondência para um conjunto de caracteres:

    ```gitignore
    file[123].txt  # Ignora file1.txt, file2.txt e file3.txt


### 3. Ignorar Arquivos com Padrões Relativos

- **Ignorar arquivos em um diretório específico:** Você pode especificar um caminho relativo para ignorar arquivos em um subdiretório:

    ```gitignore
    /log/*.log  # Ignora todos os arquivos .log dentro da pasta log/

### 4. Exceções de Ignoramento

- **Negar um arquivo ignorado:** Se você deseja ignorar um diretório inteiro, mas manter um arquivo ou subdiretório específico dentro dele, você pode usar ```!``` para negar um padrão de ignorar:

    ```gitignore
    logs/*
    !logs/keep.log  # Ignora todos os arquivos na pasta logs, mas mantém logs/keep.log

### 5. Comentários
Comentários: Para adicionar um comentário ao arquivo ```.gitignore```, basta usar o símbolo ```#```. Tudo após o ```#``` em uma linha será ignorado:
    
    # Ignorar arquivos de log
    *.log

### 6. Ignorar Arquivos de Backup

- **Arquivos de backup e temporários:** Frequentemente, você pode querer ignorar arquivos temporários criados por editores ou ferramentas de sistema:

    ```gitignore
    *~           # Arquivos de backup do editor (ex: arquivo~)
    *.swp        # Arquivos temporários do Vim (ex: .file.swp)

### 7. Ignorar Arquivos de Sistema

- **Arquivos específicos do sistema operacional:** Alguns sistemas operacionais criam arquivos ocultos ou de sistema que você pode querer ignorar:

    ```gitignore
    .DS_Store    # Arquivos de sistema do macOS
    Thumbs.db    # Arquivos de miniaturas do Windows

### 8. Ignorar Arquivos de Configuração de IDEs

- **Ignorar arquivos de configuração de editores/IDEs:** É comum querer ignorar os arquivos de configuração de IDEs e editores de código, pois esses arquivos são específicos para o ambiente de desenvolvimento de cada usuário:

    ```gitignore
    .idea/       # Ignora a pasta do IntelliJ IDEA
    .vscode/     # Ignora a pasta do Visual Studio Code
    ./bin        # Ignora a pasta do Visual Studio Community

### 9. Ignorar Arquivos de Dependências

- **Ignorar diretórios de dependências:** Dependências de pacotes ou bibliotecas frequentemente são ignoradas porque podem ser geradas novamente a partir do código-fonte:

    ```gitignore
    node_modules/  # Ignora dependências do Node.js
    vendor/        # Ignora dependências do PHP (composer)

### 10. Ignorar Arquivos Com Extensões Específicas
- **Ignorar arquivos com uma determinada extensão:** Arquivos com extensões específicas podem ser ignorados com o uso de padrões:

    ```gitignore
    *.bak  # Ignora arquivos de backup
    *.tmp  # Ignora arquivos temporários

### 11. Ignorar Arquivos no Nível Global

- **Arquivos de configuração global ```(~/.gitignore_global)```**: Você pode configurar um arquivo ```.gitignore_global``` para definir padrões de ignorância que se aplicam a todos os repositórios Git no seu sistema. Para isso, adicione o seguinte ao seu Git:

    ```bash
    git config --global core.excludesfile ~/.gitignore_global

### 12. Ignorar Arquivos na Raiz do Repositório

- **Ignorar arquivos apenas na raiz:** Para ignorar arquivos na raiz do repositório sem afetar arquivos em subdiretórios, você pode usar ```/``` no início do padrão:

    ```gitignore
    /arquivo.txt  # Ignora o arquivo.txt na raiz do repositório