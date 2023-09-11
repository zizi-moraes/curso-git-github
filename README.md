# curso-git-github
É um repositorio para estudar Git/GitHub

Resumo sobre o estudo com base no vídeo do **Victor Lima** [Curso de Git e GitHub](https://www.youtube.com/watch?v=192HgwRgOYE)

## Git

Git é um sistema de controle de versão utilizado para mudanças em arquivos e coordenar o trabalho entre várias pessoas em projetos de software.

Ele permite que você mantenha um histórico de todas as alterações feitas em um projeto, permitindo que você reverta para versões anteriores, colabore com outros desenvolvedores e mantenha um registro organizado das contribuições.

Git funciona localmente em seu computador e não requer uma conexão contínua com a internet. Isso torna mais fácil para os desenvolvedores trabalharem offline e sincronizarem suas alterações posteriormente.<br><br>


## GitHub

GitHub é uma plataforma baseada na web que hospeda repositórios Git e fornece uma série de recursos adicionais para colaboração em equipe e gerenciamento de projetos de software.

Ele oferece um serviço centralizado para armazenar, compartilhar e colaborar em projetos Git. Desenvolvedores podem enviar (push) e baixar (pull) código para e de repositórios no GitHub.

O GitHub também fornece ferramentas para rastrear problemas (issues), fazer solicitações de pull (pull requests), hospedar documentação, automatizar integração contínua e muito mais. Esses recursos ajudam as equipes a colaborarem de forma eficaz em projetos de código aberto e privados.

Em resumo, Git é o sistema de controle de versão que controla as mudanças em seu código, enquanto GitHub é uma plataforma online que facilita o compartilhamento, colaboração e gerenciamento de projetos de software usando o Git como base. Ambos desempenham papéis fundamentais no desenvolvimento de software colaborativo e no controle de versão.<br><br>


## Passo a passo

Instalar o Git no seu PC  
Confirmar instalacão: **git --version**  
Criar uma pasta que será o nosso projeto. Ex: "MeuSite"  
Acessar a pasta e fazer o comando: **git init**  
Acessar o VSCODE e abrir a pasta do projeto  
Criar um arquivo novo chamado site.html  
Comando git status exibe o status atual do projeto  

![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/c9be39ff-6903-4a9d-b7f0-e2cf23d301ba)  

Os comandos:  
**git add "nome_arquivo"**  
ou  
**git add .**  
Adiciona o arquivo na área de stage  
Se dermos outro git status podemos ver a alteração.  

![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/1df687c0-0607-4f79-ba80-54f23a75d12a)  

Antes de fazer o commit precisamos configurar o git.  
O git precisa saber qual é o autor do documento. Isso é muito importante para diferenciar as alterações feitas por autores diferentes.  
Para fazer isso deve-se informar os dados de user e e-mail  
**git config --global user.name "user"**  
**git config --global user.email "email@gmail.com"**   

O comando **git log** exibe os últimos commits realizados e exibe o mais recente que o texto HEAD  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/430dd101-9a04-4f05-ada8-7748b4214dc5)  

Se eu quiser desfazer um commit e volta no tempo posso pegar os 6 primeiro digitos de uma chave e fazer o seguinte comando:  
**git checkout a09826**  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/5d4e8db1-fe4a-4d3b-870a-bc0e0810e04d)  

com o **git log** podemos ver qual commit está no head:  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/c5aa6c26-cf10-4004-b2eb-7752d852f4ba)  

Para exibir os commits novamente basta dar o comando  
**git checkout master**  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/e45b0f7f-f0c7-4a9a-99d1-c100cee026d9)  

Para visualizar novamente dar o **git log**:  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/0fef32cf-f847-4b44-b7a9-3cf913dfea13)  


## Criando branch

Pode se utilizar os comandos:  
**git branch "nome_branch"**  
ou  
**git checkout -b "nome_branch"** //esse comando além de criar, já faz o checkout para a nova branch  


### Renomeando branch

Imagina que vc quer renomear a branch master  
Estando com essa branch já selecionada, digite o comando:  
**git branch -m main**  

Só faça isso em repositórios novos!!!!!


## Realizando o Merge  

Primeiro é necessário ir para a branch principal master ou main  
**git checkout main**  
**git pull**  

Depois faz o seguinte comando:  
**git merge nome_branch**  
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/2e6aeb73-9a4d-4e73-9722-55e62982abd6)  

Após isso, se vc der o comando git log, verá que a branch e o main estarão na mesma posição - no HEAD.  


## GITHUB

Crie um repositório e escolha:  
- privado ou público,  
- se terá readme  

Após esse passo, você terá que escolher qual dos 2
![image](https://github.com/zizi-moraes/curso-git-github/assets/136759769/985592dd-bd2e-47ba-93c7-050b129594f5)  


Como o projeto já existe localmente, vamos usar o segundo exemplo.  
Primeiro, no projeto copiar e colar o comando   
**git remote...**  

Se o projeto já estiver como main, pode se pular este segundo e ir para o próximo passo:  
**git push -u origin main**  


---
> Caso ocorra o erro abaixo, será necessário configurar o fingerprint:
Acesse os passos na página abaixo:  
1) https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent  
2) https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account  
***


