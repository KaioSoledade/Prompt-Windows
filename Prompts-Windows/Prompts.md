## Tema `cd`
**Guia para Utilizar o Comando `cd` no Prompt de Comando do Windows**

O comando `cd` (change directory) é uma das funcionalidades essenciais do Prompt de Comando do Windows que permite navegar entre pastas e diretórios do sistema operacional. Com este comando, é possível alterar o diretório de trabalho atual para qualquer outro diretório desejado. A seguir, vamos aprender como utilizar o `cd` de forma prática:

1. **Visualizando o Diretório Atual:**
   Para começar, abra o Prompt de Comando do Windows. Ao executá-lo, você será apresentado à localização inicial, geralmente a pasta do usuário. Para visualizar o diretório atual, digite o seguinte comando e pressione "Enter":
   ```
   cd
   ```
   Isso exibirá o caminho completo do diretório atual.

2. **Navegando Entre Diretórios:**
   Para mudar de diretório, você pode usar o comando `cd` seguido do caminho do diretório que deseja acessar. Se o diretório estiver em um caminho absoluto, você pode digitar o caminho completo:
   ```
   cd C:\Exemplo\Pasta
   ```
   Isso o levará diretamente para a pasta "Pasta" localizada no disco C. Se o caminho estiver relativo ao diretório atual, você pode simplesmente digitar o nome da pasta desejada:
   ```
   cd Exemplo
   ```
   Isso o levará para dentro da pasta "Exemplo," assumindo que ela está no diretório atual.

3. **Voltando para o Diretório Anterior:**
   Se você quiser voltar para o diretório anterior, pode utilizar o comando `cd ..`:
   ```
   cd ..
   ```
   Esse comando o levará uma pasta acima na hierarquia de diretórios.

4. **Voltando para o Diretório Raiz:**
   Para retornar ao diretório raiz do sistema, basta digitar o seguinte comando:
   ```
   cd \
   ```
   Isso o levará diretamente para o diretório raiz do disco atual.

5. **Navegando Entre Unidades de Disco:**
   No Windows, você pode ter várias unidades de disco (por exemplo, C:, D:, E:, etc.). Para navegar entre elas no Prompt de Comando, basta digitar a letra da unidade seguida de dois-pontos:
   ```
   D:
   ```
   Isso o levará para o diretório raiz da unidade D.

6. **Diretórios com Espaços e Caracteres Especiais:**
   Se o nome de algum diretório contiver espaços ou caracteres especiais, é necessário colocar o caminho entre aspas duplas:
   ```
   cd "C:\Meus Documentos"
   ```

7. **Autocompletar de Nomes de Diretórios:**
   Para facilitar a navegação, o Prompt de Comando possui uma funcionalidade de autocompletar nomes de diretórios. Basta digitar as primeiras letras do nome do diretório e pressionar a tecla "Tab" para que o sistema complemente o restante do nome automaticamente.

8. **Listando o Conteúdo de um Diretório:**
   Para visualizar o conteúdo de um diretório sem alterar o diretório atual, você pode usar o comando `dir`. Isso mostrará os arquivos e pastas presentes no diretório atual.

9. **Exemplos Práticos:**
   - Navegar para a pasta "Documentos":
     ```
     cd C:\Users\SeuUsuario\Documents
     ```
   - Voltar uma pasta acima:
     ```
     cd ..
     ```
   - Navegar para a unidade D:
     ```
     D:
     ```
   - Navegar para a pasta "Program Files":
     ```
     cd "C:\Program Files"
     ```

O comando `cd` é uma ferramenta poderosa para a navegação eficiente entre diretórios no Prompt de Comando do Windows. Com este guia, você está pronto para explorar e trabalhar com facilidade nos diretórios do sistema. Lembre-se de praticar e experimentar com os comandos para se tornar mais confiante no uso do `cd`.

## Tema `Dir`

**Guia para Utilizar o Comando `dir` no Prompt de Comando do Windows**

