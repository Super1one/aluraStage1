## Curso de Git e Github

## (antes de prosseguir veja SSH no GuitHub -> https://docs.github.com/pt/authentication/connecting-to-github-with-ssh)

# ----------------------------------------------------------------------------------------

## PRIMEIROS PASSOS NO GIT


git init   (cria/inicia um repositorio "git" no diretorio)
git config --global user.email "seu email"
git config --global user.name  "seu nome"

# OBS: é possível setar valores locais -> git config --local user.email "seu email"
#                                         git config --local user.name  "seu nome"

git config --list --global  (mostra dados do usuario)
git config user.name        (mostra nome de usuario)
git config user.email        mostra nome de email


git branch -M master   (renomeia a branch "main" para "master")
git remote add origin https://github.com/Super1one/aluraStage1.git (endereço do seu repositorio)
OBS: o nome "origin" é o apelido da URL do servidor remoto, pode ser outro nome (não recomendável)
OBS2: A URL pode ser de um servidor remoto (github, por exemplo) ou local (uma máquina local)

git add .  ->  Rastreia as alterações e coloca os arquivos no stage area
               É possível usar "." (todos arquivos) ou só o nome do arquivo seguido da extensão
git status
git commit -m "meu primeiro commit"    (fazer commit)
git push -u origin master


# GIT restore
git restore <arquivo>          -> para desfazer alterações (antes de colocar na stage area)
git restore --staged <arquivo> -> para desfazer alterações (já dentro da stage area)



# ----------------------------------------------------------------------------------------
# COMANDOS E ORIENTAÇÕES

# Trocando nome da branch "master" para "main" (ou vice versa)
git branch -m master main  (renomeia localmente)
git push -u origin main    (renomeia remotamente)

("origin" é um apelido local para seu repositório remoto, é mutável)
git remote remove origin (ou o apelido)

## Listar repositorios remotos
git remote -v


## Alterando o apelido do repositorio remoto (que geralmente é origin)
git remote rename <apelido>  <novo-apelido>


## clonar repositorio
git clone https://github.com/URLdoREPOSITORIO
  ou
git clone https://github.com/URLdoREPOSITORIO nomeNovaPasta
OBS: "git clone" dispensa posterior "git remote add origin https://github..."

## lista de commits
git log
git log --oneline
git log --oneline --all --graph  (mostras timelines)
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

## Fork + pull request?

## fork vs clone?
