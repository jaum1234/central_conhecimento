# GIT BASICS

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

