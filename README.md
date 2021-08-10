<h1 align="center">
    SENAI - SP    
</h1>
<h2 align="center">
    Programador Full Stack  -  Versionamento
</h2>

<p align="center">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/ortegavan/senai-versoes-colaboracoes?style=flat-square">
    <img alt="GitHub tag (latest by date)" src="https://img.shields.io/github/v/tag/ortegavan/senai-versoes-colaboracoes?style=flat-square">
    <img alt="GitHub followers" src="https://img.shields.io/github/followers/ortegavan?style=flat-square">
</p>

Seguem, abaixo, comandos que utilizei para trabalhar com versionamento.

## ⤵️ **Repositório local**

Setei nome de usuário e e-mail:

```bash
$ git config --global user.email ortegavan@live.com

$ git config --global user.name "Van Ortega"
```

Criei um repositório na pasta **senai-versoes-colaboracoes** utilizando a opção `-b` do comando `init` para setar o nome do *trunk* para **main** conforme comando abaixo:

```bash
$ git init -b "main" --initial-branch="main"
```

Fiz desta forma porque o *trunk* no GitHub "nasce" com o nome de **main** e eu não sabia alterar lá. Então, consultei a documentação do git disponível no link [Git - Reference (git-scm.com)](https://git-scm.com/docs) e cheguei na opção `-b`. Posteriormente, aprendi como alterar o nome do *trunk* no GitHub também, nas configurações do repositório.

Criei o arquivo **versoes.txt** e usei os comandos abaixo para adicioná-lo ao repositório local:

```bash
$ git add versoes.txt

$ git commit -m "meu primeiro commit"
```

Experimentei fazer alterações neste arquivo e novamente executei estes comandos para atualizá-lo no repositório.

## ⤴️ **Repositório remoto**

Criei um repositório no site do GitHub chamado **senai-versoes-colaboracoes** e utilizei o comando abaixo para fazer a ligação entre o repositório local e o repositório remoto:

```bash
$ git remote add origin git@github.com:ortegavan/senai-versoes-colaboracoes.git
```

Executei o comando a seguir para enviar o conteúdo sob versionamento no repositório local para o repositório remoto:

```bash
$ git push -u origin main
```

Com relação às branches, preferi utilizar a nomenclatura **branch1** e **branch2** e fiz o merge no *trunk*, a **main**; utilizei os comandos abaixo:

```bash
$ git checkout -b branch1
```

Alterei o **readme.md** e publiquei suas alterações:

```bash
$ git add .

$ git commit -m "subindo o readme na branch1"

$ git push origin branch1
```

Fiz o mesmo na **branch2**:

```bash
$ git checkout -b branch2

$ git add .

$ git commit -m "subindo o readme na branch2"

$ git push origin branch2
```

Voltei para o *trunk* com o comando abaixo e fiz um *merge* do **readme.md** da **main** com as **branch1** e **branch2**, atualizando o repositório local em seguida:

```bash
$ git checkout main

$ git merge branch1

$ git add .

$ git commit -m "resolvendo conflitos"

$ git merge branch2

$ git add .

$ git commit -m "resolvendo conflitos"
```

Eu havia feito previamente um *merge* sem efetuar o *commit* e o arquivo ficou só com a última alteração. Entendi meu erro e fiz novamente com os devidos *commit* conforme demonstrei no quadro anterior.

Por fim, enviei o conteúdo atualizado ao repositório remoto:

```bash
$ git push origin
```







