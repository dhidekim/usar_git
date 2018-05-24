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

Adi��o e Commits
=============================
git add nome-do-arquivo // adiciona arquivo novos e alterados para o pr�ximo commit
git add -i // Controle de adi��o interativo
git commit -m "Mensagem de teste" // d� o nome da commit
git commit -a -m "Mensagem de teste" // d� o nome da commit e adiciona arquivo alterados e removidos

Configura��o de usu�rio e email
============================
git config user.name "Nome" // Configura o nome do usu�rio
git config user.email "email@email.com" // Configura o e-mail do usu�rio, pode usar o --global para definir o usu�rio como padr�o
git config --global user.name "Nome do usu�rio" // Configura o nome do usu�rio e definir como padr�o para outros projetos tbm.
git config --global user.email "email@email.com" //Configura o e-mail do usu�rio e definir o usu�rio como padr�o para outros projetos tbm.

Logs e ver altera��es
=============================
git log // Ver log dos commits
git whatchanged // detalha mostrando quais arquivos foram alterados // tecla "q", para sair
git whatchanged -p // detalha em que parte do arquivo foi alterado // tecla "q", para sair

Criar repositorio remoto e atualizar arquivos
=============================
git remote // consulta os repositorios remotos existentes na pasta
git remote add origin url-do-git // adicionar um reposit�rio remoto, neste caso com o nome de origin
git push origin master // envia para o repositorio remoto "origin" os arquivos na branch "master"



Boas pr�ticas
============================

git branch // verifica as branch
git checkout -b desenvolvimento // cria a branch desenvolvimento e altera para ela
git add nome-arquivo nome-arquivo  // adiciona o arquivo para o commit, pode adicionar mais de um arquivo separando por espa�o os nomes.
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