O comando `dir` é uma ferramenta essencial do Prompt de Comando do Windows que permite listar o conteúdo de um diretório específico. Com este comando, você pode visualizar os arquivos e pastas presentes em um diretório, bem como suas propriedades e informações relevantes. A seguir, vamos aprender como utilizar o `dir` de forma prática:

1. **Listando o Conteúdo do Diretório Atual:**
   Para visualizar o conteúdo do diretório atual, basta abrir o Prompt de Comando e digitar o seguinte comando:
   ```
   dir
   ```
   Ao pressionar "Enter", o Prompt de Comando mostrará uma lista detalhada de todos os arquivos e pastas presentes no diretório em que você está posicionado.

2. **Listando o Conteúdo de um Diretório Específico:**
   Para listar o conteúdo de um diretório específico, você precisa fornecer o caminho absoluto ou relativo do diretório após o comando `dir`. Por exemplo:
   ```
   dir C:\Exemplo\Pasta
   ```
   Esse comando exibirá a lista de arquivos e pastas dentro do diretório "Pasta" localizado no caminho C:\Exemplo.

3. **Opções para Exibir Detalhes:**
   O comando `dir` pode ser usado com diversas opções para exibir informações adicionais sobre os arquivos e pastas listados. Algumas opções úteis são:
   - `/W`: Exibe a lista em formato de colunas.
   - `/P`: Exibe a lista por páginas, pausando após cada tela cheia.
   - `/A`: Exibe arquivos e pastas ocultos.
   - `/S`: Lista o conteúdo de forma recursiva, mostrando também o conteúdo de subpastas.

4. **Filtrando a Listagem:**
   Você pode filtrar a listagem de arquivos usando caracteres curinga, como `*` e `?`, para corresponder a nomes de arquivo específicos. Por exemplo:
   ```
   dir *.txt
   ```
   Isso exibirá apenas os arquivos com extensão ".txt" no diretório atual.

5. **Redirecionando a Saída:**
   Assim como outros comandos, você pode redirecionar a saída do comando `dir` para um arquivo de texto, em vez de exibi-la no prompt. Basta usar o operador de redirecionamento `>` seguido do nome do arquivo. Por exemplo:
   ```
   dir > lista.txt
   ```
   Esse comando criará um arquivo chamado "lista.txt" contendo a lista de arquivos e pastas do diretório atual.

6. **Ordenando a Listagem:**
   Se você deseja ordenar a lista de arquivos, pode usar a opção `/O`. Por exemplo, para listar os arquivos por tamanho, use:
   ```
   dir /O:S
   ```
   Isso classificará os arquivos por tamanho, mostrando os maiores primeiro.

7. **Exemplos Práticos:**
   - Listar o conteúdo do diretório atual:
     ```
     dir
     ```
   - Listar o conteúdo do diretório "Downloads":
     ```
     dir C:\Users\SeuUsuario\Downloads
     ```
   - Listar arquivos com extensão ".docx" no diretório atual:
     ```
     dir *.docx
     ```
   - Listar conteúdo de forma recursiva, incluindo subpastas:
     ```
     dir /S
     ```
   - Redirecionar a listagem para um arquivo de texto:
     ```
     dir > lista_de_arquivos.txt
     ```

O comando `dir` é uma ferramenta poderosa para visualizar e gerenciar o conteúdo de diretórios no Prompt de Comando do Windows. Experimente as opções disponíveis e torne-se mais eficiente em sua navegação e organização de arquivos e pastas. Pratique regularmente e explore todas as funcionalidades que o `dir` tem a oferecer!

![imagem de estrutura de pastas do sistema, usando dir](Imagens/DIR-CMD.png)

## Tema `More`

**Guia para Utilizar o Comando `more` no Prompt de Comando do Windows**

O comando `more` é uma ferramenta útil do Prompt de Comando do Windows que permite visualizar o conteúdo de arquivos de texto de forma paginada. Ele é especialmente útil quando você deseja ler arquivos extensos linha por linha, evitando que o conteúdo se sobreponha rapidamente no prompt. A seguir, vamos aprender como utilizar o `more` de forma prática:

