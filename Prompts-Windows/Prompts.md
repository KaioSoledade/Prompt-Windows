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

## Tema 7

Durante o vídeo Tratando erros, criamos o seguinte script:

```
@echo off
echo `Compactando arquivos`
tar -cf notas.zip *.xml  2>erros.txt

IF %ERRORLEVEL% NEQ 0 (echo "Erro na execução do script.")
```

Agora vamos entender em detalhes cada uma das linhas desse script:

```
@echo off
```

Com esse comando desabilitamos a exibição dos comandos no prompt do Windows relacionados ao conteúdo das instruções contidas no arquivo.

Vamos usar como exemplo o script ``exemplo.bat``, com o conteúdo ``echo Olá Mundo!``. Ao executarmos esse simples script, teremos como retorno o seguinte:

```
c:\Users\Emerson\Desktop>.\exemplo.bat

c:\Users\Emerson\Desktop>echo Olá Mundo
Olá Mundo

c:\Users\Emerson\Desktop>
```

Ao adicionarmos o ``@echo off``, teremos como resultado:

```
c:\Users\Emerson\Desktop>.\exemplo.bat
Olá Mundo

c:\Users\Emerson\Desktop>
```

Perceba que não é exibido qual é o comando dentro do arquivo, apenas o seu resultado.

```
echo `Compactando arquivos`
```

Com este comando, exibimos uma mensagem para o usuário sobre a compactação.

```
tar -cf notas.zip *.xml  2>erros.txt`
```

Para lidar com arquivos compactados, usamos o comando ``tar``. Podemos ver mais detalhes com o comando ``tar /?``, que retorna as seguintes informações:

```
C:\Users\Emerson\Desktop>tar /? 

Usage:

