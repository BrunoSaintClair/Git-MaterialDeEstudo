# Git-MaterialDeEstudo

# Material de estudo de Git e Github.

Git: software de controle de versão distribuído que nos permite desenvolver projetos em que várias pessoas podem contribuir simultaneamente, seja criando ou editando arquivos, e permitindo que alterações possam existir sem risco de serem sobrescritas.

Um commit no git salva na sua máquina um repositório local com as alterações feitas, o push envia pro repositório remoto, o github.

## Vantagens: 
* Controle de histórico
* Trabalho em equipe
* Ramificação do projeto
* Segurança e Organização. 


# Configurações Iniciais:
Com o git já instalado na máquina, pra configurar o usuário que irá usar o repositório local:

   ```
          git config --global user.name <Nome>
          git config --global user.email <Email>
   ```
   

# Na prática: 
Para iniciar o git na pasta atual, digitar no terminal:
```
        git init
```


* Se você já possui um repositório anterior ou deseja criar um repositório com um nome em específico, você pode passar o nome como parâmetro do comando:

```
        git init <O nome do seu repositório>
```


Adiciona seus arquivos modificados à fila para serem submetidos a um commit posteriormente:

```
        git add . 
```


* Ou caso queira adicionar apenas um arquivo específico:

```    
        git add <Nome do arquivo>
```


Com as alterações preparadas, para "commitar": 

```
        git commit -a -m <Mensagem no Commit>
```


* Onde o -a adiciona todo tipo de arquivo ao commit, e o -m te dá a possibilidade de adcionar uma mensagem para o commit.

É possível realizar o add e o commit em um único comando com:

```
         git commit -a
```


* Sendo possível tbm utilizar o -m para adicionar uma mensagem.
      
Para modificar o commit mais recente:

```
        git commit --amend -m <Mensagem no Commit>
```


# Ramificações/Branchs:
A ramificação que contém a versão do código principal e que o cliente vai utilizar após alterações estáveis, se chama main/master. 

A partir da branch principal, você pode criar novas pra ir fazendo alterações, pegando uma cópia da versão principal, e após isso, você pode passar as alterações pra branch principal, num processo chamado merge.

Lista todas as branchs:

```
        git branch
```
      
      
Criar branchs:

```
        git branch <Nome da branch>
        git checkout -b <Nome da branch>  // Cria branch nova a partir da antiga e já muda para ela.
```
      

Ir para outra branch:

```
        git checkout <Nome da branch>
```
      

Para passar alterações feitas em branchs para outras ramificações:

* Dá git checkout para a branch que vai receber a mescla, e em seguida:

```
        git merge <Nome da branch>  // passando o nome da branch que vai ser mesclada.
```
    

Para mesclar as branchs pode ser necessário fazer um:

```
        git rebase <Nome da branch> 
```
    

* Quando usar o rebase? 
    * Quando você criar uma branch a partir da principal, e quando quiser mesclá-la com a principal, alterações tenham sido feitas, então ele vai servir para alterar a base da branch criada. (Usar apenas em repositório local)

Alterar nome de uma branch:

```
        git branch -b <Novo nome da branch>
```

Arquivar as alterações em uma branch sem precisar commitar (possibilitando navegar entre branchs sem precisar commitar algo que está incompleto):

```
      git stash
```

Para voltar a ter acesso ao que está arquivado:

```
      git stash apply
```
 

Retorna a branch onde você está e se tem algo para commitar:

```
        git status
```

Para deletar branch:

```
        git branch -D <Nome da branch>
```


# Repositório remoto:
Já com um repositório criado no github:

* Enviar para repositório remoto:

Adiciona o repositório:

```
        git remote add origin <Link do repositório .git> 
```


Envia:

```
        git push origin <Nome da branch>
```


Puxa arquivos do repositório remoto para o local e atualiza seu conteúdo para a última versão:

```
        git pull <Nome da branch>
```

      
Clonar repositório existente:

```
        git clone <Link do repositório .git>
```


* Se você tiver autorização, quando você der um push no repositório que foi clonado, as alterações vão para o repositório remoto que foi clonado.

Traz as alterações que foram feitas no repositório remoto em relação ao repositório local:

```    
        git fetch
``` 


# Outras coisas:
Retorna histórico de commits:

```
       git log
       git shortlog
```


Mostra as diferenças do arquivo atual para o último commit:

```
        git diff
```
      

Restaura arquivo para o deixar identico ao último commit: 

```
        git restore <Nome do arquivo>
```


Permite selecionar qualquer commit específico de uma branch e suas alterações, e aplicá-lo a outra:

```
        git cherry-pick <Commit Hash ou tag>
```


Remove arquivos presentes na pasta que ainda não foram adicionados à fila pré-commit:

```
        git clean -f
```

Alterar um commit, apagar o último commit, fazer um novo commit, com as novas alterações que tinham no anterior mais as alterações novas que você fez e mais a mensagem de commit, que pode ser a mesma ou uma nova:
   * Também altera o hash do commit, o que pode causar problema na hora de enviar a branch que possui esse commit alterado pro repositório remoto

```
      git commit --ammend
```

Volta o arquivo para o jeito que estava no último commit:

```
        git checkout <Nome do arquivo>
```