1. **Exibindo o Conteúdo Completo de um Arquivo de Texto:**
   Para visualizar o conteúdo completo de um arquivo de texto no Prompt de Comando, basta digitar o seguinte comando, seguido do nome do arquivo:
   ```
   more nome_do_arquivo.txt
   ```
   Ao pressionar "Enter", o Prompt de Comando exibirá o conteúdo completo do arquivo. Você pode navegar pelas linhas usando as teclas "Seta para Baixo" ou "Barra de Espaço".

2. **Visualizando o Conteúdo de Forma Paginada:**
   Por padrão, o `more` exibe o conteúdo do arquivo de forma paginada, mostrando uma tela de cada vez. Quando o final da primeira tela é atingido, você pode pressionar a tecla "Barra de Espaço" para avançar uma tela, ou a tecla "Enter" para avançar uma linha por vez.

3. **Navegando Pelo Conteúdo:**
   Além das teclas mencionadas acima, você pode usar as teclas "Seta para Cima" para voltar uma linha, e "Q" para sair do modo de visualização e retornar ao prompt do comando.

4. **Utilizando o Redirecionamento de Saída:**
   O comando `more` também pode ser usado em conjunto com o redirecionamento de saída para exibir o conteúdo de um arquivo paginado em um novo arquivo de texto. Por exemplo:
   ```
   more nome_do_arquivo.txt > arquivo_paginado.txt
   ```
   Esse comando criará um novo arquivo chamado "arquivo_paginado.txt" contendo o conteúdo do arquivo original exibido de forma paginada.

5. **Exemplos Práticos:**
   - Visualizar o conteúdo completo de um arquivo:
     ```
     more texto.txt
     ```
   - Visualizar o conteúdo de um arquivo paginado:
     ```
     more longo_texto.txt
     ```
   - Navegar pelo conteúdo paginado:
     ```
     more arquivo.txt
     ```
     (Pressione "Barra de Espaço" para avançar, "Seta para Cima" para voltar, "Q" para sair)
   - Redirecionar a saída paginada para um novo arquivo:
     ```
     more conteudo.txt > paginado.txt
     ```

O comando `more` é uma ferramenta útil para visualizar o conteúdo de arquivos de texto no Prompt de Comando do Windows. Com ele, você pode ler arquivos extensos de forma mais confortável e controlada, além de utilizar opções de redirecionamento de saída para criar novos arquivos com o conteúdo paginado. Experimente e aproveite essa funcionalidade para facilitar a leitura de arquivos em linha de comando!

## Tema `Tree`
**Guia para Utilizar o Comando `tree` no Prompt de Comando do Windows**

O comando `tree` é uma funcionalidade útil do Prompt de Comando do Windows que permite visualizar a estrutura hierárquica de pastas e subpastas em um diretório específico. Ele cria uma representação gráfica em forma de árvore, facilitando a compreensão da organização dos arquivos e diretórios em uma determinada pasta. A seguir, vamos aprender como utilizar o `tree` de forma prática:

1. **Visualizando a Estrutura de Diretórios do Diretório Atual:**
   Para visualizar a estrutura de diretórios do diretório atual, abra o Prompt de Comando e digite o seguinte comando:
   ```
   tree
   ```
   Ao pressionar "Enter", o Prompt de Comando mostrará uma representação gráfica da estrutura de pastas e subpastas a partir do diretório em que você está posicionado.

2. **Visualizando a Estrutura de Diretórios de um Diretório Específico:**
   Você também pode utilizar o comando `tree` para visualizar a estrutura de um diretório específico. Basta fornecer o caminho absoluto ou relativo do diretório após o comando `tree`. Por exemplo:
   ```
   tree C:\Exemplo\Pasta
   ```
   Esse comando exibirá a representação gráfica da estrutura de pastas e subpastas a partir do diretório "Pasta" localizado no caminho C:\Exemplo.

3. **Limitando a Profundidade da Visualização:**
   Por padrão, o `tree` exibe a estrutura de pastas e subpastas completa, até o nível mais profundo. No entanto, você pode limitar a profundidade da visualização utilizando a opção `/A` seguida do número de níveis desejados. Por exemplo:
   ```
   tree /A 2
   ```
   Esse comando exibirá a estrutura de diretórios até o segundo nível de profundidade.