List: tar -tf <archive-filename>
Extract: tar -xf <archive-filename>
Create: tar -cf <archive-filename> [filenames…]
Help: tar --help
```

Visto que queremos compactar um arquivo, usamos as flags ``cf``.

O próximo argumento, o ``notas.zip``, é o nome do arquivo quando for compactado, seguido do que eu quero compactar, no caso, ``*.xml``. Com isso, estamos falando que todos os arquivos que terminam com a extensão ``.xml`` serão compactados.

Finalizando o comando, temos ``2>erros.txt``, que nos diz que estamos redirecionando a saída do comando (ou seja, pegando o resultado gerado pelo ``tar`` e levando para algum lugar).
```
IF %ERRORLEVEL% NEQ 0 (echo "Erro na execução do script.")
```

E, por fim, fazemos uma condição representada pelo ``IF``, indicando que se o conteúdo da variável ``ERRORLEVEL`` não for igual (``NEQ``, ou seja, Not EQual to) a zero, nós exibimos uma mensagem à pessoa informando que não foi possível encontrar os arquivos.

Quase todos os aplicativos e utilitários definirão um código de saída representado pela variável ``ERRORLEVEL``. Quando seu valor é zero, indica que houve sucesso na execução. Como estamos avaliando o caso de ser diferente de zero, estamos tratando justamente quando houver algum erro.

## Tema 8

Quando trabalhamos com script é comum precisarmos armazenar uma informação de forma temporária.

Para isso, nosso computador oferece um espaço de memória chamado variávies, justamente para podermos colocar uma informação no mesmo espaço de memória e depois sobrepor com outra informação.

Isso acontece quando criamos nossos scripts e também em programas externos, como Java e Python, por exemplo.

Aprenderemos de forma prática como trabalhar com essas variáveis. Para isso, vamos criar um script no qual armazenaremos uma variável chamada nome com uma informação e outra variável e-mailcom outra informação. Por fim, exibiremos uma mensagem com essas duas variáveis para o usuário final.

André: Bacana, Emerson. E como criamos uma variável no terminal do Windows Prompt?

Emerson: Primeiro apertamos a tecla "Windows". No campo de busca, digitamos "cmd" e apertamos a tecla "Enter". Na área de trabalho escrevemos cd Desktop e apertamos "Enter" novamente.

Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

C:\Users\Emerson>cd DesktopCOPIAR CÓDIGO
Feito isso, temos:

Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

C:\Users\Emerson>cd\Desktop>COPIAR CÓDIGO
Agora, para criar nossa primeira variável precisaremos de um novo comando, o set. Em seguida ele precisa receber o nome da variável que queremos criar. Nesse caso ela se chamará mensagem.

Depois, inserimos o sinal = para atribuir, ou seja, dar um valor a essa variável e escrevemos Olá Mundo!

Microsoft Windows [versão 10.0.2200.1335]
(c) Microsoft Corporation. Todos os direitos reservados.

C:\Users\Emerson>cd Desktop

C:\Users\Emerson>cd\Desktop>set mensagem=Olá Mundo!COPIAR CÓDIGO
Em seguida, apertamos a tecla "Enter" e assim temos a variável criada.

André: Mas, como conseguimos acessar o conteúdo que você atribuiu a essa variável mensagem ?

Emerson: Para exibirmos um conteúdo no nosso Prompt, podemos usar o comando echo, como aprendemos anteriormente. Porém, para exibirmos o conteúdo dentro de uma variável precisamos colocá-la entre porcentagens.

Inserir uma variável entre símbolos de % permite a exibição do seu conteúdo, quando utilizado com o comando echo.

Então, digitamos o sinal %, depois escrevemos o nome da variável mensagem e novamente o sinal %.

// Código omitido

C:\Users\Emerson>cd\Desktop>echo %mensagem%COPIAR CÓDIGO
Ao apertar a tecla "Enter" ele exibira a mensagem:

Olá Mundo!

Se escrevermos %MENSAGEM%, com letras maiúsculas, teremos o mesmo retorno.

André: Agora que aprendemos a criar variáveis, vamos criar um script que permitirá a criação de um cadastro do nome e e-mail no Prompt.

Emerson: Vamos, sim. Para isso, abrimos o bloco de notas escrevendo notepade seguido da tecla "Enter".

C:\Users\Emerson>cd\Desktop>notepadCOPIAR CÓDIGO
Feito isso, o bloco de notas abre. Agora, vamos escrever todo o script e depois explicar linha por linha para entendermos exatamente o que ele faz.

@echo off 
rem limpando a tela
cls
set /p nome=Digite seu nome completo =
set /p email=Digite seu e-mail principal =
pause
echo Pressione [enter] para continuar
echo ..................................................................................
echo Seu nome é %nome% e seu e-mail %email%COPIAR CÓDIGO
Na primeira linha colocamos @echo off. Aprendemos anteriormente que ele serve para não exibir o comando e sim o resultado desse comando no nosso terminal.

Em seguida temos o rem Limpando a tela. Esse comando passa uma mensagem para quem está editando nosso script, ou seja, essa informação não será exibida, ela só ficará visível para a pessoa que for editar entender o próximo comando que é o cls, que limpará todo nosso terminal.

Na linha de baixo utilizamos o set para inserir uma informação em uma variável. Porém, nesse caso passamos parâmetro /p que permite com que o usuário informe um dado e ele seja armazenado na variável nome. Para o usuário aparecerá a mensagem Digite seu nome.

Sendo assim, o terminal irá esperar pela mensagem que será digitada pelo usuário. Depois que ele fizer isso e apertar a tecla "Enter" a informação será armazenada.

O mesmo acontece com o e-mail, que aparecerá para o usuário a mensagem Digite seu e-mail e a mensagem digitada será salva em e-mail.

Depois disso, damos um pause, simulando o comportamento de um terminal, que irá pausar e exibir a mensagem Pressione [enter] para continuar. Em seguida, aparecerá uma sequência de pontilhados e a informação final Seu nome é %nome% e seu e-mail %email%. Como estão entre sinais de porcentagem vão exibir o conteúdo das variáveis.

Para checar se está funcionando, na barra de menu, localizada no canto superior esquerdo da tela, clicamos em "Arquivo > Salvar como". Nomeamos de "script.bat" e clicamos em "Salvar".

Fechamos o bloco de notas e voltamos no nosso cmd. Nele, digitamos .\script.bat e apertamos "Enter".

C:\Users\Emerson>cd\Desktop>.\script.batCOPIAR CÓDIGO
Perceba que nosso terminal foi limpo e a primeira mensagem que aparece é Digite deu nome=.

Agora, escrevemos o nome Suellen e apertamos "Enter".

Digite seu nome=SuellenCOPIAR CÓDIGO
Em seguida aparece a mensagem Digite seu e-mail=. Preenchemos o campo com `suellen@email.com`.

Digite seu e-mail=suellen@email.comCOPIAR CÓDIGO
A mensagem seguinte é Pressione qualquer tecla para continuar..., uma mensagem padrão quando usamos o pause.

Digite seu nome=Suellen
Digite seu e-mail=suellen@email.com
Pressione qualquer tecla para continuar...
Pressione [enter] para continuar
COPIAR CÓDIGO
Feito isso, exibe a seguinte mensagem:

Seu nome é Suellen e seu e-mail suellen@email.com

André: Emerson, o que você acha de fazermos uma edição nesse script e deixar apenas a mensagem do pause para não ficar redundante?

Emerson: Vamos editá-lo, então. Para isso, vamos digitamos notepad script.bat e apertamos "Enter".

Com o bloco de notas aberto, removemos a linha echo Pressione [enter] para continuar. Salvamos e fechamos.

Em seguida, voltamos para o cmd. Utilizamos a seta para cima do teclado para encontrar o .\script.bar

C:\Users\Emerson>cd\Desktop>.\script.batCOPIAR CÓDIGO
Executamos apertando "Enter". Agora, vamos repetir o processo de preenchimento.

Em nome escrevemos Andre e em e-mail `andre@email.com. Aparece a mensagemPressione qualquer tecla para continuar` e feito isso obtemos o resultado.

Digite seu nome=Andre
Digite seu e-mail=andre@email.com
Pressione qualquer tecla para continuar...
..................................................................................
Seu nome é Andre e seu e-mail andre@email.com
COPIAR CÓDIGO
André: Muito bom, Emerson! Aprendemos muitas coisas. Você pode fazer um resumo de tudo?

Emerson: Claro, vamos lá. Começamos aprendendo a importância das variáveis, uma forma de trazer dinamismo quando trabalhamos com scrips nossos ou externos.

Com essas variáveis conseguimos armazenar informações que podemos exibir por meio do comando echo e a variável entre o símbolo de porcentagem.

Além disso, aprendemos como criar uma variável por meio do comando set. Para colocar tudo isso em prática, criamos um script para conseguir exibir para o usuário final a informação de nome e e-mail digitado.

André: Emerson, você pode executar novamente a exibição da variável mensagem no terminal?

Emerson: Vamos lá. Para isso digitamos echo %mensagem% e apertamos "Enter".

C:\Users\Emerson>echo %mensagem%COPIAR CÓDIGO
Feito isso, temos o seguinte retorno:

Olá Mundo!

André: Bacana! Agora, abre outro terminal e tenta acessar essa variável também.

Emerson: Apertamos a tecla "Windows", digitamos "cmd" e "Enter". Agora, digitamos echo %mensagem%.

Ele não exibe o conteúdo de uma variável, mas sim a própria mensagem que digitamos.

%mensagem%

André: É importante lembrarmos que essa variável só existe no terminal que criamos. Nesse segundo terminal que abrimos agora ela não existe, por isso tivemos esse retorno. Além disso, outro ponto importante é que as variáveis são temporárias, ou seja, se você fechar o primeiro terminal e tentar abrir de novo, você não terá acesso à variável que criou, pois ela não existirá mais.