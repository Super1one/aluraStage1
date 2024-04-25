## lista de commits
git log
git log --oneline --all --graph --decorate (advance)
git log -p   (detalhes)

------------------------------------------------------
# REVERTER ou APAGAR ou MODIFICAR UM "commit"

## como desfazer um commit
git revert + codigo do "commit"   (necessário "commit" posterior para registrar a reversão)

use "git log" para ver a lista de "commits" e selecione o código do "commit" (hash/id).
escreva o comando "git revert + o código do commit" e execute
OBS: é necessário fazer um n'ovo "commit" para registrar a reversão

## excluir/apagar commits
# OBS: o comando reset deve ser aplicado ao ID do "commit" anterior ao "commit" a ser apagado
# DICA -> reset = desfazer 1 passo anterior
git reset + "id do commit"
git reset --hard + "id do commit"

## modificar  DADOS de 1 commit (recomendável somente antes de algum PUSH)
## "--amend" -> efeitos sobre o ultimo "commit"
git commit --amend                     (altera o ultimo commit)
git commit --amend -m "nova mensagem"  (altera a mensagem do ultimo commit)



## VIAJANDO OU RETROCEDENDO ENTRE OS COMMIT
Navegamos entre commits da mesma forma que navegamos entre branch

use "git log --oneline" para ver os hash/id resumidos dos commits

selecione o hash do commit para qual deseja navegar e execute:
git checkout <commit hash>

OBS: quando vamos para um commit, estamos no LIMBO, ou seja, numa area desvinculada de tudo
Não estamos numa branch ou timeline nenhuma
Para continuar a partir do commit acessado, é necessário criar uma nova branch

↓VEJA o exemplo↓


git checkout 2b27fd9
git checkout -b <nome da branch>



----------------------------------------------------------------------

## GIT STASH / SAVE TEMPORARIO
git add .
git status
git stash -> save temporario

git stash list -> listar saves temporarios

exemplo de stash -> stash@{0}
                           |
                           número da stash

git stash apply numeroStash -> aplica o save temporario (stash)
git stash drop  numeroStash -> deleta o save temporario (stash)

git stash pop -> aplica e elimina o ultimo save temporario (stash)
  É bem utel para lidar apenas com uma stash por vez


----------------------------------------------------------------------

# GIT DIFF /VENDO ALTERAÇÕES


git diff -> mostra todas alterações que ainda não foram para "STAGE"
git diff <commit/hash A>..<commit/hash B> -> mostra as alterações de um commit "A" até um commit "B"


----------------------------------------------------------------------

# TAGs & RELEASE
# Se complementam/ não são sinonimos

Primeiro navega até o commit desejado (caso não seja o current)

git tag -a <nome> -m <msg>    ->  cria um release/entregavel do codigo
OBS: geralmente o nome da tag é algo parecido como  <v1.0.1> e a mensagem é obrigatoria
OBS2: essa versão é aparte do desenvolvimento e imutável, pode ser enviado por PUSH
OBS3: apos o PUSH, é acessível no github em RELEASE

A tag é uma forma que de você marcar seu commit (versão do código) para enviar para o github.
No github, é possível transformar essa tag em um RELEASE (versão entregavel e baixavel)



----------------------------------------------------------------------

# DELETE/DROP branch

git branch -d <nome/branch>