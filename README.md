# Git

Configurações globais:
``` sh
git config --global user.name "Nome do autor"
git config --global user.email "email.do.autor@exemplo.com"
```

Configurações para um projeto específico:
``` sh
git config --local user.name "Nome do autor"
git config --local user.email "email.do.autor@exemplo.com"
```

Inicializar repositório:
``` sh
git init
```

Visualizar o estado do repositório:
``` sh
git status
```

Adicionar arquivo ao monitoramento do Git:
``` sh
git add meu_arquivo.txt
```

Adicionar todos os arquivos ao monitoramento do Git:
``` sh
git add .
```

Criar um commit (marcação) com uma mensagem (-m) (verificar padrões de commit):
``` sh
git commit -m "mensagem de commit"
```

Verificar o histórico de commits:
``` sh
git log
```

Verificar o histórico de commits (resumido):
``` sh
git log --oneline
```

Verificar o histórico de commits (com as alterações):
``` sh
git log -p
```

[Formatos de log](https://devhints.io/git-log)

Ignorar arquivos com .gitignore:
* Criar aquivo .gitignore
* Copiar o conteúdo do site [gitignore.io](https://www.toptal.com/developers/gitignore) de acordo com o tipo de projeto


Repositórios remotos

Criar repositório para armazenamento (servidor):
``` sh
git init --bare
```

Listar repositórios remotos:
``` sh
git remote
```

Adicionar repositório remoto:
(por padrão, o nome do repositório é origin e o caminho a url)
``` sh
git remote add nome_repositorio caminho_ou_url_repositorio
```

Verificar endereço dos repositórios:
``` sh
git remote -v
```

Clonar repositório:
``` sh
git clone caminho_ou_url_repositorio
```

Clonar repositório e renomear pasta:
``` sh
git clone caminho_ou_url_repositorio nome_pasta
```

Enviar (empurrar) arquivos para repositório:
``` sh
git push nome_repositorio nome_branch

# Exemplo:
git push origin main
```

Trazer (puxar) arquivos do repositório remoto:
``` sh
git pull nome_repositorio nome_branch
```

Renomear repositório remoto
``` sh
git remote rename nome_antigo novo_nome
```

## Padrões de commit

- `feat`- **novo recurso** 

- `fix` - **solucionando um problema**

- `docs` - **mudanças na documentação**

- `test` - **alterações em testes**

- `build` - **arquivos de build e dependências**

- `perf` - **performance**

- `style` - **formatações de código**

- `refactor` - **refatorações que não alterem sua funcionalidade**

- `chore` - **atualizações de tarefas**

- `ci` - **integração contínua**


[Visualizador Git](https://git-school.github.io/visualizing-git/)  
