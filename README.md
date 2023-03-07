# Git

## Configurações

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


## Init

Inicializar repositório:
``` sh
git init
```


## Status

Visualizar o estado do repositório:
``` sh
git status
```


## Add

Adicionar arquivo ao monitoramento do Git:
``` sh
git add meu_arquivo.txt
```

Adicionar todos os arquivos ao monitoramento do Git:
``` sh
git add .
```

## Commit

Criar um commit (marcação) com uma mensagem (-m) (verificar padrões de commit):
``` sh
git commit -m "mensagem de commit"
```


## Histórico

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

Verificar o histórico com linhas de desenvolvimento:
``` sh
git log --graph
```

[Formatos de log](https://devhints.io/git-log)


## Ignorar arquivos

* Criar aquivo .gitignore
* Copiar o conteúdo do site [gitignore.io](https://www.toptal.com/developers/gitignore) de acordo com o tipo de projeto


## Repositórios remotos

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


## Clone

Clonar repositório:
``` sh
git clone caminho_ou_url_repositorio
```

Clonar repositório e renomear pasta:
``` sh
git clone caminho_ou_url_repositorio nome_pasta
```


## Push

Enviar (empurrar) arquivos para repositório:
``` sh
git push nome_repositorio nome_branch

# Exemplo:
git push origin main
```


## Pull

Trazer (puxar) arquivos do repositório remoto:
``` sh
git pull nome_repositorio nome_branch
```

Renomear repositório remoto:
``` sh
git remote rename nome_antigo novo_nome

# Exemplo:
git pull origin main
```

## Branches

Criar nova Branch:
``` sh
git branch nome_da_branch
```

Alternar entre Branches:
``` sh
git checkout nome_da_branch
```

Criar uma Branch e fazer Checkout:
``` sh
git checkout -b nome_nova_branch
```


## Merge

Trazer alterações de outra branch:

``` sh
git merge outra_branch

# Exemplo (estando na branch main trazendo alterações da branch dev):
git merge dev
```


## Rebase

Unificar branches, puxando commits para frente do branch de destino:
``` sh
git rebase outra_branch

# Exemplo (estando na branch main trazendo alterações da branch dev):
git rebase dev
```

* O merge preserva o histórico, enquanto o rebase o reescreve.
* O merge junta os trabalhos e gera um merge commit.
* O rebase aplica os commits de outra branch na branch atual.


## Desfazer alterações

Antes de adicionar os arquivos (add):
``` sh
git checkout -- nome_do_arquivo
```

Após adicionar os arquivos (add):
``` sh
git reset HEAD nome_do_arquivo
```

Após realizar o commit (cria um novo commit de revert):
``` sh
git revert hash_do_commit
```


 ## Stash 

Salvamento temporário:
``` sh
git stash
```

Listar alterações no stash:
``` sh
git stash list
```

Aplicar alterações de uma stash :
(Apply mantém a stash, necessário realizar o Drop)
``` sh
git stash apply num_da_stash

# Exemplo de número da stash 0 = stash@{0}
```

Apagar alterações de uma stash:
``` sh
git stash drop num_da_stash
```

Aplicar a última alteração adicionada à stash e removê-la:
(após isso, realizar add e commit)
``` sh
git stash pop
```


## Alternar entre commits (Checkout)

``` sh
git checkout hash_do_commit
```

Necessário criar uma nova Branch:
``` sh
git checkout -b nova_branch
```

Voltar para main:
``` sh
git checkout main
```


## Verificar diferenças (Diff)

Alterações realizadas e ainda não adicionadas (add):
``` sh
git diff
```

Verificar diferenças entre dois commits:
``` sh
git diff hash_commit_1..hash_commit_2
```


## Marcações (Releases)

Criar Tag:
``` sh
git tag -a nome_da_tag

# Exemplo:
git tag -a v0.1.0 -m "Primeira versão"
```

Listar Tags:
``` sh
git tag
```

Enviar Tag:
``` sh
git push nome_repositorio nome_da_tag

# Exemplo:
git push origin v0.1.0
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


---


## [Visualizador Git](https://git-school.github.io/visualizing-git/)  