4. **Excluindo Arquivos da Visualização:**
   O `tree` também permite excluir os arquivos da visualização, exibindo apenas a estrutura de diretórios. Para isso, utilize a opção `/F`:
   ```
   tree /F
   ```
   Isso mostrará apenas as pastas presentes na estrutura hierárquica.

5. **Copiando a Saída para a Área de Transferência:**
   Caso deseje copiar a saída do `tree` para a área de transferência, você pode redirecionar a saída para o comando `clip` usando o operador de redirecionamento `|`. Por exemplo:
   ```
   tree | clip
   ```
   Isso copiará a representação gráfica da estrutura de diretórios para a área de transferência, permitindo colá-la em outro aplicativo, como um editor de texto ou planilha.

6. **Exemplos Práticos:**
   - Visualizar a estrutura de diretórios do diretório atual:
     ```
     tree
     ```
   - Visualizar a estrutura de diretórios de um diretório específico:
     ```
     tree C:\Exemplo\Pasta
     ```
   - Limitar a visualização a dois níveis de profundidade:
     ```
     tree /A 2
     ```
   - Excluir arquivos da visualização:
     ```
     tree /F
     ```
   - Copiar a saída para a área de transferência:
     ```
     tree | clip
     ```

O comando `tree` é uma ferramenta valiosa para visualizar e compreender a organização de pastas e subpastas em um diretório. Ao utilizar suas opções, você pode adaptar a visualização de acordo com suas necessidades e tornar a navegação e a análise da estrutura de diretórios mais eficientes. Pratique com diferentes diretórios e explore todas as possibilidades que o `tree` tem a oferecer!


## Tema `fc`

**Guia para Utilizar o Comando `fc` no Prompt de Comando do Windows**

O comando `fc` (File Compare) é uma ferramenta do Prompt de Comando do Windows que permite comparar o conteúdo de dois arquivos de texto e exibir as diferenças entre eles. Ele é especialmente útil para verificar se dois arquivos são idênticos ou para identificar alterações específicas entre eles. A seguir, vamos aprender como utilizar o `fc` de forma prática:

1. **Comparando Dois Arquivos:**
   Para comparar dois arquivos de texto, digite o seguinte comando no Prompt de Comando:
   ```
   fc nome_do_arquivo1.txt nome_do_arquivo2.txt
   ```
   O Prompt de Comando exibirá as diferenças encontradas entre os dois arquivos, se houver. Caso não haja nenhuma diferença, uma mensagem informando que "nenhuma diferença foi encontrada" será exibida.

2. **Formato da Saída:**
   Por padrão, o `fc` exibe as diferenças entre os arquivos usando o seguinte formato:
   ```
   ***** nome_do_arquivo1.txt
   linha1
   linha2
   ...
   linhaN
   ***** nome_do_arquivo2.txt
   linha1
   linha2
   ...
   linhaN
   *****
   ```
   As linhas que são idênticas nos dois arquivos não são exibidas na saída. Apenas as linhas diferentes são apresentadas para facilitar a análise.

3. **Comparando Diferentes Formatos de Linha:**
   Se os arquivos comparados tiverem formatos de linha diferentes (por exemplo, um arquivo com quebra de linha Unix e outro com quebra de linha Windows), o `fc` pode retornar uma mensagem de erro indicando que os arquivos não são comparáveis diretamente. Nesse caso, você pode usar a opção `/B` para realizar uma comparação binária, ignorando as diferenças de formato de linha:
   ```
   fc /B nome_do_arquivo1.txt nome_do_arquivo2.txt
   ```

4. **Comparando Caracteres Especiais e Espaços em Branco:**
   Por padrão, o `fc` realiza uma comparação entre os arquivos sem levar em conta caracteres especiais e espaços em branco no início e no final das linhas. Caso deseje realizar uma comparação sensível a essas diferenças, você pode usar a opção `/W`:
   ```
   fc /W nome_do_arquivo1.txt nome_do_arquivo2.txt
   ```

