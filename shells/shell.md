### Introdução 
 - Shell é um programa que fornece uma interface de linha de comando para o sistema operacional.
 - O Shell permite que os usuários executem comandos, scripts e programas, além de gerenciar arquivos e diretórios.
 - GNU/Bash
 - ZSH
 - DASH
 - Não existe `main` no shell
 
### Forma executar
 - `$ sh script.sh` ou `sh script.sh`
 - `$ bash script.sh` ou `bash script.sh`

### Shebang
 - `#!/bin/sh` ou `#!/usr/bin/env sh`
 - O shebang é uma linha no início de um script que indica qual interpretador deve ser usado para executar o script. 
 - Não é possível usar dois shebangs em um único arquivo shell, pois o interpretador considera apenas o primeiro shebang encontrado no início do arquivo.
 - O shebang deve ser a primeira linha do script e deve começar com `#!` seguido pelo caminho do interpretador.
 - Exemplo: `#!/bin/sh` indica que o script deve ser executado com o interpretador Bash.
 
### Variáveis
 - Usa-se `nome=valor` para criar uma variável.
 - Usa-se `${nome}` para acessar o valor da variável.

### Variáveis do Shell
 - `HOME` - Diretório inicial do usuário.
 - `SHELL` - Caminho do interpretador do shell atual.
 - `PATH` - Lista de diretórios onde o shell procura por executáveis.
 - `$?` - Código de saída do último comando executado.
 - `$$` - ID do processo do shell atual.
    - Toda execução ele cria um shell que é morto quando o script termina.
    - Util para criar arquivos/variáveis temporários.
 - `$!` - ID do último processo executado em segundo plano.
 - `$#` - Número de argumentos passados para o script.
 - `&` - Executa o comando em segundo plano.
 - `$0` - Nome do script ou comando atual.
 - Para ver todas as variáveis do shell, use o comando `set` ou `set | less`

### Argumentos
 - `$1`, `$2`, `$3`, ... - Argumentos passados para o script.
 - `$@` - Todos os argumentos passados para o script.
 - `$*` - Todos os argumentos passados para o script como uma única string.
 - `shift` - Remove o primeiro argumento da lista de argumentos.
 - `var=${nome}` ou `$(nome)`  Acessa o valor da variável `nome`.

### Operações
    - `=` - Atribuição de valor a uma variável.
    - `==` - Comparação de igualdade.
    - `!=` - Comparação de desigualdade.
    - `-eq` - Comparação de igualdade numérica.
    - `-ne` - Comparação de desigualdade num
    - `expr` - Comparação de maior que.
    - `||` - Comando lógico "ou", só executado se falhar o primeiro.
    - `&&` - Comando lógico "e", só executado se o primeiro for bem-sucedido.
