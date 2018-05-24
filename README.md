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
git log // Ver log dos commits // tecla "q", para sair <br/>
git whatchanged // detalha mostrando quais arquivos foram alterados // tecla "q", para sair <br/>
git whatchanged -p // detalha em que parte do arquivo foi alterado // tecla "q", para sair

Criar repositório remoto e atualizar arquivos
=============================
git remote // consulta os repositorios remotos existentes na pasta <br/>
git remote -v // verifica o endereço do repositório remoto <br/>
git remote add origin url-do-git // adicionar um repositório remoto, neste caso com o nome de origin <br/>
git push origin master // envia para o repositorio remoto "origin" os arquivos na branch "master"
git push -u origin master // envia para o repositorio remoto "origin" os arquivos na branch "master" -u //vincula a branch remota à local, assim não é necessário passar a origem e a branch, ficando somente: git push, para as próximas

Copia um repositório do Git
=============================
git clone link-do-git //copia o repositorio na máquina local

Adicionar colaborador
=============================
Vá em setting > Collaborators > adiciona o user > Add Collaborator

Branch
=============================
git branch // mostra as branch locais <br/>
git branch -r // mostra as branch remotas <br/>
git branch -a // mostra as branch remotas e locais <br/>
git branch -t design origin/design // Cria a branch local(design) e vinculada a branch remota origin/design <br/>
git branch -d  // Apaga uma branch, mas se não estiver sincronizada utilizada -D

git branch design // cria a branch design<br/>
git checkout design // mudar para a design <br/>
git checkout -b desenvolvimento // cria a branch desenvolvimento e altera para ela <br/>
git checkout -t origin/design // Cria a branch design do repositório remoto com o mesmo nome, mudar para ela e cria um link para as branchs.

Removendo Branch remota
================================
git push -d origin design // Remove Branch remota design<br/>
git push origin :design // Remove Branch remota design

Verificando atualizações do repositório
================================
git fetch origin // verifica todas as atualizações realizadas no repositório origin

Boas práticas
============================
git branch // mostra as branch <br/>
git checkout -b desenvolvimento // cria a branch desenvolvimento e altera para ela <br/>
git add nome-arquivo nome-arquivo  // adiciona o arquivo para o commit, pode adicionar mais de um arquivo separando por espaço os nomes. <br/>
git commit -m "texto do commit" // envia o commit <br/>
git checkout master // muda para a master <br/>
git pull //Verifica o estado o repositorio remoto (master) <br/>
git rebase master desenvolvimento  // tras os arquivos da master para o desenvolvimento  <br/>
-----------------------------
- Se encontrar algum conflito no git rebase master desenvolvimento <br/>
- Arruma o conflito, depois adicionar e manda continuar o rebase <br/>
git add nome-do-arquivo  <br/>
git rebase --continue // Continua o rebase, que foi parado devido o conflito <br/>
-----------------------------
git checkout master // mudar para a master <br/>
git merge desenvolvimento // Unir o desenvolvimento para a master <br/>
git push // envia para o repositorio

Identificando conflitos
==================================
O Git utiliza os caracteres >, < e =. Entre o < e o = fica o conteúdo antigo e entre o > e = fica o conteúdo novo.

Rebase
==================================
git rebase --continue // Continua a partir do ponto de conflito<br/>
git rebase --abort // Aborta e volta ao estado original<br/>
git rebase --skip // Alterações sejam descartadas.<br/>

Desfazer alterações
==================================
git checkout nome-do-arquivo // Volta o arquivo para o estado original antes de ser modificado.<br/>
git reset HEAD nome-do-arquivo //Volta o arquivos se ele já foi dado o git add, estado index.<br/>
git reset codigo-do-commit // Desfaz o commit no log, mas não altera o arquivo.<br/>
git revert codigo-do-commit //Desfaz um commit antigo, reverte as alterações e da o direito de dar um novo nome do commit com a alteração desfeita

Usar área temporário
==================================
git stash // coloca em area temporária<br/>
git stash list // lista áreas temporárias guardadas<br/>
git stash pop // retorna para o último stash<br/>
git stash apply stash@{0} // retorna para o stash no número determinado<br/>
git stash drop // apaga os stash

Localizar um commit
===================================
git bisect start // Inicia um bisect<br/>
git bisect bad HEAD // Informa que o HEAD é ruim<br/>
git bisect good codigo-do-commit good // informar que o commit é bom<br/>
-Vai informando se good e bad, para dizer se está no caminho certo ou errado para o Git encontrar o commit que está procurando.


Para minimizar conflitos
==================================
- Commits com pouco conteúdo<br/>
- Sincronização (pull) frequente do repositório remoto<br/>
- Ferramentas visuais de merge http://kdiff3.sourceforge.net/, http://meldmerge.org/

Criando alias
==========================

!git checkout master && git  pull && git checkout desenvolvimento && git rebase master && git checkout master && git merge desenvolvimento && git push