5. **Redirecionamento de Saída:**
   Assim como em outros comandos do Prompt de Comando, você pode redirecionar a saída do `fc` para um arquivo de texto. Por exemplo, para salvar a saída da comparação em um arquivo chamado "diferencas.txt", você pode usar o seguinte comando:
   ```
   fc arquivo1.txt arquivo2.txt > diferencas.txt
   ```

6. **Exemplos Práticos:**
   - Comparar dois arquivos:
     ```
     fc arquivo1.txt arquivo2.txt
     ```
   - Comparar dois arquivos com formato de linha diferente:
     ```
     fc /B arquivo1.txt arquivo2.txt
     ```
   - Comparar dois arquivos sensíveis a caracteres especiais e espaços em branco:
     ```
     fc /W arquivo1.txt arquivo2.txt
     ```
   - Comparar e redirecionar a saída para um arquivo:
     ```
     fc arquivo1.txt arquivo2.txt > resultado.txt
     ```

O comando `fc` é uma ferramenta útil para comparar o conteúdo de dois arquivos de texto e identificar diferenças entre eles. Utilize as opções disponíveis conforme a necessidade do seu trabalho e aproveite essa funcionalidade para analisar e verificar a integridade dos arquivos no Prompt de Comando do Windows!

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

Quando trabalhamos com scripts, é comum precisarmos armazenar temporariamente informações em nosso computador. Para isso, utilizamos variáveis, que permitem colocar dados em um espaço de memória e, posteriormente, sobrepor com outras informações. Essa prática é comum tanto em nossos próprios scripts quanto em programas externos, como Java e Python.

Vamos aprender como trabalhar com variáveis de forma prática. Primeiro, criaremos um script para armazenar duas variáveis: uma chamada "nome" e outra chamada "email". Em seguida, exibiremos uma mensagem contendo essas duas variáveis para o usuário final.

No Windows Prompt, podemos criar uma variável digitando "set" seguido pelo nome da variável e o valor que desejamos atribuir a ela. Por exemplo, para criar a variável "mensagem" com o valor "Olá Mundo!", digitamos:

```
set mensagem=Olá Mundo!
```

Para exibir o conteúdo de uma variável, utilizamos o comando "echo" e colocamos a variável entre porcentagens, assim: `echo %mensagem%`.

Agora, vamos criar um script que permita o cadastro do nome e email no Prompt. Primeiro, abrimos o bloco de notas digitando "notepad" no terminal. Em seguida, escrevemos o código do script:

```
@echo off
cls
set /p nome=Digite seu nome completo: 
set /p email=Digite seu e-mail principal: 
echo Seu nome é %nome% e seu e-mail %email%
```

Explicando o script, a primeira linha `@echo off` serve para não exibir os comandos, mostrando apenas o resultado no terminal.

Usamos `cls` para limpar o terminal.

Com `set /p`, permitimos que o usuário digite o nome e o email, e essas informações são armazenadas nas variáveis "nome" e "email", respectivamente.

Ao utilizar `echo` para exibir a mensagem, inserimos as variáveis entre porcentagens para mostrar o conteúdo.

Salvamos o arquivo como "script.bat" e o executamos digitando `.\script.bat` no terminal.

Depois de preenchermos os campos nome e email, o script exibirá a mensagem com as informações digitadas.

Para editar o script e remover a mensagem do "pause", abrimos o arquivo "script.bat" no bloco de notas e removemos a linha `echo Pressione [enter] para continuar`. Salvamos e fechamos o arquivo.

Reexecutamos o script e obtemos o mesmo resultado, mas sem a mensagem redundante.

É importante lembrar que as variáveis criadas são temporárias e existem apenas no terminal em que foram criadas. Se fecharmos o terminal, as variáveis não estarão mais disponíveis.

Por fim, reforçamos que as variáveis são uma ferramenta poderosa para manipular dados em nossos scripts, tornando-os mais dinâmicos e interativos.