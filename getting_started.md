# VERSION CONTROL

## O que é Controle de Versão
- Sistema de controle de versões;
- Salva as modificações feitas a um arquivo ou a um grupo de arquivos;

### Controle de Versionamento Local
![](https://i.gyazo.com/7520bae07a54304a6eeff93442735fae.png)

### Controle de Versionamento Centralizado
![](https://i.gyazo.com/c686cce4e4cf81b4bfe5ba39214d03d4.png)

### Controle de Versionamento Distribuído
![](https://i.gyazo.com/d41e9922a5d5304485a66c010d661631.png)

## O que é Git?

### Snapshots
- A maiorias dos VCS armazenam as informações como listas de alterações baseadas em arquivos;
![](https://i.gyazo.com/161f15b0c3e2a09cf56d9b4878fc7493.png)

- No Git, a cada commit, uma fotografia (snapshot) é tirada do estado atual dos arquivos e uma referência é guardada para essa fotografia;
![](https://i.gyazo.com/d324b803f8ad4bfd6ecff4cd3954684c.png)

### Operações Locais
- Quase todas as operações são locais;
- Todo o histórico dos arquivos é armazenado localmente;

### Integridade
- É feito um checksum de todos os dados antes de serem armazenados;
- SHA-1 hash;

![](https://i.gyazo.com/e792a0914f2baa524ce52147ddb51ab6.png)

- Toda informação armazenada nos bancos de dados do git são referenciadas por um valor hash;

### Adição de Dados
- Geralmente, o Git apenas adiciona dados;
- É extramamente difícil fazer algo que exclua uma informação permanentemente; 

### Os 3 Estados
1. Modificado: arquivos modificados que ainda não foram commitados;
2. Staged: arquivos marcados para o próximo commit;
3. Commitado: arquivos adicionados no banco de dados local;

![](https://i.gyazo.com/5f7257dadc760075b9162d108538c4ec.png)

Obs: Ao menos no VSCode, um quarto estado pode ser observado: Não rastreado. Um arquivo se encontra nesse estado quando ele nunca foi commitado anteriomente.

## Comandos
```php
git config

// adicionar flag --help ou -h ao final do comando para mais informações
```