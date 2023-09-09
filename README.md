# curso-git-github
É um repositorio para estudar Git/GitHub

Resumo sobre o estudo: <br>

##Git

Git é um sistema de controle de versão utilizado para mudanças em arquivos e coordenar o trabalho entre várias pessoas em projetos de software.

Ele permite que você mantenha um histórico de todas as alterações feitas em um projeto, permitindo que você reverta para versões anteriores, colabore com outros desenvolvedores e mantenha um registro organizado das contribuições.

Git funciona localmente em seu computador e não requer uma conexão contínua com a internet. Isso torna mais fácil para os desenvolvedores trabalharem offline e sincronizarem suas alterações posteriormente.<br><br>


##GitHub<br>

GitHub é uma plataforma baseada na web que hospeda repositórios Git e fornece uma série de recursos adicionais para colaboração em equipe e gerenciamento de projetos de software.

Ele oferece um serviço centralizado para armazenar, compartilhar e colaborar em projetos Git. Desenvolvedores podem enviar (push) e baixar (pull) código para e de repositórios no GitHub.

O GitHub também fornece ferramentas para rastrear problemas (issues), fazer solicitações de pull (pull requests), hospedar documentação, automatizar integração contínua e muito mais. Esses recursos ajudam as equipes a colaborarem de forma eficaz em projetos de código aberto e privados.

Em resumo, Git é o sistema de controle de versão que controla as mudanças em seu código, enquanto GitHub é uma plataforma online que facilita o compartilhamento, colaboração e gerenciamento de projetos de software usando o Git como base. Ambos desempenham papéis fundamentais no desenvolvimento de software colaborativo e no controle de versão.<br><br>


##Passo a passo

Instalar o Git no seu PC
Confirmar instalacão: git --versionCriar uma pasta que será o nosso projeto. Ex: "MeuSite"Acessar a pasta e fazer o comando: git init
Acessar o VSCODE e abrir a pasta do projeto
Criar um arquivo novo chamado site.html
Comando git status exibe o status atual do projeto
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/c9be39ff-6903-4a9d-b7f0-e2cf23d301ba)


O comando git add <nome arquivo> ou git add . 
Adiciona o arquivo na área de stage
Se dermos outro git status podemos ver a alteração.
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/1df687c0-0607-4f79-ba80-54f23a75d12a)

 
Antes de fazer o commit precisamos configurar o git.
O git precisa saber qual é o autor do documento. Isso é muito importante para diferenciar as alterações feitas por autores diferentes.
Para fazer isso deve-se informar os dados de user e e-mail
git config --global user.name "user"
git config --global user.email "email@gmail.com" 

O comando <b>git log<b> exibe os últimos commits realizados e exibe o mais recente que o texto HEAD
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/430dd101-9a04-4f05-ada8-7748b4214dc5)
 

Se eu quiser desfazer um commit e volta no tempo posso pegar os 6 primeiro digitos de uma chave e fazer o seguinte comando:
git checkout a09826
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/5d4e8db1-fe4a-4d3b-870a-bc0e0810e04d)

com o <b>git log<b> podemos ver qual commit está no head:
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/c5aa6c26-cf10-4004-b2eb-7752d852f4ba)

 

Para exibir os commits novamente basta dar o comando
<b>git checkout master</b>  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/e45b0f7f-f0c7-4a9a-99d1-c100cee026d9)


Para visualizar novamente dar o 
git log
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/0fef32cf-f847-4b44-b7a9-3cf913dfea13)



##Criando branch

Pode se utilizar os comandos: 
git branch "<nome>"
ou 
git checkout -b "<nome>" //esse comando além de criar, já faz o checkout para a nova branch

Renomeando branchImagina que vc quer renomear a branch master
Estando com essa branch já selecionada, digite o comando:
git branch -m main

Só faça isso em repositórios novos!!!!!


##Realizando o Merge

Primeiro é necessário ir para a branch principal master ou main
git checkout main
git pull

Depois faz o seguinte comando:
git merge <nome-da-branch> 
Após isso, se vc der o comando git log, verá que a branch e o main estarão na mesma posição - no HEAD.


GITHUB

Crie um repositório e escolha:
-  privado ou público, 
- se terá readme

Após esse passo, você terá que escolher qual dos 2 

 

Como o projeto já existe localmente, vamos usar o segundo exemplo.
Primeiro, no projeto copiar e colar o comando 
git remote....

Se o projeto já estiver como main, pode se pular este segundo e ir para o próximo passo:
git push -u origin main

------------------------------------------------------------------------------------------------------
Caso ocorra o erro abaixo, será necessário configurar o fingerprint:

Acesse os passos na página abaixo:1) https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
2) https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
------------------------------------------------------------------------------------------------------

Clonar projeto:
No terminal, acessar pasta desejada e digitat o comando:
git clone <link SSH do projeto>

ou use o alias para o git clone
gcl  <link SSH do projeto>


Repositório Remoto
Subindo alterações no GitHub
git push origin <nome branch> 

IMPORTANTE:
Sempre que foi iniciar algum trabalho, dar um:
git pull origin <branch>

Isso vai puxar as alterações recentes, feitas por outros devs e enviadas para a main (por ex).
Ter esse hábito vai ajudar a evitar possíveis problemas/conflitos.


Resolvendo Conflitos
Estando na sua branch, após digitar os comandos abaixo:
git pull origin main
git merge <minhaBranch> //branch que estou trabalhando
Pode acontecer de você ser alertado sobre algum conflito.
Isso ocorre quando algum dev sobe para main alguma alteração em uma linha que você está trabalhando.

Para resolver você pode seguir a opções que aparecem no vscode (accept current change... e etc), ou apagar informação indesejada e realizar os comandos:
git add .git commit -m "resolvendo conflitos"git push origin main //sobe para a main


Rebase




Pull/Merge Request










