# Scripting

**Scripting** ou linguagem de script é uma linguagem de programação para um [run-time environment](https://en.wikipedia.org/wiki/Run-time_environment) especial que automatiza a execução de tarefas, estas tarefas que poderiam ser executadas uma a uma por um operador humano. Linguagens de script são freqüentemente [interpretadas](https://en.wikipedia.org/wiki/Interpreted_language), em vez de [compiladas](https://en.wikipedia.org/wiki/Compiler).

Os ambientes que podem ser automatizados por meio de scripts incluem [software applications](https://en.wikipedia.org/wiki/Software_application), [páginas da web](https://en.wikipedia.org/wiki/Web_page) em um navegador da web, uso de shells de sistemas operacionais, sistemas embarcados, bem como vários jogos. Uma linguagem de script pode ser vista como uma linguagem específica de domínio para um ambiente particular. As linguagens de script às vezes também são chamadas de linguagens de programação de alto nível, pois operam em um alto nível de abstração, ou como linguagens de controle, principalmente para linguagens de controle de tarefas em mainframes.

O termo "linguagem de script" também é usado para se referir a linguagens dinâmicas de alto nível de uso geral, como **Perl**, **PowerShell**, **Python**, etc. Com o termo "script" frequentemente usado para pequenos programas em tais linguagens ou em linguagens de domínio específico, como as linguagens de processamento de texto **sed** e **AWK**. Algumas dessas linguagens foram originalmente desenvolvidas para uso em um ambiente específico e, posteriormente, desenvolvidas em linguagens portáteis específicas de domínio ou de uso geral. 

O espectro de linguagens de script varia de linguagens muito pequenas e altamente específicas de domínio a linguagens de programação de propósito geral usadas para script. Exemplos padrão de linguagens de script para ambientes específicos incluem: **Bash**, para o Unix ou sistemas operacionais semelhantes ao Unix; **ECMAScript** (JavaScript), para navegadores da web; e **Visual Basic for Applications**, para aplicativos do Microsoft Office. **Lua** é uma linguagem projetada e amplamente utilizada como uma linguagem de extensão. **Python** é uma linguagem de propósito geral que também é comumente usada como uma linguagem de extensão, enquanto ECMAScript ainda é principalmente uma linguagem de script para navegadores da web, mas também é usada como uma linguagem de propósito geral. O dialeto **Emacs Lisp** do **Lisp** (para o editor Emacs) e o dialeto Visual Basic for Applications do Visual Basic são exemplos de dialetos de linguagem de script de linguagens de propósito geral.

As linguagens de script típicas são destinadas a serem muito rápidas de aprender e escrever, seja como arquivos de **código-fonte** curtos ou interativamente em um **[ read–eval–print loop](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)** (REPL, shell de linguagem). Isso geralmente implica sintaxe e semântica relativamente simples para elas.

## A Linguagem Bash

Bash é o **[shell](https://en.wikipedia.org/wiki/Unix_shell)**, ou interpretador de linguagem de comando, para o sistema operacional GNU/Linux. O nome é um acrônimo para ‘*Bourne-Again SHell*’, um trocadilho com Stephen Bourne, o autor do ancestral direto do atual shell **sh** do Unix, que apareceu na versão do Unix da Sétima Edição do Bell Labs Research.

Como uma linguagem de script, o bash é uma [linguagem específica de domínio](https://en.wikipedia.org/wiki/Domain-specific_language) para manipular e compor processos e arquivos.

Embora o sistema operacional GNU forneça outros shells, incluindo uma versão do **csh**, Bash é o shell padrão. Como outros softwares GNU, o Bash é bastante portátil. Atualmente é executado em quase todas as versões do Unix e alguns outros sistemas operacionais - existem portas com suporte independente para as plataformas MS-DOS, OS/2 e Windows.

Bash é um processador de comando que normalmente é executado em uma janela de texto onde o usuário digita comandos que causam ações. O Bash também pode ler e executar comandos de um arquivo, chamado de [shell script](https://en.wikipedia.org/wiki/Shell_script). Como todos os shells do Unix, ele suporta *globbing* de nome de arquivo (correspondência de *wildcard*), [piping](https://en.wikipedia.org/wiki/Pipeline_(Unix)), [command substitution](https://en.wikipedia.org/wiki/Command_substitution), [variáveis](https://en.wikipedia.org/wiki/Variable_(programming)) e [estruturas de controle](https://en.wikipedia.org/wiki/Control_flow) para [testes de condição](https://en.wikipedia.org/wiki/Conditional_(programming)) e [iteração](https://en.wikipedia.org/wiki/Iteration). As palavras-chave, sintaxe, variáveis com escopo dinâmico e outros recursos básicos da linguagem são todos inspirados do sh. Outros recursos, por exemplo, histórico, são inspirados no csh e ksh. Bash é um shell compatível com POSIX, porém com diversas extensões.

**$SHELL** é a variável de ambiente que contém sua shell favorita. Ela é inicializada por login ou qualquer outro aplicativo que efetua login com base no campo shell em sua entrada de usuário no banco de dados **passwd** (seu shell de login).

Para vermos a nossa shell atual podemos executar o comando:

```bash 
echo $SHELL # /bin/bash
```

### Por que usar Bash?

Vejamos algumas tarefas ao qual o Bash pode nos auxiliar:

- Orquestrar tarefas de inicialização/desligamento do sistema.
- Renomear automaticamente uma coleção de arquivos.
- Encontrar todos os arquivos `.png` duplicados em um disco rígido.
- Orquestrar um conjunto de ferramentas para quebrar a senha de uma aplicação.
- Implementar um banco de dados relacional a partir de arquivos de texto.
- Encontrar padrões de textos em arquivos.
- Simplificação da configuração e reconfiguração de software.

### Bash Scripting

Para criarmos um script bash, devemos colocar `#!/bin/bash` no topo de nosso arquivo.

Em seguida, temos que alterar as permissões no arquivo para torná-lo executável:

```bash
chmod u+x script.sh
```

Para executar o script a partir do diretório atual, podemos executar `./script.sh` ou `bash script.sh` e passar os parâmetros que desejarmos.

Quando o shell executa um script, ele encontra o `#!/caminho/do/interpretador`.

Em seguida, ele executa o interpretador (neste caso, `/bin/bash`) no próprio arquivo.

#### Hello World

Nós programadores geralmente aprendemos novas linguagens por meio do programa Hello World. Um simples programa que imprime a string "Hello World" no *standard output*.

Vamos então criar um arquivo com o comando **touch**:

```bash
touch hello_word.sh
```

Podemos agora usar um editor como [vim](https://www.vim.org/) ou [nano](https://www.nano-editor.org/) para editá-lo com o seguinte conteúdo:

```bash
#!/bin/bash
echo "Hello World"
```

Devemos agora salvar o arquivo e tornar este arquivo executável usando o comando abaixo:

```bash
chmod 764 hello_word.sh
```

Agora podemos executá-lo com um dos seguintes comandos:

```bash
bash hello_word.sh 
./hello_word.sh
```

Como podemos observar, será impresso "*Hello World*" em nossa tela.

#### O Comando echo 

O comando echo é usado para imprimir informações no bash. É semelhante à função C **printf()** e fornece muitas opções comuns, incluindo *escape sequences* e redirecionamento.

Por exemplo:

```bash
#!/bin/bash

echo "Imprimindo texto"
echo -n "Imprimindo texto sem uma nova linha"
echo -e "\nImprimindo \t caracteres \t especiais\n"
```

A opção **-n** indica que não desejamos imprimir uma nova linha no final. Já a opção **-e** habilita interpretação de *backslash escapes* como por exemplo `\t` e `\n`.

Bash também possui o comando **printf** que por padrão é capaz de interpretar *backslash escapes*:

```bash
#!/bin/bash

printf "Olá\t Mundo\n"
```

#### Comentários

Os comentários são úteis para a documentação de nosso código. É uma prática comum colocar comentários dentro de códigos que lidam com a lógica crítica. Para comentar uma linha, basta usar o caractere **#** (hash) antes dela.

```bash
#!/bin/bash

# Elevando 2 na potência 3
(( x = 2**3 ))

# Imprimindo o resultado
echo $x
```

Como já tínhamos visto, a primeira linha é uma exceção e é chamado de **shebang** e permite que o sistema saiba qual interpretador usar ao executar este script, que irá imprimir o resultado da expressão `2**3` que é igual a `8`.

Também é possível usarmos comentários de várias linhas para documentar nossos scripts:

```bash
#!/bin/bash

: '
Script que calcula
recursivamente
o enésimo número 
da série Fibonacci

O número deve ser 
passado via parâmetro

Input / Output
1 -> 1
2 -> 1
3 -> 2
4 -> 3
5 -> 5
6 -> 8
20 -> 6.765
'
echo $1 | awk 'function fib(n) {
    return n<2 ? n : fib(n-1) + fib(n-2)
} {printf ("%'"'"'d\n", fib($1))}'
```

Neste script calculamos o enésimo número da série Fibonacci com o auxílio da [linguagem AWK](https://en.wikipedia.org/wiki/AWK), para executarmos o script devemos passar um valor como argumento:

```bash
bash mult_comments.sh 8 # 55
./mult_comments.sh 10 # 21
```

Observe que os comentários de várias linhas são colocados entre os caracteres `:'` e `'`.

#### While Loop

A construção **while** loop é usada para executar instruções várias vezes enquanto uma condição for verdadeira, por exemplo:

```bash
#!/bin/bash

i=0
while [ $i -le 10 ]
do
	echo "Número: $i" 
((i++))
done
```

Enquanto o valor de **i** for menor ou igual a **10** os comandos dentro do **while** serão executados.

Lembre que o espaço ao redor dos colchetes é obrigatório.

#### Until Loop

O loop until é usado para executar um determinado conjunto de comandos, desde que a condição fornecida seja avaliada como **falsa**.

O loop Bash until assume a seguinte forma:

```
until [CONDIÇÃO]
do
  [COMANDOS]
done
```

A condição é avaliada antes de executar os comandos. Se a condição for avaliada como falsa, os comandos serão executados. Caso contrário, se a condição for avaliada como verdadeira, o loop será encerrado e o controle do programa será passado para o comando seguinte.

No exemplo abaixo, em cada iteração, o loop imprime o valor atual da variável **COUNT** e incrementa a variável em um.

```bash
#!/bin/bash

COUNT=0
# bash until loop
until [ $COUNT -gt 5 ]; do
    echo Valor de COUNT é = $COUNT
    let COUNT++
done 
```

#### For Loop

O **for** loop é outra construção do Bash amplamente usada que permite aos usuários iterar códigos de forma eficiente.

Podemos iterar no estilo C, usando um valor inicial para **i**, uma condição de parada `i<=13` e incrementar a variável `i++`:

```bash
#!/bin/bash

for (( i=1; i<=13; i++ ))
do
	echo -n "$i "
done
```

Neste caso o comando `echo -n "$i "` será executado até que `i<=13`.

Também podemos iterar sob o resultado de um comando como o **ls**, por exemplo:

```bash
for i in $(ls)
do
	echo "$i"
done
```

Serão impressos todos os arquivos do diretório que executarmos o script. Além disso, podemos também usar o **for** para iterar sob uma sequência pré-determinada:

```bash
for i in {0..20..4}
do 
    printf "$i\t"
done
```

Serão impressos os valores de **0** até **20**, iterando de 4 em 4.

```
0	4	8	12	16	20	
```

#### Recebendo Input do Usuário

Obter o *Input* do usuário é crucial para implementar a interação do usuário em nossos scripts, para isso contamos com o auxílio do comando **read**:

```bash
#!/bin/bash

echo -n "Informe seu nome: "
read nome

echo "Você informou $nome com ${#nome} caracteres"
```

O *Input* é então armazenado dentro da variável **nome** e pode ser acessado usando o sinal `$`, neste caso estamos imprimindo o `$nome` digitado e a quantidade de caracteres presente nele `${#nome}`.

#### Declaração If

As instruções **if** são uma construção condicional disponível no Bash, elas nos permitem alterar o fluxo de nosso programa. As instruções são executadas apenas se determinada condição for verdadeira. A palavra-chave **fi** é usada para marcar o final da instrução **if**.

```bash
#!/bin/bash

echo -n "Escolha um número: "
read n

if [[ ( $n -eq 13 || $n -eq 27 ) ]]
then
	echo "Número vencedor"
else
	echo "Número incorreto!"
fi
```

O programa acima irá imprimir `Número vencedor` se o usuário digitar o número **13** OU **27**, caso contrário ele irá imprimir `Número incorreto!`.

O operador **-eq** quer dizer **equal** ou igualdade.

Abaixo estão alguns dos operadores mais comumente usados:

- `-n VAR` - Verdadeiro se o comprimento de VAR for maior que zero.
- `-z VAR` - Verdadeiro se o VAR estiver vazio.
- `STRING1 = STRING2` - Verdadeiro se STRING1 e STRING2 forem iguais.
- `STRING1 != STRING2` - Verdadeiro se STRING1 e STRING2 forem diferentes.
- `INTEGER1 -eq INTEGER2` - Verdadeiro se INTEGER1 e INTEGER2 forem iguais.
- `INTEGER1 -gt INTEGER2` - Verdadeiro se INTEGER1 for maior que INTEGER2.
- `INTEGER1 -lt INTEGER2` - Verdadeiro se INTEGER1 for menor que INTEGER2.
- `INTEGER1 -ge INTEGER2` - Verdadeiro se INTEGER1 for maior ou igual que INTEGER2.
- `INTEGER1 -le INTEGER2` - Verdadeiro se INTEGER1 for menor ou igual que INTEGER2.
- `-h ARQUIVO` - Verdadeiro se o ARQUIVO existe e é um link simbólico.
- `-r ARQUIVO` - Verdadeiro se o ARQUIVO existe e é legível.
- `-w ARQUIVO` - Verdadeiro se o ARQUIVO existe e é gravável.
- `-x ARQUIVO` - Verdadeiro se o ARQUIVO existe e é executável.
- `-d ARQUIVO` - Verdadeiro se o ARQUIVO existe e é um diretório.
- `-e ARQUIVO` - Verdadeiro se o ARQUIVO existe e é um arquivo, independentemente do tipo (node, diretório, socket, etc).
- `-f ARQUIVO` - Verdadeiro se o ARQUIVO existe e é um arquivo normal (não um diretório ou dispositivo).

#### O Operador AND

O operador AND permite que nosso programa verifique se várias condições são satisfeitas de uma vez ou não. Todas as partes separadas por um operador AND devem ser verdadeiras. Caso contrário, a instrução que contém o AND retornará falso.

Por exemplo:

```bash
#!/bin/bash

echo -n "Informe um número: "
read num

if [[ ( $num -ge 0 ) && ( $num%2 -eq 0 ) ]]
then
	echo "Número é par e positivo"
elif [[ (( $num -lt 0 )) ]]
then 
	echo "Número é negativo"
else
	echo "Número é ímpar"
fi
```

Para o comando `echo "Número é par e positivo"` ser executado, é necessário que a variável **num** seja maior que **0** e também o resto de divisão por **2** (`$num%2`) deve ser igual a **0**. Caso estas condições sejam falsas, iremos para o **elif**, que testará se **num** é menor ou igual a **0**, caso seja falso, o **else** será executado.

O operador **AND** é denotado pelo sinal **&&**, no exemplo anterior vimos o operador **OR** que é denotado pelo sinal **||**, ao contrário de AND, uma instrução que consiste do operador OR retorna verdadeiro quando pelo menos um de seus operandos é verdadeiro. Ele retorna falso apenas quando todos os operandos separado por OR são falsos.

#### Switch

O constructo **switch** é outro recurso poderoso oferecido pelos scripts bash.

Ele pode ser usado onde as condições aninhadas são necessárias, mas você não quer usar cadeias **if-else-elif** complexas. Vejamos um exemplo para compreendermos melhor:

```bash
#!/bin/bash

echo -n "Informe uma opção (1, 2 ou 3): "
read num

case $num in
1)
echo "Opção 1 Selecionada";;
2)
echo "Opção 2 Selecionada";;
3)
echo "Opção 3 Selecionada";;
*)
echo "Opção inexistente";;
esac
```

As condições são escritas entre as palavras-chave **case** e **esac**. A condição `*)` é usada para corresponder todos os *inputs* que não sejam `1, 2 ou 3`.

#### Capturando Argumentos 

Obter argumentos diretamente do shell de comando pode ser interessante em vários casos. 

```bash
#!/bin/bash

echo "Total de argumentos = $#"
echo "Primeiro argumento = $1"
echo "Segundo argumento = $2"
echo "Terceiro argumento = $3"
```

Executamos este script da seguinte forma `bash arguments.sh 1 2 3` ou `./arguments.sh 1 2 3`. Perceba que **$1** é usado para acessar o primeiro argumento, **$2** para o segundo e assim por diante. O **$#** é usado para obter o número total de argumentos.

#### Argumentos com Nomes

O exemplo a seguir mostra como obter argumentos de linha de comando com seus respectivos nomes.

```bash
#!/bin/bash

for arg in "$@"
do
index=$(echo $arg | cut -f1 -d=)
valor=$(echo $arg | cut -f2 -d=)
case $index in
X | x) x=$valor;;
Y | y) y=$valor;;
*)
esac
done
((z=x+y))
echo "$x+$y=$z"
```

Podemos então executá-lo:

```bash
./named_arguments.sh x=1 y=2 # 1+2=3
bash named_arguments.sh X=3 Y=4 # 3+4=7
```

Os argumentos neste caso são armazenados dentro de **$@** e o script os busca usando o comando **cut** do Linux.

#### Concatenando Strings

O processamento de strings é de extrema importância para uma ampla variedade de scripts bash modernos. Felizmente este processamento é muito confortável no bash e permite uma maneira precisa e concisa de implementá-lo. Por exemplo:

```bash
#!/bin/bash

sistema="Linux"
linguagem="C"

echo "O ${sistema} foi escrito com a linguagem ${linguagem}"
```

O script acima irá imprimir `O Linux foi escrito com a linguagem C` em nosso terminal.

#### Slicing de Strings

Ao contrário de muitas linguagens de programação, o bash não fornece nenhuma função embutida para cortar partes de uma string. O exemplo a seguir demonstra como isso pode ser feito usando a expansão de parâmetros.

```bash
#!/bin/bash

string="Programação com Bash"
substring=${string:0:12}
echo $substring
```

Este script irá imprimir apenas `Programação` em nosso tela. A expansão do parâmetro assume a forma `${VAR:S:L}`. Onde, **S** denota a posição inicial e **L** indica o comprimento.

Podemos ainda usar [Parameter expansion](http://wiki.bash-hackers.org/syntax/pe) para manipular caminhos de nosso sistema:

```bash
STR="/arquivos/teste/main.cpp"
echo ${STR%.cpp}    # /arquivos/teste/main
echo ${STR%.cpp}.o  # /arquivos/teste/main.o
echo ${STR%/*}      # /arquivos/teste

echo ${STR##*.}     # cpp (extensão)
echo ${STR##*/}     # main.cpp (basepath)

echo ${STR#*/}      # arquivos/teste/main.cpp
echo ${STR##*/}     # main.cpp

echo ${STR/main/tests} # /arquivos/teste/tests.cpp

SRC="/arquivos/teste/main.cpp" # /arquivos/teste/main.cpp
BASE=${SRC##*/}   # main.cpp (basepath)
DIR=${SRC%$BASE}  # /arquivos/teste/ (dirpath)

echo $SRC $BASE $DIR
```

#### Manipulando Strings

- `,` - Altera o primeiro caractere para *lowercase*
- `,,` - Altera todos os caracteres para *lowercase*
- `^` - Altera o primeiro caractere para *uppercase*
- `^^` - Altera todos os caracteres para *uppercase*

```bash
STR="BASH"
echo ${STR,} # bASH
echo ${STR,,} # bash

STR="programming!"
echo ${STR^} # Programming!
echo ${STR^^} # PROGRAMMING!
```

#### Extraindo Substrings com Cut

O comando **cut** do Linux pode ser usado dentro dos scripts para "cortar" uma parte de uma string, também conhecida como substring. O exemplo a seguir mostra como podemos usá-lo:

```bash
#!/bin/bash
string="Coluna1 Coluna2 Coluna3"
substring=$(echo $string | cut -d ' ' -f 1-3)
echo $substring
```

Neste exemplo específico, selecionamos o delimitador espaço `' '` com a opção **-d** e dizemos a ele que desejamos selecionar os campos **1** até **3** (`1-3`) com a opção **-f**.

#### Adicionando Múltiplos Valores

Podemos usar um **for** loop para calcular a soma de uma sequência de números:

```bash
#!/bin/bash
soma=0
for (( i=1; i<=36; i++ ))
do
	(( soma+=i ))
	echo -n "$i "
done
printf "\n"
echo "Total = $soma"
```

Que ira nos trazer como *output*:

```
1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 
Total = 666
```

#### Funções em Bash

Como em muitas linguagens de programação, as funções desempenham um papel essencial nos scripts bash. Eles permitem que os programadores criem blocos de código personalizados para uso frequente. Vejamos uma demonstração:

```bash
#!/bin/bash

function Quadrado() {
	echo Função $FUNCNAME!
	echo -n "Informe um número -> "
	read x
	echo "$x² = $(( x**2 ))"
}

function Soma {
	(( x=$1+$2 )) 
	echo "$1 + $2 = $x"
}

Quadrado
soma=$(Soma 2 13)
echo $soma
```

Definimos duas funções:

- **Quadrado**: Responsável por receber *input* do usuário e elevar o número informado ao quadrado. 
- **Soma**: Responsável por somar dois números recebidos via parâmetro.

Em seguida, invocamos a função `Quadrado` sem informar nenhum parâmetro, invocamos a função `Soma` passando os parâmetros **2** e **13** e atribuindo o seu resultado à variável **soma** que é impressa com o comando **echo**.

#### Criação de Diretórios com Scripts Bash

A habilidade de executar comandos do sistema usando scripts de shell permite que nós desenvolvedores sejamos muito produtivos. O exemplo a seguir mostra como criar um diretório a partir de um script de shell:

```bash
#!/bin/bash

echo -n "Informe o nome do diretório ->"
read dir

if [ -d "$dir" ]
then
	echo "Diretório já existente"
else
	`mkdir $dir`
	echo "Diretório criado com sucesso!"
fi
```

Veja que estamos testando pela existência do diretório, caso já exista um de mesmo nome iremos retornar `"Diretório já existente"`, caso contrário usamos o comando **mkdir** para criar o diretório de nome fornecido pelo usuário.

Podemos ainda escrever este script de forma simplificada:

```bash
#!/bin/bash
echo -n "Informe o nome do dir: "
read newdir
cmd="mkdir $newdir"
eval $cmd
```

**eval** é um comando embutido do Linux que é usado para executar argumentos como um comando shell. Ele combina argumentos em uma única string e os usa como *input* para o shell e executa os comandos.

#### Lendo Arquivos

Os scripts Bash permitem que os usuários leiam os arquivos de forma muito eficaz. O exemplo a seguir mostra como ler um arquivo. 

Como exemplo vamos criar um arquivo `editores.txt` com o comando `touch editores.txt` e vamos inserir nele o seguinte conteúdo:

```
Sublime Text
Visual Studio Code
Atom
Vim
Emacs
```

Nosso script irá imprimir todas as linhas de nosso arquivo acima com seu respectivo número de linha, armazenado na variável **n**.

```bash
#!/bin/bash

filename='files/editores.txt'
n=1
cat $filename | while read line || [[ -n $line ]]
do
	echo "Linha $n -> $line"
	n=$((n+1))
done
```

#### Testando pela Existência de um Arquivo

Para checarmos se um determinado arquivo existe em nossa máquina podemos utilizar o seguinte script:

```bash
#!/bin/bash

filename=$1
if [ -f "$filename" ]; then
	echo "Arquivo existe"
else
	echo "Arquivo não existe"
fi
```

Observe que estamos passando o nome do arquivo como argumento através da linha de comandos.

```bash
bash file_existance.sh while.sh # Arquivo existe
bash file_existance.sh teste.sh # Arquivo não existe
```

#### Enviando Emails

Podemos utilizar a ferramenta **mail** para enviarmos emails através de scripts. Por exemplo:

```bash
#!/bin/bash
recipient='gabrielfelippe90@gmail.com'
subject='Desenvolvimento de Software'
message='Vamos desenvolver um projeto juntos?'
`mail -s $subject $recipient <<< $message`
```

Ele enviará um e-mail para o **destinatário** contendo o **assunto** e a **mensagem** fornecidos.

#### Data e Hora

O próximo exemplo de script bash mostra como trabalhamos com datas e horas. O comando **date** do Linux é usado para obter as informações necessárias e nosso programa faz o *parsing* dos dados.

```bash
#!/bin/bash

ano=`date +%Y`
mes=`date +%m`
dia=`date +%d`
hora=`date +%H`
minuto=`date +%M`
segundo=`date +%S`

echo `date`
echo "Data atual: $dia-$mes-$ano"
echo "Horário atual: $hora:$minuto:$segundo"
```

Obteremos como *output*: 

- o resultado completo do comando **date**
- a data atual no formato `dia-mês-ano` 
- e o horário atual no formato `hora:minuto:segundo`

#### O Comando Sleep

O comando **sleep** permite que seu script de shell faça uma pausa entre as instruções. É útil em vários cenários, como a execução de *system-level jobs*.

```bash
#!/bin/bash

echo "Quanto tempo de espera?"
read time
sleep $time
echo "Esperados $time segundos!"
```

#### Mostrando o Último Arquivo Alterado

Às vezes precisamos encontrar o último arquivo atualizado. O programa simples a seguir nos mostra como fazer isso no bash usando o comando **awk**. Ele irá listar o último arquivo atualizado ou criado em seu diretório de trabalho atual.

```bash
#!/bin/bash
ls -lrt | grep ^- | awk 'END{print $NF}'
```

**awk** será responsável por filtrar a lista de arquivos e nos trazer aquele que foi alterado mais recente.

#### Adicionando Extensões

O exemplo a seguir aplicará a extensão `.py` a todos os arquivos dentro do diretório que for passado como argumento.

```bash
#!/bin/bash

# Recebe um diretório como argumento
# Altera a extensão dos arquivos para .py
for file in `ls $1/*`
do
	mv $file $file.py
done
```

Podemos executar o script da seguinte forma:

```bash
./extensions arquivos/
bash extensions.sh arquivos/
```

**Importante**: Atenção para o diretório que você irá usar!

#### Imprimir Número de Arquivos e Diretórios

O script bash a seguir é capaz de encontrar o número de arquivos e diretórios presentes em um determinado diretório. Ele utiliza o comando **find** do Linux. Precisamos passar o nome do diretório onde desejamos pesquisar os arquivos na linha de comando, caso contrário ele irá usar o *current working directory*.

```bash
#!/bin/bash

# encontra o número de arquivos ou diretórios 
# presentes em um determinado diretório.
if [ -d "$@" ]; then
	echo "Arquivos encontrados: $(find "$@" -type f | wc -l)"
	echo "Diretórios encontrados: $(find "$@" -type d | wc -l)"
else
	echo "Erro. Informe outro diretório."
	exit 1
fi
```

Para executá-lo é muito simples:

```bash
bash files_directories.sh
./files_directories.sh
bash files_directories.sh files/
```

#### Backup com Bash

Os *shell scripts* fornecem uma maneira robusta de fazer backup de nossos arquivos e diretórios. O exemplo a seguir fará o backup de cada arquivo ou diretório que foi modificado nas últimas 24 horas. Este programa utiliza o comando **find** para realizar essas tarefas.

```bash
#!/bin/bash

backupfile=backup-$(date +%m-%d-%Y)
archive=${1:-$backupfile}

find . -mtime -1 -type f -print0 | xargs -0 tar rvf "$archive.tar"
echo "Directory $PWD backed up in archive file \"$archive.tar.gz\"."
exit 0
```

#### Checando por Root

O exemplo a seguir demonstra uma maneira rápida de descobrir se um usuário é root ou não:

```bash
#!/bin/bash
ROOT_UID=0

if [ "$UID" -eq "$ROOT_UID" ]
then
	echo "You are root."
else
	echo "You are not root"
fi
exit 0
```

O *output* desse script depende do usuário que o executa. Ele corresponderá ao usuário root com base no **$UID**.

#### Manutenção do Sistema

Podemos usar um simples script para executar as rotinas básicas de atualização de nosso sistema. Por exemplo:

```bash
#!/bin/bash

echo -e "\n$(date "+%d-%m-%Y --- %T") Iniciando Atualização\n"

apt update
apt upgrade

apt autoremove
apt autoclean

echo -e "\n$(date "+%T") Script finalizado"
```

O script também cuida de pacotes antigos que não são mais necessários. Precisamos executar este script usando o **sudo**, caso contrário ele não funcionará corretamente.

#### Arrays

O array é uma variável que contém vários valores que podem ser do mesmo tipo ou de tipos diferentes. Não há limite máximo para o tamanho de um array, nem qualquer requisito de que as variáveis de membro sejam indexadas ou atribuídas de forma contígua. O índice do array começa com zero.

O exemplo a seguir nos mostra como podemos usar os arrays no Bash:

```bash
#!/bin/bash

# Definindo o array de arquivos
arquivos=( "/etc/passwd" "/etc/group" "/etc/hosts" )

# Extraindo o tamanho do array
tamanho_array=${#arquivos[@]}

# Extraindo cada elemento do array
elemento1=${arquivos[0]}
elemento2=${arquivos[1]}
elemento3=${arquivos[2]}

# Imprimindo elementos individualmente
echo $elemento1, $elemento2, $elemento3

# Percorrendo todos os elementos com for
for i in "${arquivos[@]}"
do
	echo $i
done

# Percorrendo todos os elementos com for
for (( i=0; i<$tamanho_array; i++))
do
	echo ${arquivos[${i}]}
done
```

#### Números Aleatórios

O Bash fornece uma variável global $RANDOM que imprime um número aleatório entre 0 e 32.767 toda vez que o acessamos.

```bash
#!/bin/bash
echo $RANDOM $RANDOM $RANDOM 

# número aleatório entre 0-10
echo $(($RANDOM % 11))
```

#### Checando o Resultado de um Comando:

Neste exemplo se o comando **ping** executar com sucesso então executaremos o comando `echo "Internet está operando."` do bloco **if**.

```bash
if ping -c 1 google.com; then
  echo "Internet está operando."
fi
```

Os scripts Bash apresentados nesse artigo podem ser encontrados no seguinte diretório **[Scripts](https://github.com/the-akira/Comandos-Bash/tree/master/Scripts)**