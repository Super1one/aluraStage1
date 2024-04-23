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

## create a new repository on the command line
## (CRIANDO UM NOVO REPOSITORIO)
echo "# nomeRepositorioGitHub" >> README.md
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/Super1one/aluraStage1.git
git push -u origin main

## or push an existing repository from the command line
## (PARA REPOSITORIO EXISTENTE)
git remote add origin https://github.com/Super1one/aluraStage1.git
git branch -M main
git push -u origin main