## lista de commits
git log
git log --oneline --all --graph --decorate (advance)

## como desfazer um commit
git revert + codigo do "commit"   (necessário "commit" posterior para registrar a reversão)

use "git log" para ver a lista de "commits" e selecione o código do "commit" (seu id).
escreva o comando "git revert + o código do commit" e execute
OBS: é necessário fazer um novo "commit" para registrar a reversão