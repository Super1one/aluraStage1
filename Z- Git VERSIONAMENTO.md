## lista de commits
git log
git log --oneline --all --graph --decorate (advance)

------------------------------------------------------
# REVERTER ou APAGAR ou MODIFICAR UM "commit"

## como desfazer um commit
git revert + codigo do "commit"   (necessário "commit" posterior para registrar a reversão)

use "git log" para ver a lista de "commits" e selecione o código do "commit" (seu id).
escreva o comando "git revert + o código do commit" e execute
OBS: é necessário fazer um novo "commit" para registrar a reversão

## excluir/apagar commits
# OBS: o comando reset deve ser aplicado ao ID do "commit" anterior ao "commit" a ser apagado
# DICA -> reset = desfazer 1 passo anterior
git reset + "id do commit"
git reset --hard + "id do commit"

## modificar  DADOS de 1 commit (recomendável somente antes de algum PUSH)
## "--amend" -> efeitos sobre o ultimo "commit"
git commit --amend                     (altera o ultimo commit)
git commit --amend -m "nova mensagem"  (altera a mensagem do ultimo commit)




