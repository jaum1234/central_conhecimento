# Expressões Regulares

## 1 Definição

Sequência de caracteres que descreve um padrão em um texto. A sequência pode ser composta por caracteres literais ou metacaracteres.

## 2 Metacaracteres

| Metacaracter | Descrição |
| ------------ | --------- |
| . | Busca por qualquer simbolo exceto uma nova linha |
| [] | Busca por qualquer simbolo contido no conjunto descrito dentro dos colchetes |
| [^] | Busca por qualquer simbolo que não está contido no conjunto descrito dentro dos colchetes |
| * | Busca por 0 ou mais ocorrêncas do simbolo predecessor |
| + | Busca por 1 ou mais ocorrêncas do simbolo predecessor |
| ? | Torna o simbolo predecessor opcional |
| {n,m} | Busca por pelo menos 'n' ocorrêncas, mas nada mais do que 'm' ocorrência do símbolo predecessor |
| (xyz) | Busca por qualquer simbolo contido no grupo na mesma exata ordem |
| &#124; | Busca pelo simbolo precessor ou pelo simbolo sucessor |
| \ | Escapa o simbolo sucessor |
| ^ | Corresponde ao inicio do input |
| $ | Corresponde ao fim do input |

## 3 Conjuntos de Simbolos

| Conjunto | Descrição |
| ------------ | --------- |
| . | Qualquer simbolo exceto uma nova linha |
| \w | Qualquer simbolo alfanumérico |
| \W | Qualquer simbolo não alfanumérico |
| \d | Qualquer dígito |
| \D | Qualquer não dígito |
| \s | Qualquer espaço em branco |
| \S | Qualquer espaço não em branco |

# 4 Olhar ao Redor

| Simbolo | Descrição |
| ------------ | --------- |
| (?=) | Busca pelo simbolo predecessor sucedido pelo padrão definido dentro do grupo sem incluir o grupo na lista de busca |
| (?!) | Busca pelo simbolo predecessor não sucedido pelo padrão definido dentro do grupo sem incluir o grupo na lista de busca |
| (?<=) | Busca pelo simbolo sucessor precedido pelo padrão definido dentro do grupo sem incluir o grupo na lista de busca |
| (?<!) | Busca pelo simbolo sucessor não precedido pelo padrão definido dentro do grupo sem incluir o grupo na lista de busca |



