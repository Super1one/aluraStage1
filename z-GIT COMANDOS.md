## Curso de Git e Github

## Criando usuário no repositorio local

## Conta de identificação no Git (Deve ser a mesma do GitHub)
## (CRIANDO USUARIO ou MUDANDO NOMES EXISTENTES)
git init
git config --global user.email "personalEmail"
git config --global user.name  "personalName"
## Para checkar usurio e email SETADOS
git config --list --global

## ---------------------------------------

## Primeiros comandos do github

## (antes de prosseguir veja SSH no GuitHub -> https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)

## create a new repository on the command line
## (CRIANDO UM NOVO REPOSITORIO)
## OPCIONAL -> echo "# nomeRepositorioGitHub" >> README.md
git init

git branch -M master   (renomeia a branch principal para master)
git remote add origin https://github.com/Super1one/aluraStage1.git

git add .   (ou o nome dos arquivos desejados)
git status
git commit -m "first commit"    (fazer commit)
git push -u origin master

## or push an existing repository from the command line
## (PARA REPOSITORIO EXISTENTE)
git remote add origin https://github.com/Super1one/aluraStage1.git
git branch -M master
git push -u origin master

("origin" é um apelido local para seu repositório remoto, é mutável)
git remote remove origin (ou o apelido)

## Listar repositorios remotos
git remote -v

## Alterar a URL de um repositori remoto
git remote set-url origin (apelido) https://github.com/NOVA-URL

## Alterando o apelido do repositorio remoto (que geralmente é origin)
git remote rename origin novo-origin
                     |        |
##                apelido  novo-apelido

## ----------------------------------------------------

## clonar repositorio
git clone https://github.com/URLdoREPOSITORIO
OBS: "git clone" dispensa o "git remote add origin https://github..."

## lista de commits
git log
git log --oneline --all --graph --decorate (advance)

## sair do comando
letra "q"

## SOBRE os COMMITS->
Dicas para mensagens de commits -> curtas e concisas/ max char 72
...quebre linha se precisar adicionar detalhes
...use verbo no infinitivo
...evite detalhes tecnicos
... commit são úteis para sinalizar uma mudança ou um bug resolvido
...não faça commit antes de resolver bugs
...todo commit possui um ID

## SOBRE push e projetos publicos->
Projetos publicos são publicos apenas para leitura, ou seja...
...não é possível fazer push para o respositorio de outro usuário...
...sem autorização (colaboradores "ONLY").


## Downstream/Download os commits de colaboradores
Puxando commits do github...
(antes é necessário o "git remote origin https://github... " ou git clone)
git pull origin main (vai baixar os commits)

## ↑push commit ↑ vs ↓pull commit↓
git push -> envia commits
git pull -> baixar commits

## pull request?

## Fork + pull request

## fork vs clone
