# Curso Git em 3 Dias
## Autor: Andre Iacono
## Plataforma: Udemy
## Inicio: 15/06/2023
## Recurso: [git.zip](git.zip)

# Inicializando seu primeiro repositório
```
$ git init
```
* Ao inicialiar o repositorio os arquivos existentes passaram a ser controlado as suas versões.

# Status
## Untracked
* Arquivos que ainda não fazem parte do controle de versão.Se houver alguma alteração nos arquivos não vai tirar o snapshot, ou seja tirar copia desses arquivos.

```
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        git.zip
        hamburger.jpg
        index.html
        tablesetting.jpg
        tablesetting2.jpg

```

## Tracked
* nesse caso ele tira o snapshot do arquivo modificado (commit) para criar uma nova versão.
* Pode ser feito por arquivo ou por todos os arquivos no diretorio.

### Por arquivo
```
$ git add index.html
git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        git.zip
        hamburger.jpg
        tablesetting.jpg
        tablesetting2.jpg

```
* Nesse ponrto o arquivo index.html esta pronto para fazer o commit (snapshot) e caso queira retornar o arquivo para unstage basta usar o comando:m `git rm --cached <file>..`

```
$ git rm --cached index.html
rm 'index.html'
```
```
$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md
        git.zip
        hamburger.jpg
        index.html
        tablesetting.jpg
        tablesetting2.jpg

nothing added to commit but untracked files present (use "git add" to track)

```

### Todos no diretório

Pode usar dois comando `$ git add --all` ou `$ git add .` este ultimo o mais usado.

```
$ git add .
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it
```

```
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   README.md
        new file:   git.zip
        new file:   hamburger.jpg
        new file:   index.html
        new file:   tablesetting.jpg
        new file:   tablesetting2.jpg

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

```
* Nesse estagio todos os arquivos estão prontos para o commit

# Commit

Verifica todos os arquivos que estão no status staged e vai criar uma versão desses arquivos, vai tirar um snapshot.

```
$ git commit -m "Primeiro commit - Todos arquivos inclusos"
[main (root-commit) 2fd06bc] Primeiro commit - Todos arquivos inclusos
 6 files changed, 195 insertions(+)
 create mode 100644 README.md
 create mode 100644 git.zip
 create mode 100644 hamburger.jpg
 create mode 100644 index.html
 create mode 100644 tablesetting.jpg
 create mode 100644 tablesetting2.jpg
```

```

```
