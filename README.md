# COMANDOS GIT

#VERSIONANDO PROJETO INICIAL

git init 

git add .

git commit -m "mensagem"

git branch -M main

git remote add origin < chave SSH >

git push -u origin main 

#COMANDOS GIT

.gitignore >> arquivo que indica o que nao deve ser salvo pelo git salvo na pasta principal do projeto   

git status >> verificar o status do projeto

git add . >> enviar todos os arquivos para a area de stage

code . >> abrir o vscode

git diff "nomeDoArquivo.extensao" >> mostra a diferença entre arquivos modificados

git checkout "codigoDoCommit">> modificar temporariamente os arquivos do projeto ao estado de um commit ou branch fornecido [volta o projeto no codigoDoCommit] ::undo::

git checkout main >> volta o commit para a ultima versão [original]

git checkout HEAD~1 >> HEAD~N >> referencia a N versao de um commit 				OBS::: geralmente nao se modifica os arquivos com checkout

git reset >> tira os arquivos da area de stage

git clean -df

git checkout -- . >> checkout para limpar modificações

# RESOLVENDO PROBLEMAS BASICOS

git status>> git reset>> remover arquivos da area de stage

git status>> git reset>> git clean -df>> git checkout -- .>>desfazer modificações nao salvas [voltar o projeto no ultimo commit]

git status>> git reset --soft HEAD~1>> desfazer o ultimo commit sem desfazer as modificações nos arquivos

git status>> git reset --hard "codigoDoCommit">> deletar commits e modificações nos arquivos 

git status>> git pull origin main>> atualizar o repositorio local em relação ao remoto

git pull origin main>> resolver push rejeitado devido ao historico do projeto local diferente do remoto [gera um commit de merge adicional]

git push -f>> sobrescrever historico no github		OBS:::ação destrutiva

git remote set-url origin "sshDoRepositorio">> apontar projeto para outro repositorio remoto

#REMOVENDO ARQUIVOS DO GITIGNORE

git config --global core.excludesfile ~/.gitignore

git rm -r --cached PATH_NAME

#RESOLVENDO CONFLITOS [historicos diferentes em um mesmo arquivo]
1 - analisar o codigo fonte
2 - fazer edições necessarias
3 - fazer um novo commit


#EDITOR VIM 

i>> habilitar edição
<esc> >> :wq >> <enter> >> sair do VIM salvando alterações
<esc> >> :q! >> <enter> >> sair do VIM descartando alterações

