## SENAI - SP

### Programador Full Stack  -  Versionamento

Seguem, abaixo, comandos que utilizei para trabalhar com versionamento.



**Repositório local**

Setei nome de usuário e e-mail:

```
$ git config --global user.email ortegavan@live.com

$ git config --global user.name "Van Ortega"
```

Criei um repositório na pasta **senai-versoes-colaboracoes** utilizando a opção `-b` do comando `init` para setar o nome do *trunk* para **main** conforme comando abaixo:

```
$ git init -b "main" --initial-branch="main"
```

Fiz desta forma porque o *trunk* no GitHub "nasce" com o nome de **main** e eu não sabia alterar lá. Então, consultei a documentação do git disponível no link [Git - Reference (git-scm.com)](https://git-scm.com/docs) e cheguei na opção `-b`. Posteriormente, aprendi como alterar o nome do *trunk* no GitHub também, nas configurações do repositório.

Criei o arquivo **versoes.txt** e usei os comandos abaixo para adicioná-lo ao repositório local:

```
$ git add versoes.txt

$ git commit -m "meu primeiro commit"
```

Experimentei fazer alterações neste arquivo e novamente executei estes comandos para atualizá-lo no repositório.



**Repositório remoto**

Criei um repositório no site do GitHub chamado **senai-versoes-colaboracoes** e utilizei o comando abaixo para fazer a ligação entre o repositório local e o repositório remoto:

```
$ git remote add origin git@github.com:ortegavan/senai-versoes-colaboracoes.git
```

Executei o comando a seguir para enviar o conteúdo sob versionamento no repositório local para o repositório remoto:

```
$ git push -u origin main
```

Com relação às branches, preferi utilizar a nomenclatura **branch1** e **branch2** e fiz o merge no *trunk*, a **main**; utilizei os comandos abaixo:

```
$ git checkout -b branch1
```

Alterei o **readme.md** e publiquei suas alterações:

```
$ git add .

$ git commit -m "subindo o readme na branch1"

$ git push origin branch1
```

Fiz o mesmo na **branch2**:

```
$ git checkout -b branch2

$ git add .

$ git commit -m "subindo o readme na branch2"

$ git push origin branch2
```

Voltei para o *trunk* com o comando abaixo e fiz um *merge* do **readme.md** da **main** com as **branch1** e **branch2**, atualizando o repositório local em seguida:

```
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

```
$ git push origin
```







