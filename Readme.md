## Principais comandos do Git:

git config --global user.name "Claudio Alves" -> Define nome do usuário do projeto

git config --global user.email "teste@teste.com" -> Define o e-mail do projeto

git config --global core.editor vim (ou vi)(ou emacs subl (ou s)) -> Define o editor padrão que será usado no projeto

git config user.name -> Exibe o usuário do projeto

git config user.emails -> Exibe o e-mal do projeto

git config --list -> Exibe uma lista com as variáveis e seus valores pertencentes ao projeto

mkdir git-course -> Cria uma pasta para o projeto

cd git-course/ -> Entra na pasta do projeto

git init -> Inicializa o projeto e fica enxergando todas as mudanças que tiverem dentro do projeto

ls -la -> Lista os diretórios da pasta

cd.. -> Volta uma pasta acima

vi readme.md -> Abre o editor de texto (pode usar o notepad, notepad ++...)

no editor de texto: (tecla "I" habilita o editor para modo de inserção, tecla "ESC" sai do modo de inserção,
tecla ":" permite iniciar um comando, tecla "W" permite escrever/salvar, tecla "Q" + tecla "Enter" permite sair do
editor de texto, Teclas "D" + "D" apaga a linha desejada)

ls -> lista os arquivos da pasta do projeto

git status -> Serve para reportar como está o repostitório naquele momento

git add Readme.md -> Adciona esse arquivo no rastreio do Git

git commit -m "Add readme.mb" -> Commita o arquivo e adiciona uma mensagem

git log -> Exibe o histórico das versões, que arquivos mudaram

git log --decorate -> Exibe de qual branch foi para qual branch, se houve um merge, que threads foram geradas...

git log --author="Cla" -> Lista todos os commits do autor que tenha um nome com "cla"

git shortlog -> Exibe em ordem alfabética quais foram os autores, quantos commits fizeram e quais eles foram

git shortlog -sn -> Exibe somente a quantidade de commits e o autor

git log --graph -> Exibe em forma gráfica o que está acontecendo com as branchs e as versões

git show 2c0190d2ed472c4ab293f66dcdfd10a24d139707 (hash do commit) -> Exibe o que aconteceu com o commit, o que
foi adicionado, excluido...

git diff -> Exibe as modificações no arquivo antes de commitar

git diff --name-only -> Exibe somente o nome dos arquivos que foram modificados

git commit -am -> Prepara (adiciona) somente arquivos já existentes modificados para serem commitados, não prepara novos arquivos

git checkout readme.md -> Volta o arquivo para antes da edição

git reset HEAD -> Remove do stage o arquivo do local que você está, retira o arquivo da fila do stage

git reset --soft -> Remove somente o commit, mantendo o arquivo com suas modificações no stage pronto para ser
commitado novamente

git reset --mixed -> Remove o commit e retira o arquivo do stage deixando o arquivo como modified

git reset --hard -> Remove o commit, retira o arquivo do stage e ignora todas as modificações feitas no arquivo

ssh-keygen -t ed25519 -C "your_email@example.com"^ -> Gera uma nova chava SSH

ssh-keygen -t rsa -b 4096 -C "your_email@example.com" -> Gera uma nova chava SSH, Se você estiver usando um
sistema legado que não é compatível com o algoritmo Ed2551

cd ~/.ssh/ -> Exibe o local da nossa chave SSH
ls dentro do local da chave ssh exibe as chaves ssh (Ex.: id_ed25519  id_ed25519.pub/ ou id_rsa  id_rsa.pub known_hosts)

cat id_rsa.pub -> Pega a chave e exibe ela em tela

more id_rsa.pub -> Pega a chave e exibe ela em tela

vim id_rsa.pub -> Abre o editor de texto VI exibindo a chave

git remote add origin https://github.com/csalves/teste-versionamento-git.git -> Liga o repositório remoto ao
repositório local

git remote -> Informa que já existe o repositório origin

git remote -v -> Informa mais detalhes sobre o repositorio remoto adicionado, como o endereço

git push -u origin main(ou master) -> Envia os arquivos que tem no repositório local, o log e todas as modificações para o
repositório remoto que está sendo determinado. O "u" é para trackear o comando e em uma próxima não precisar
digitar tudo, somente git push, "origin" informa para onde vai e "master" informa de onde vem.

git clone git@github.com:csalves/teste-versionamento-git.git teste-versionamento-git-clone -> Permite clonar todo um repositório para sua máquina local

Fork (Feito direto no Github) -> Pega um projeto que não é seu e faz uma cópia dele pra você

git checkout -b test -> Cria uma nova branch no seu repositório

git branch - Exibe quais branchs seu repositório tem, *informa qual branch você está no momento

git checkout test -> Sai da branch atual e aponta para a branch desejada

git branch -D test -> Apaga a branch desejada

git merge test -> Junta os commits da branch desejada à branch master, adicionando o commmit na ordem cronológica respeitando o histórico de commits já presentes
na branch master, deixando o histórico linear

git add . -> Adiciona o arquivo ao stage
Vogit rebase rebase-brach -> Adiciona o commit da brant desejada para a branch master, colocando o commit no topo do histórico de commits deixando a estrutura linear

vi .gitignore -> Cria um arquivo de configuração do Git Ignore pra ignorar arquivos no (*.json ignora arquivos com a extenção .jason.../ db.xlsx ignora um arquivo
específico)

ctrl no terminal do git -> Limpa a tela

git stash (após ter feito alguma modificação em algum arquivo) -> Serve para guardar em um arquivo modificações que não ainda foram commitadas para serem chamadas posteriormente

git apply (após criar uma nova branch ou estar em alguma branch desejada) -> Serve para resgatar as modificações desejadas para serem commitadas na branch desejada

git stash clear -> Limpa a fila de stashs para não ter mais nenhuma modificação armazenada

git config --global alias.s status -> Cria um alias (um atalho) para um comando do git

git tag -a 1.0.0 -m "Readme finalizado" -> Cria uma tag (-a serve para adicionar algum dado, no caso a versão; -m serve para adicionar uma mensagem, já que a tag é uma
tag anotated (ou seja que contem uma anotação)

git push origin master --tags -> Sobe a tag para o repositório remoto

git revert d2a02532a03a6db64f3d034fb0e32bb52bfd2e82 -> Volta as alterações feitas no arquivo sem apagar o histórico do commit, possibilitando a correção da alteração
desejada e posteriormente subir a altração novamente com as modificações desejadas

git tag -d 1.0.1 -> Apaga a tag no repositório local

git push origin :1.0.1 -> Apaga a tag no repositório remoto


git push origin :testeapagar -> Apaga a branch no repositório remoto

------------------------------------------------------------------------------------------------------------------

# Git Course

Este é um repositório teste para ensinar como o Git funciona.i

Saiba mais em [willianjusten.com.br](http://willianjusten.com.br)

Gostou do curso? Quer mais? Ajude com uma doação, até um café é valido =)

[![paypal](https://paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=UTMFZUHX6EUGE)

Outros cursos em : [willian justen cursos](http://willianjusten.teachable.com)

Teste alteração

