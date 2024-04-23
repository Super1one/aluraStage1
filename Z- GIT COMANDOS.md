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
echo "# nomeRepositorioGitHub" >> README.md
git init

git add .   (ou o nome dos arquivos desejados)
git status
git commit -m "first commit"    (fazer commit)

git branch -M master   (renomeia a branch principal para master)
git remote add origin https://github.com/Super1one/aluraStage1.git
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

