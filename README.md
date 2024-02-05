# Git-MaterialDeEstudo

# Material de estudo de Git e Github.

Git: software de controle de versão distribuído. 

Um commit no git salva na sua máquina um repositório local com as alterações feitas, o push envia pro repositório remoto, o github.

## Vantagens: 
* Controle de histórico
* Trabalho em equipe
* Ramificação do projeto
* Segurança e Organização. 



# Na prática: 
Com o git instalado, e o projeto aberto no editor de código:

* Para iniciar o git, digitar no terminal:
    * 'git init'
      
* Para enviar as alterações para o histórico/"commitar":
    * 'git add .' ou 'git add nome_do_arquivo '   -> pega os arquivos alterados e adiciona num estágio para commit.
      
* Com as alterações preparadas, para "commitar": 
    * 'git commit -m "mensagem_de_commit"
      
* Para modificar o commit mais recente:
    * 'git commit --amend -m "mensagem_de_commit" '  

## Ramificações/Branchs:
A ramificação que contém a versão do código principal e que o cliente vai utilizar após alterações estáveis, se chama main/master. 

A partir da branch principal, você pode criar novas pra ir fazendo alterações, pegando uma cópia da versão principal, e após isso, você pode passar as alterações pra branch principal, num processo chamado merge.

# Entre ramificações:
* Mostra a branch atual:
    * 'git branch'
      
* Criar branchs:
    * 'git branch nome_da_branch '  -> Passando um nome como paramêtro você cria uma nova branch.
    * 'git checkout -b nome_da_branch '   -> Cria branch nova a partir da branch antiga e já muda para ela.
      
* Ur para outra branch:
    * 'git checkout nome_da_branch '
      
* Para passar alterações feitas nas outras branchs para outras ramificações:
    * Dá git checkout para a branch que vai receber a mescla
    * 'git merge nome_da_branch ', passando o nome da branch que vai ser mesclada.

## Outras coisas:
* Retorna a branch onde você está e se tem algo para commitar:
    * 'git status'
      
* Retorna histórico de commits:
    * 'git log'
      
* Mostra as diferenças do arquivo atual para o último commit:
    * 'git diff'
      
* Restaura arquivo para o deixar identico ao último commit: 
    * 'git restore nome_do_arquivo '  


# Repositório remoto:
Já com um repositório criado no github:

* Enviar para repositório remoto:
    * 'git remote add origin link_do_repositorio ' 
    * 'git push origin nome_da_branch ' 

* Puxa arquivos do repositório remoto para o local:
    * 'git pull origin nome_da_branch '
      
* Traz as alterações que foram feitas no repositório remoto em relação ao repositório local:
    * 'git fetch' 
