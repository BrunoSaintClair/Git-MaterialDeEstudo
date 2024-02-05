# Git-MaterialDeEstudo

ORGANIZAR EM TÓPICOS BONITINHO SE BASEANDO NO DE DOUGLAS, MUDAR AS PALAVRAS E APRIMORAR O MATERIAL
PROXIMOS VIDEOS: 
https://youtu.be/ts-H3W1uLMM?si=ij-upzLB3AlmFw8l
https://youtu.be/Zwv9qRyVeU4?si=3sMUhwch-YDRmVhi





Material de estudo de Git e Github.

Git: software de controle de versão dsitribuído. 

Um commit no git salva na sua máquina um repositório local com as alterações feitas, o push envia pro repositório remoto, o github.

Vantagens: controle de histórico, trabalho em equipe, ramificação do projeto, segurança e organização. 

Ramificações:
A ramificação que contém a versão do código principal e que o cliente vai utilizar após alterações estáveis, se chama main/master. A partir da branch principal você pode criar novas pra ir fazendo alterações, pegando uma cópia da versão principal, e após você pode passar as alterações pra branch principal, esse processo se chama merge. 



Na prática: 
Com o git instalado, e o projeto aberto no editor de código:
Para iniciar o git digitar no terminal 'git init' 
Para enviar as alterações para o histórico/"commitar":
'git add .' -> pega todos arquivos alterados e adiciona num estágio para commit. 
'git add ____ ' -> adiciona num estágio para commit apenas o arquivo indicado onde estam os underlines. 
Com as alterações preparadas, para "commitar": 
'git commit -m "___"  (os underlines representam o lugar onde se deve colocar o nome do commit)
'git commit --amend' -> modifica o commit mais recente

'git status' -> retorna a branch onde você está e se tem algo para commitar. 
'git log' -> retorna histórico de commits, incluindo o hash, que pode ser usado para voltar para aquele commit específico. 
'git diff' -> mostra as diferenças do arquivo atual para o último commit.
'git restore __ ' -> restaura arquivo para o deixar identico ao último commit. 

'git branch' -> mostra a branch atual
'git branch ___ ' -> passando um nome como parametro vc cria uma nova branch
'git checkout -b ___ ' -> cria branch nova a partir da branch antiga e já muda para ela.
'git checkout ____ ' -> vai para a branch selecionada. 

Para passar alterações feitas nas outras branchs para outras ramificações:
Dá git checkout para a branch que vai receber, e em seguida 'git merge ___ ', passando o nome da branch que vai ser mesclada.

+ Repositório remoto:
Com um repositório criado no github:
'git remote add origin ___ ' -> link dado após criar o repositório
'git push origin ___ ' -> nome da branch

'git pull origin ___ ' -> nome da branch, puxa arquivos do repositório remoto

'git fetch' -> traz as alterações que foram feitas no repositório remoto.
