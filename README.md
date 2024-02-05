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

## Ramificações:
A ramificação que contém a versão do código principal e que o cliente vai utilizar após alterações estáveis, se chama main/master. 

A partir da branch principal, você pode criar novas pra ir fazendo alterações, pegando uma cópia da versão principal, e após isso, você pode passar as alterações pra branch principal, num processo chamado merge.

# Entre ramificações:
* Mostra a branch atual:
    * 'git branch'
      
* Criar branchs:
    * 'git branch ___ '  -> Passando um nome como paramêtro você cria uma nova branch.
    * 'git checkout -b ___ '   -> Cria branch nova a partir da branch antiga e já muda para ela.
      
* Vai para a branch passada como paramêtro:
    * 'git checkout ____ '
      
* Para passar alterações feitas nas outras branchs para outras ramificações:
    * Dá git checkout para a branch que vai receber a mescla
    * 'git merge ___ ', passando o nome da branch que vai ser mesclada.

## Outras coisas mais específicas:
* Retorna a branch onde você está e se tem algo para commitar:
    * 'git status'
      
* Retorna histórico de commits, incluindo o hash, que pode ser usado para voltar para aquele commit específico:
    * 'git log'
      
* Mostra as diferenças do arquivo atual para o último commit:
    * 'git diff'
      
* Restaura arquivo para o deixar identico ao último commit: 
    * 'git restore ___ '  -> passar nome do arquivo


# Repositório remoto:
Já com um repositório criado no github:

* Enviar para repositório remoto:
    * 'git remote add origin ___ '  -> passando link do repositório
    * 'git push origin ___ ' -> nome da branch

* Puxa arquivos do repositório remoto para o local:
    * 'git pull origin ___ '  -> nome da branch

* Traz as alterações que foram feitas no repositório remoto em relação ao repositório local:
    * 'git fetch' 
