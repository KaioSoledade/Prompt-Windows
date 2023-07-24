## Tema 1
Nesta aula, aprendemos os primeiros comandos no prompt de comando, entre eles, o cd (change directory), que nos permite mudar o diretório atual de trabalho para outro especificado. Se quisermos ir para a área de trabalho (Desktop), por exemplo, basta digitar: cd Desktop.

```
Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

c:\Users\Emerson>cd Desktop

c:\Users\Emerson\Desktop>
```

Observamos, ao abrir o cmd, que o ponto de partida é a pasta de usuário e que podemos voltar para o diretório anterior com o comando cd ...

```
Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

c:\Users\Emerson>cd Desktop

c:\Users\Emerson\Desktop>cd ..

c:\Users\Emerson>
```

Mas o que será que acontece se tentarmos voltar vários diretórios? Qual o diretório inicial que gera todos os outros?

```
Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

c:\Users\Emerson>cd Desktop

c:\Users\Emerson\Desktop>cd ..

c:\Users\Emerson>cd ..\..\..\..\..\..\..\..\..\..\..\..\..\..\..\..\..\..\
```

Se tentarmos voltar para o diretório anterior quantas vezes quisermos, pararemos no diretório C: que, para o sistema operacional Windows, é o primeiro ou mais alto diretório em uma hierarquia, o qual chamamos de diretório raiz.

Podemos compará-lo a uma árvore onde todos os ramos existentes partiram de uma raiz, assim todos os diretórios partem dessa pasta.

Ao abrir o cmd ou qualquer diretório que estivermos, podemos acessar o diretório raiz de forma prática através do comando cd /.

```
c:\Users\Emerson>cd /
c:\>
```

Caso queira visualizar o conteúdo desse diretório, basta usar o comando dir:

```
c:\dir
O volume na unidade C é Windows-SSD
O Número de Série do Volume é 5E18-9CE7

Pasta de c:\

15/05/2022 13:06   <DIR>      $WINDOWS.~BT
11/05/2022 13:41   <DIR>      Drivers
15/05/2022 07:01   <DIR>      Program Files
26/12/2022 18:28   <DIR>      Program Files (x86)
29/03/2022 07:01   <DIR>      Users
26/12/2022 07:01   <DIR>      Windows
```
            0 arquivo(s)               0 bytes
            6 pasta(s)  56.535.347.200 bytes disponíveis


E, aqui, vemos algumas pastas importantes para o funcionamento do nosso sistema, como:

Users: aqui estão as informações dos usuários existentes no computador. Diretórios como Documentos, Downloads, Música, Vídeo e qualquer arquivo na área de trabalho estão disponíveis nesta pasta.

Program Files: também conhecida como “Arquivos de Programas”, em português; por padrão, é a pasta para instalar aplicativos de terceiros no Windows. A pasta inclui diferentes opções de subpastas onde um aplicativo instalado é armazenado.

Program Files (x86): é outra opção de pasta disponível no diretório raiz que inclui aplicativos de 32 bits. Sempre que instalamos um aplicativo de 32 bits em um Windows de 64 bits, ele se move diretamente para os “Arquivos de Programas (x86)”.

Windows: este diretório é onde todos os arquivos principais do sistema operacional estão armazenados, incluindo a famosa pasta System32, entre outras.

## Tema 2
Quando estamos trabalhando com o prompt de comando temos à disposição diversos comandos. Um dos mais interessantes é o comando tree, que nos mostra a estrutura de pastas do sistema.

Vamos fazer mais um teste! No prompt, digite o comando tree:



![imagem de estrutura de pasta di sistema](Imagens/image1.png)


Dependendo do diretório atual, muitas informações podem aparecer; mas, repare que o comando tree mostra as pastas e subpastas organizadas em uma árvore.

O tree pode ser útil para entender a estrutura de um projeto. Com esse comando, você já pode ver facilmente como o projeto está organizado! É um recurso muito útil!

## Tema 3

O comando ``more`` funciona de forma semelhante ao comando ``type``, com a diferença de exibir página por página do arquivo no terminal, em vez de mostrá-lo todo de uma vez.

Para utilizar o comando, utilizamos o ``more`` seguido do nome do arquivo que se deseja exibir o conteúdo. Por exemplo: ``more arquivo.txt``.

Esse comando é muito útil quando queremos exibir arquivos de texto com várias linhas para ler lentamente, em vez de abri-lo todo no terminal de uma única vez.

Um exemplo disso é quando queremos ler os logs de uma aplicação que está em um servidor na nuvem; neste caso, é preciso ler grandes arquivos de texto linha a linha para identificar um bug ou realizar algum teste.

## Tema 4

Alguns dos principais comandos usados no dia a dia, porém, o cmd oferece diversos outros comandos, como:

``fc``: File Compare ou “Comparação de Arquivos” (em português); compara dois arquivos ou grupos de arquivos e mostra as diferenças entre eles. Caso não haja diferença, uma mensagem é exibida informando que nenhuma diferença foi encontrada. Por exemplo:
```
C:\Users\Emerson\Desktop>type a.txt
texto a

C:\Users\Emerson\Desktop>type b.txt
texto b

C:\Users\Emerson\Desktop>fc a.txt b.txt
Comparando os arquivos a.txt e B.TXT
***** a.txt
texto a
***** B.TXT
texto b
*****

C:\Users\Emerson\Desktop>fc a.txt a.txt
Comparando os arquivos a.txt e A.TXT
FC: nenhuma diferença encontrada
```


``systeminfo``: como o nome do comando sugere, ele traz informações em detalhes sobre o seu Windows.

