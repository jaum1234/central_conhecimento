# Git Basics

## Inicializando um Repositório em um Diretório Existente
```
cd /home/user/directory

git init
git add .
git commit -m "First commit"
```

## Clonando um Repositório
```php
git clone <url> [nome-do-diretório]

// [nome-do-diretório] é um parâmetro opcional.
```

## Salvando Alterações
![](https://i.gyazo.com/9b953f7a87c62c2bd33a9934d83548fb.png)

### Verificando o Status
```
git status
```

### Adicionando Arquivos ao Próximo Commit
```php
git add <arquivos>

// 'arquivos' pode ser o caminho tanto de um diretório, quanto de um arquivo.
```
Caso um arquivo já adicionando a fase a fase de staging tenha sido modificado, a versão enviada para o commit será a versão do arquivo no momento da adição ao staging.


### Breve status
```
git status -s
```

### Ignorando Arquivos
```
cat .gitignore

node_modules
.env
```

- Linhas em branco ou que iniciam com # são ignoradas;
- Glob pattern pode ser utilizado;
- Iniciar um padrão com / evita recursividade;
- Finalizar um padrão com / especifica um diretório;
- Negar com padrão iniciando com !;

### Visualizando Mudanças
```php
git diff // compara o diretório de trabalho com a área de staging
git diff --staged ou --cached // exibe tudo que está na área de staging
```

### Commitando Alterações
```php
git commit // abre o editor de texto configurado para que uma mensagem seja adicionada ao commit
git commit -m <mensagem> // permite escrever a mensagem do commit via linha de comando
git commit -v // exibe no editor o resultado do git diff --staged
```

### Pulando a Área de Staging
```
git commit -a
```
Automaticamente adiciona os arquivos à área de staging, sem a necessidade do ```git add```, e commita as alterações.

### Removendo Arquivos
```php
rm <arquivo> // removendo arquivo do diretório de trabalho
git rm <arquivo> // adiciona o arquivo na área de staging para remoção do banco do git
```
```php
git rm -f <arquivo> // força a remoção de um arquivo que já está na área de staging (remove tanto do git, quanto do diretório de trabalho)

git rm --cached <arquivo> // remove o arquivo da área de staging
```

### Movendo Arquivos
- O Git não rastreia arquivos explicitamente;
- Nenhum metadado é armazenado, indicando que um arquivo tenha sido renomeado, por exemplo;
```php
git mv arquivo_de arquivo_para
```
- A renomeação é feita de forma implícita, movendo os dados de um arquivo para outro;
- O Git é inteligente o suficiente para entender que essa renomeação aconteceu (isso pode ser observado pelo ```git status```);

O comando acima é equivalente a:
```php
mv arquivo_de arquivo_para
git rm arquivo_de
git add arquivo_para
```

## Visualizando o Histórico de Commits
```php
git log
```
Exibe uma lista de todos os commits em cronologia reversa.

---

```
git log --patch
```
Adiciona ao output as mudanças que ocorreram em cada commit.

---

```
git log --stat
```
Sumariza o status (arquivos modificados, removidos, inseridos, numero de linhas modificas e etc) de cada commit.

---

```php
git log --pretty=(oneline|short|full|fuller|format)

// Quando utilizado a opção 'format', uma exibição personalizada pode ser especificada.

git log --pretty=format:"%h - %an, %ar : %s"
```
Formata a exibiçâo do log.

![](https://i.gyazo.com/48507fa73655a4df004f70ad98f22204.png)

---
```
git log --pretty=format:"%h %s" --graph
git log --pretty=oneline --graph
```
Exibe um gráfico que mostra as branchs e o histórico de merges.

---
Opções comuns para o git log:

![](https://i.gyazo.com/85aac2bc4dc5d440b53accb1425a2f36.png)

---

### Limitando a Saída do Log
As opções a seguir tem por objetivo exibir somente um subconjunto de commits.

---

```
git log -2
```
Limita a quantidade exata de commits a serem exibidos.

---

```
git log --since=2.weeks
```
Limita a partir de qual momento os commits devem ser exibidos.

---
```
git log --until=2024-02-10
```
Limita até qual momento o commits devem ser exibidos.

---
```
git log --grep="Entendendo"
```
Busca pelos commits que contém a string informada.

---
```
git log --author="joao"
```
Busca pelos commits com o autor informado.

---
```
git log -S <nome-funcao>
```
Busca pelos commits que estão relacionados a string informada. A busca ocorre não pelo texto dos commits, mas sim pelas linhas de código alteradas.

---
```
git log -G <regex>
git log -- caminho/para/arquivo
git log --no-merges
```
---

![](https://i.gyazo.com/ac43a01a8360770dc0e66b310997c706.png)

---
## Desfazendo Coisas
```
git commit --amend -m "Nova mensagem"
```
O comando ```--amend``` sobrescreve o último commit com a área de staging atual e com a nova mensagem de commit. Sendo assim, é como se o último commit nunca tivesse existido.
