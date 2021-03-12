______________________________________________________________________________________________________________________________________________

Bibliotecas

----------------------------------------------------------------------------------------------------------------------------------------------

Python (Instalar utilizando pip3 ou superior):

Utilizando PyPi:

"pip3 install matplotlib" 
"pip3 install numpy"
"pip3 install pylsl"
"pip3 install python-osc"
"pip3 install pyserial"
"pip3 install requests"
"pip3 install socketIO-client"
"pip3 install websocket-client"
"pip3 install wheel"
"pip3 install Yapsy"
"pip3 install xmltodict"
"pip3 install matplotlib"
"pip3 install scipy"
"sudo apt-get install rpi.gpio"

----------------------------------------------------------------------------------------------------------------------------------------------

OpenBCI: 

Utilizando PyPi:
Executar no terminal o c�digo "pip3 install openbci-python"

Utilizando c�digo python:
1 - Download arquivos no link:
2 - Executar comando no terminal "python3 setup.py develop"

----------------------------------------------------------------------------------------------------------------------------------------------

______________________________________________________________________________________________________________________________________________


Raspberry Pi

----------------------------------------------------------------------------------------------------------------------------------------------

A arquitetura ARM n�o compila o arquivo liblsl32.so que est� presente na biblioteca pyLSL.

1 - Download arquivo link: 
2 - Desempacotar o mesmo
3 - Utilizar o comando alterandoos respectivos diretorios para mover o arquivo liblsl-bcm2709 para a o diretorio da biblioteca pylsl:
"mv <path_to>/liblsl-bcm2708.so <pylsl_path>/liblsl32.so"

----------------------------------------------------------------------------------------------------------------------------------------------

______________________________________________________________________________________________________________________________________________

C�digos

----------------------------------------------------------------------------------------------------------------------------------------------

Baixe o arquivo no link:

O sistema completo pode ser configurado e executado utilizando o script "stream_online.py", respons�vel por chamar todas as outras fun��es
caso exista a necessidade de alterar alguma informa��o essencial (n�mero de aquisi��es, n�mero de eletrodos e outros), existe a necessidade
de realizar essas altera��es nos programas "main.py" e "stream_time.py".

"stream_online.py" -> Fun��o respons�vel por realizar a aquisi��o e classifica��o online, ela executa os outros programas "main.py" e 
"stream_time.py"

Existem 4 vari�veis importantes para o controle da fun��o desse programa, cujo valores variam de 1 e 0:

"treino" -> Realiza a aquisi��o do sistema para que possa gerar a base de dados de treino (programa stream_time.py);
"aplica_filtro" -> Janela a base da etapa anterior, aplica os filtros e executa a BCI offline com ou sem sele��o de atributos (programa 
"main.py");
"classifica_online" -> Executa a as aquisi��es para a BCI online de acordo com o n�mero de aquisi��es.

______________________________________________________________________________________________________________________________________________