``rmdir``: vimos o mkdir para criar um diretório, mas caso queiramos excluí-lo, usamos o rmdir (remove directory ou, em português, remover diretório).

``shutdown``: permite desligar ou reiniciar o computador de forma imediata ou agendada.

``date``: exibe a data atual e permite alterá-la. Por exemplo:

```
C:\Users\Emerson\Desktop>date
Data atual: 04/01/2023
Digite a nova data: (dd-mm-aa)  _
```

``find``: busca uma sequência de texto em um arquivo ou arquivos. Por exemplo:
```
C:\Users\Emerson\Desktop>type exemplo.txt
Estou muito feliz, pois estou aprendendo mais sobre o prompt de comando

C:\Users\Emerson\Desktop>find “triste” exemplo.txt
- - - - - - - - - -  EXEMPLO.TXT

C:\Users\Emerson\Desktop>find “feliz” exemplo.txt
- - - - - - - - - -  EXEMPLO.TXT
    Estou muito feliz, pois estou aprendendo mais sobre o prompt de comando
```
    
``exit``: fecha o cmd.

## Tema 5

Por que usar um terminal?
Conhecer o terminal de comandos é um recurso interessante, pois muitas ferramentas no setor de desenvolvimento não possuem uma interface gráfica.

### Abrir o prompt de comando
O primeiro passo é abrir um terminal (ou console). No mundo Windows, esse terminal se chama Prompt de comando ou, abreviando, cmd. Para abrir um novo terminal, devemos ir em Todos os Programas (ícone do Windows que normalmente fica no canto inferior esquerdo), digitarmos ``cmd`` e apertarmos Enter. Outra forma de abrir o Prompt é pelo atalho Botão Iniciar + R e no campo de pesquisa digitar ``cmd``.

### Listando arquivos
Para listar todos os arquivos em diretórios, usamos o comando ``dir`` e então recebemos uma lista dos arquivos e pastas existentes.

### Navegando entre diretórios
Para mudarmos de pasta, utilizamos o comando ``cd`` (change directory) seguido do nome da subpasta. Por exemplo: ``cd Documents`` . Para voltarmos ao diretório anterior, usamos o comando ``cd ...`` 

### Criando diretórios
Para criarmos diretórios, usamos o comando ``mkdir`` (make directory). Lembre-se de evitar acentos e espaços nos nomes de arquivos e diretórios. Uma boa boa prática é usar o caractere ``_`` ao invés do espaço ao criar diretórios.

### Trabalhando com arquivos
Para mover arquivos ou pastas, utilizamos o comando ``move`` e indicamos o arquivo com o nome completo (incluindo o caminho dos diretórios). Por exemplo: ``move ..\Desktop\texto.txt`` . Já para conferir o conteúdo de um arquivo, usamos o comando ``type``, como em ``type texto.txt``.

Para a função de copiar um arquivo, utilizamos o comando ``copy``, como em ``copy texto.txt texto2.txt``. Já para renomear um arquivo, utilizamos o comando ``rename`` seguido do nome original do arquivo e o nome que desejamos aplicar, como em ``rename texto2.txt mensagem.txt``. E, por fim, para apagar um arquivo, utilizamos o comando ``del`` seguido do nome do arquivo que se deseja deletar, por exemplo, ``del texto.txt``.

### Limpando o terminal
Com o tempo, o terminal vai ficar poluído com comandos antigos, que tiram o foco e dificultam a legibilidade. Para limpar o terminal, utilizamos ``cls`` (clear screen).

## Tema 6

Comando tar: compactando arquivos
Esse comando possui duas flags, ou parâmetros:

-``C``: indica que a ação que realizaremos naquele momento é a compactação de arquivos;

-``F``: para nomear o arquivo compactado ao final.

Vamos digitar esse comando no nosso terminal e, para indicar que queremos inserir algumas informações especiais, usamos a flag. Com ela, conseguimos utilizar várias funcionalidades com o mesmo comando.

Por exemplo, queremos usar o comando tar para compactar. Mas, com esse mesmo comando, podemos mudar as flags para tanto descompactar como listar o conteúdo de um arquivo compactado.

Para compactar, digitamos um hífen (``-``) indicando que queremos inserir uma flag para esse comando, junto da letra ``c``, flag de compactação. Damos um espaço e digitamos mais um hífen com a flag ``f``, de nomeação: tar ``-c`` ``-f``

Podemos construir o comando desse jeito ou unificar as flags, digitando o hífen apenas uma vez e inserindo as flags em sequência: tar ``-cf``.

O próximo parâmetro que esse comando exige é o nome do arquivo compactado. Vamos nomeá-lo como "notas" junto da extensão ``.zip``, usada para compactar arquivos.

Por fim, passamos o que, afinal, queremos compactar. No caso, são os nossos dois arquivos XML: ``NF001.xml`` e ``NF002.xml``.

Nosso comando ficou assim:

```
Desktop>tar -cf notas.zip NF001.xml NF002.xml
```
Agora, podemos apertar "Enter" para executá-lo. Não teremos nenhuma resposta do terminal; mas, se digitarmos o comando dir para verificar o conteúdo do Desktop, encontraremos:

```
Pasta de C:\Users\Emerson\Desktop

26/12/2022 10:13 83 NF001.xml
26/12/2022 10:13 83 NF002.xml
26/12/2022 15:43 3.072 notas.zip
3 arquivo(s) 3.238 bytes
```

Ou seja, o nosso arquivo compactado ``notas.zip`` foi criado.