## Clonar projeto:  
No terminal, acessar pasta desejada e digitat o comando:  
**git clone link_SSH_projeto**  
ou  
use o alias para o git clone  
**gcl link_SSH_projeto**  


## Repositório Remoto
Subindo alterações no GitHub  
**git push origin nome_branch**  

```
IMPORTANTE:  
Sempre que foi iniciar algum trabalho, dar um:  
**git pull origin <branch>**

Isso vai puxar as alterações recentes, feitas por outros devs e enviadas para a main (por ex).  
Ter esse hábito vai ajudar a evitar possíveis problemas/conflitos.  
```

## Resolvendo Conflitos  
Estando na sua branch, após digitar os comandos abaixo:  
**git pull origin main**  
**git merge minhaBranch** //branch que estou trabalhando  
Pode acontecer de você ser alertado sobre algum conflito.  
Isso ocorre quando algum dev sobe para main alguma alteração em uma linha que você está trabalhando.  

Para resolver você pode seguir a opções que aparecem no vscode (accept current change... e etc), ou apagar informação indesejada e realizar os comandos:  
**git add .**  
**git commit -m "resolvendo conflitos"**  
**git push origin main** //sobe para a main


## Rebase vs Merge   
### Merge:   
Cria um novo commit de mesclagem.  
Preserva o histórico original de cada branch.  
Resulta em um histórico de commits não linear.  
Bom para preservar o histórico detalhado de desenvolvimento de cada branch.  

### Rebase:   
Move commits para o topo de outra branch.  
Torna o histórico mais linear.  
Resulta em um histórico mais limpo, mas reescreve o histórico original.  
Útil para manter um histórico mais limpo e linear.  

#### Passos para fazer o Rebase:
1. Acesse a branch main e puxe as últimas alterações  
**git checkout main**  
**git pull** 
2. Volte para a branch em que você está trabalhado (branch feature) e digite o comando:  
**git rebase main**  
3. Caso exista algum conflito, o vscode irá indicar. Após corrigir o conflito, digitar o comando:  
**git rebase --continue**  
4. Repetir o passo 3 até que não exista mais conflito.  

### Escolha:   
Use o merge para preservar históricos detalhados e visíveis.  
Use o rebase para manter um histórico mais limpo e linear, especialmente em branches de recursos.  
A escolha entre merge e rebase depende das necessidades do projeto e das preferências da equipe. Mantenha a estratégia consistente em seu projeto.  


## Pull/Merge Request  
Um **pull request** (PR), também conhecido como **merge request** em algumas plataformas, é uma solicitação feita por um colaborador de um repositório Git para incorporar suas alterações em uma branch (normalmente uma branch de recurso) na branch principal (geralmente `main` ou `master`). Aqui está um resumo:  

1. **Abertura de um Pull Request**:  
   - Um desenvolvedor faz um fork de um repositório ou clona um repositório existente.  
   - Eles criam uma nova branch para trabalhar em uma funcionalidade ou correção específica.  
   - Após concluir o trabalho na nova branch, eles abrem um pull request no repositório original para solicitar a mesclagem das alterações.  

2. **Revisão de Código**:  
   - Outros membros da equipe revisam o código e fornecem feedback por meio de comentários.  
   - As discussões podem ocorrer para esclarecer dúvidas e fazer melhorias no código.  
   - A revisão de código ajuda a manter a qualidade do código e a evitar problemas.  

3. **Testes Automatizados**:  
   - Muitas vezes, sistemas de integração contínua (CI) executam testes automatizados nas alterações propostas.  
   - Isso ajuda a garantir que as alterações não introduzam problemas no código existente.  

4. **Mesclagem**:  
   - Após revisões, discussões e aprovações, o mantenedor do repositório original pode mesclar as alterações na branch principal.  
   - As alterações são agora parte do código principal e estão disponíveis para todos.  

5. **Encerramento do Pull Request**:  
   - O pull request é fechado após a mesclagem bem-sucedida das alterações.  
   - Qualquer problema relacionado à funcionalidade ou correção é acompanhado por meio de issues (problemas) associadas.  

6. **Histórico de Mudanças Transparente**:  
   - O pull request fornece um histórico transparente das alterações propostas, revisões e comentários relacionados.  

7. **Colaboração e Contribuições Abertas**:  
   - O pull request permite uma colaboração eficaz em projetos de código aberto e equipes de desenvolvimento distribuídas.  
   - Facilita a contribuição de desenvolvedores externos aos projetos.  

O pull request é uma prática comum no desenvolvimento colaborativo de software e é amplamente usado em plataformas de hospedagem de código, como o GitHub e o GitLab. Ele é essencial para manter o controle de alterações, facilitar a revisão do código e garantir a qualidade do software em desenvolvimento.  

