# usar_git

Comando do Git

Projeto do zero
============================
md nome-da-pasta // criar um pasta <br/>
cd nome-da-pasta // dentro da pasta <br/>
git init // inicia git

Ver status e lista de arquivos
============================
git ls-files // lista os arquivos  <br/>
git status // ver o status dos arquivos

Adição e Commits
=============================
git add nome-do-arquivo // adiciona arquivo novos e alterados para o próximo commit <br/>
git add -i // Controle de adição interativo <br/>
git commit -m "Mensagem de teste" // dá o nome da commit <br/>
git commit -a -m "Mensagem de teste" // dá o nome da commit e adiciona arquivo alterados e removidos

Configuração de usuário e email
============================
git config user.name "Nome" // Configura o nome do usuário <br/>
git config user.email "email@email.com" // Configura o e-mail do usuário, pode usar o --global para definir o usuário como padrão <br/>
git config --global user.name "Nome do usuário" // Configura o nome do usuário e definir como padrão para outros projetos tbm. <br/>
git config --global user.email "email@email.com" //Configura o e-mail do usuário e definir o usuário como padrão para outros projetos tbm.

Logs e ver alterações
=============================
git log // Ver log dos commits <br/>
git whatchanged // detalha mostrando quais arquivos foram alterados // tecla "q", para sair <br/>
git whatchanged -p // detalha em que parte do arquivo foi alterado // tecla "q", para sair

Criar repositorio remoto e atualizar arquivos
=============================
git remote // consulta os repositorios remotos existentes na pasta <br/>
git remote -v // verifica o endereço do repositório remoto <br/>
git remote add origin url-do-git // adicionar um repositório remoto, neste caso com o nome de origin <br/>
git push origin master // envia para o repositorio remoto "origin" os arquivos na branch "master"
git push -u origin master // envia para o repositorio remoto "origin" os arquivos na branch "master" -u //atrela a branch remota à local, assim não é necessário passar a origem e a branch, ficando somente: git push, para as próximas

Copia um repositório do Git
=============================
git clone link-do-git //copia o repositorio na máquina local

Adicionar colaborador
=============================
Vá em setting > Collaborators > adiciona o user > Add Collaborator

Boas práticas
============================

git branch // verifica as branch <br/>
git checkout -b desenvolvimento // cria a branch desenvolvimento e altera para ela <br/>
git add nome-arquivo nome-arquivo  // adiciona o arquivo para o commit, pode adicionar mais de um arquivo separando por espaço os nomes. <br/>
git commit -m "texto do commit" // envia o commit <br/>
git checkout master // muda para a master <br/>
git pull //Verifica o estado o repositorio remoto (master) <br/>
git rebase master desenvolvimento  // tras os arquivos da master para o desenvolvimento  <br/>
git checkout master // mudar para a master <br/>
git merge desenvolvimento // Unir o desenvolvimento para a master <br/>
git push // envia para o repositorio

Em caso de conflito no git rebase master desenvolvimento <br/>
Arruma o conflito depois adicionar e manda continuar o rebase <br/>
git add nome-do-arquivo  <br/>
git rebase --continue <br/>


Criando alias
==========================

!git checkout master && git  pull && git checkout desenvolvimento && git rebase master && git checkout master && git merge desenvolvimento && git push



