# usar_git

Comando do Git


Projeto do zero
============================
md nome-da-pasta // criar um pasta
cd nome-da-pasta // dentro da pasta
git init // inicia git

Ver status e lista de arquivos
============================
git ls-files // lista os arquivos 
git status // ver o status dos arquivos

Adição e Commits
=============================
git add nome-do-arquivo // adiciona arquivo novos e alterados para o próximo commit
git add -i // Controle de adição interativo
git commit -m "Mensagem de teste" // dá o nome da commit
git commit -a -m "Mensagem de teste" // dá o nome da commit e adiciona arquivo alterados e removidos

Configuração de usuário e email
============================
git config user.name "Nome" // Configura o nome do usuário
git config user.email "email@email.com" // Configura o e-mail do usuário, pode usar o --global para definir o usuário como padrão
git config --global user.name "Nome do usuário" // Configura o nome do usuário e definir como padrão para outros projetos tbm.
git config --global user.email "email@email.com" //Configura o e-mail do usuário e definir o usuário como padrão para outros projetos tbm.

Logs e ver alterações
=============================
git log // Ver log dos commits
git whatchanged // detalha mostrando quais arquivos foram alterados // tecla "q", para sair
git whatchanged -p // detalha em que parte do arquivo foi alterado // tecla "q", para sair

Criar repositorio remoto e atualizar arquivos
=============================
git remote // consulta os repositorios remotos existentes na pasta
git remote add origin url-do-git // adicionar um repositório remoto, neste caso com o nome de origin
git push origin master // envia para o repositorio remoto "origin" os arquivos na branch "master"



Boas práticas
============================

git branch // verifica as branch
git checkout -b desenvolvimento // cria a branch desenvolvimento e altera para ela
git add nome-arquivo nome-arquivo  // adiciona o arquivo para o commit, pode adicionar mais de um arquivo separando por espaço os nomes.
git commit -m "texto do commit" // envia o commit
git checkout master // muda para a master
git pull //Verifica o estado o repositorio remoto (master)
git rebase master desenvolvimento  // tras os arquivos da master para o desenvolvimento 
git checkout master // mudar para a master
git merge desenvolvimento // Unir o desenvolvimento para a master
git push // envia para o repositorio

Em caso de conflito no git rebase master desenvolvimento
Arruma o conflito depois adicionar e manda continuar o rebase
git add nome-do-arquivo 
git rebase --continue


Criando alias
==========================


!git checkout master && git  pull && git checkout desenvolvimento && git rebase master && git checkout master && git merge desenvolvimento && git push



