<div align="center">
	<img src="./assets/git.png">
	<h1>Comandos Git: Versionamento básico</h1>
</div>
&nbsp;
     
&nbsp;       
**1. Configurações básicas**  
---
Configurando a identidade do usuário que realizará o versionamento:
```sh
$ git config --global user.name "nome do usuario aqui"
$ git config --global user.email "email do usuario aqui"
```
Consultando a identidade registrada:
```sh
$ git config user.name 
$ git config user.email 
```
&nbsp;
&nbsp;   
**2. Inicializando um repositório Git**  
---
```sh
# Criando um diretório para o projeto
$ mkdir nome-do-diretorio

# Acessando o diretório
$ cd nome-do-diretorio/   

# Indicando ao Git que este será o diretório local usado para versionamento do projeto
$ git init 
```
&nbsp;
&nbsp;       
**3. Adicionando arquivos e registrando alterações**   
---
```sh
# Adicionando um arquivo para ser rastreado
$ git add nome-do-arquivo
```
```sh
# Adicionando todos os arquivos de um diretório de uma só vez
$ git add .
```
```sh
# Adicionando todos os arquivos de um diretório, de acordo com a sua extensão
$ git add *.py
$ git add *.js
```
Registrando as alterações do projeto (junto com uma mensagem de log):
```sh
$ git commit -m  "inclua breve descrição da alteração aqui"
```
Alterando a mensagem de commit:
```sh
$ git commit --amend -m  "inclua a nova descrição da alteração aqui"
```
&nbsp;
&nbsp;   
**4. Desfazendo alterações**   
---
Retornando o arquivo para antes da edição (antes dele ter sido adicionado ao stage):  
```sh
$ git checkout nome-do-arquivo
```
&nbsp;
Retirando um arquivo da gravação (depois dele ter sido adicionado ao stage):  
```sh
$ git reset HEAD nome-do-arquivo
```
Desfazendo o último commit da gravação  
```sh
$ git reset HEAD~1   
```
&nbsp;
&nbsp;   
**5. Exibindo o estado de um arquivo no momento**   
---
```sh
$ git status
```
&nbsp;
&nbsp;   
**6. Examinando o histórico de alterações**   
---
Visualizando o histórico das alterações:
```sh
$ git log   
```
```sh
# para auxiliar com maiores informações sobre os commits
$ git log -p  
```
```sh
# neste exemplo, para retornar apenas os dois últimos commits
$ git log -p -2  
```
```sh
# para retornar estatísticas sobre os commits realizados
$ git log --stat -2  
```
```sh
# para retornar o log resumido em uma única linha
$ git log --prety-oneline
```
```sh
# neste exemplo, para retornar o log dos commits realizados nos 2 últimos dias
$ git log --since=2.days 
```
&nbsp;
&nbsp;   
**7. Verificando diferenças entre versões**   
---
```sh
$ git diff
```
&nbsp;
&nbsp;       
**8. Branches**  
---
Criando um novo branch:
```sh
$ git branch nome-do-novo-branch
```
Criando e sendo redirecionado para um novo branch:
```sh
$ git checkout -b nome-do-novo-branch
```

Listando todos os branches existentes: *(branch em trabalho estará destacado em verde, caso haja mais de um)*
```sh
$ git branch     
```
```sh
# para listar os branches com seus respectivos logs de commits realizados
$ git branch -v   
```

Redirecionando para outro branch do repositório:
```sh
$ git checkout nome-do-outro-branch
```

Voltando para o branch master:
```sh
$ git checkout master    
``` 

Apagando um branch:
```sh
$ git branch -D nome-do-branch    
``` 
&nbsp;
&nbsp;       
**9. Unindo branches**  
---
Fazendo o merge:
```sh
$ git merge nome-do-branch-a-ser-mesclado    
``` 

&nbsp;
&nbsp;       
**10. Enviando as modificações para a nuvem**    
---
Criando um repositório remoto:
```sh
$ git remote add origin colar-link-aqui
# o link acima é o endereço do repositório criado no GitHub
# 'origin' é o nome default do repositório; se desejar, pode ser alterado
```

Enviando os arquivos ou alterações para o repositório remoto:
```sh
$ git push origin master  
```
&nbsp;
&nbsp;     
**11. Criando uma cópia de um repositório da nuvem para a máquina local**
---
```sh
$ git clone colar-link-aqui  
# o link acima é o endereço do repositório a ser copiado do GitHub
```
&nbsp;
&nbsp;   
**12. Atualizando repositório local com base no repositório na nuvem**
---
```sh
$ git pull
```
&nbsp;
&nbsp;   
**13. Criando um arquivo .gitignore**
---
```sh
1 - Criar aquivo de texto chamado: .gitignore
2 - Especificar nele quais os arquivos, pastas ou extensões (ex: *.txt) que não se deseja que sejam 'trackeados' pelo Git
```
&nbsp;
&nbsp;   
**Extra: Comandos úteis do Linux**  
---
`cd`: acessar um diretório      
`ls`: listar os arquivos do diretório em que o usuário se encontra   
`mkdir`: criar um diretório   
`pwd`: exibir o diretório em que o usuário se encontra  
`clear`: limpar a tela do terminal

**Utilizando o editor de texto Vim**  
`$ vim nome-do-arquivo`:  para criar, abrir ou editar um arquivo  
`i`: para entrar no modo insert  
`ESC`: para sair do modo insert  
`:w`: para salvar o arquivo  
`:w novo-nome-do-arquivo`: para salvar novo nome de arquivo  
`:q`: para sair do editor  
`:wq`: para salvar o conteúdo e sair do editor

&nbsp;
&nbsp; 
---
:bookmark_tabs: **Fontes consultadas:**  
[Git - Documentation](http://git-scm.com/docs)   
[Git e GitHub para Iniciantes (por Willian Justen)](https://www.youtube.com/playlist?list=PLlAbYrWSYTiPA2iEiQ2PF_A9j__C4hi0A)    
[GitHub Docs](https://docs.github.com/en/get-started/getting-started-with-git)    
[Bitbucket Support](https://support.atlassian.com/bitbucket-cloud/docs/git-and-mercurial-commands/)