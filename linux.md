## **GUIA DE COMANDOS E ATALHOS**
# **LINUX**


### ***Comandos e atalhos essenciais de LINUX***   
**`<CTRL>` `<ALT>` `<F1>`** Muda para o primeiro terminal de texto. Em LINUX podemos ter vários terminais abertos ao mesmo tempo. 

**`<CTRL>` `<ALT>` `<Fn>`** (n=1..6). Muda para o n-ésimo terminal. 

**`<CTRL>` `<ALT>` `<Fm>`** (m=7..12). Muda para 0 m-ésimo terminal GUI (se houver um terminal GUI a correr na sessão m-1).

**`<Tab>`** Autocompleta o comando (num terminal). Este é um dos melhores atalhos em LINUX. Trabalha inclusivamente na prompt LILO.

**`<ArrowUp>` `<ArrowDown>`** Lista um por um e permite edição do historial de comandos executados. Carregue em `<ENTER>` para executar o comando escolhido.

**`<ShJR>` `<PcUp>`** Visualiza as "janelas" anteriores do terminal. Trabalha inclusivamente na prompt de login, para
podermos visualizar as mensagens de bootup.

**`<Shift>` `<PcDown>`** Visualiza as "janelas" seguintes do terminal.

**`<CTRL>` `<ALT>` `< + >`** (em X-window). Muda para a próxima resolução de X-server (se tivermos configurado o X-server para mais do que uma rcsolução).

**`<CTRL>` `<ALT>` `<->`** (em X-window). Muda para a resolução anterior do X-server.

**`<CTRL>` `<ALT>` `<BkSpC>`** (em X-window). Mata (kill) o servidor X-window actual. Usa-se quando o X window bloqueia e
não podemos sair normalmente.

**`<CTRL>` `<ALT>` `<DEL>`** Desliga o sistema e faz reboot. Executa o comando **shutdown** normal.

**`<CTRL>`**c Mata (kill) o processo corrente.

**`<CTRL>`**d Sai da sessão actual.

**`<CTRL>`**d Envia [End-of-File] para o processo corrente.

**`<CTRL>`**l Limpa o ecran. Igual ao comando clear da shell.

**`<CTRL>`**s Pára a transferência para o terminal.

**`<CTRL>`**q Retoma a transferência para o terminal. Tentar este atalho quando o terminal deixar de responder misteriosamente...

**`<CTRL>`**z Suspende a execução interactiva do processo corrente. O comando da shell **fg** retoma a execução do processo em modo interactivo (em foreground).O comando **bg** retoma a execução do processo em modo não-interactivo (em background).

**reset** "Restaura um terminal "estragado" (com caracteres esquisitos) para as definições de defeito. Usa-se, por exemplo, quando se executa o comando **cat** num ficheiro binário. Podemos não ver o comando enquanto o escrevemos.

**`<BotaoRatoMeio>`** Cola (paste) o texto seleccionado noutro sítio qualquer. Esta é a operação "copy-paste" normal em LINUX (não funciona no Netscape ou no WordPerfect, porque estes programas usam o "copy-paste" típico do MS-WINDOWS. Perfeito quando usado com um rato LINUX-compatível de 3 botões (Logitech ou algo do género).

**~** (tile). Muda para a home directory. Por exemplo, **cd ~/minha_dir** muda para a directoria minha_dir situada abaixo da nossa home directory. Digitar apenas **cd** é o equivalente ao comando **cd~**.

**.** (ponto). Directoria actual. Por exemplo, **./meu_programa** executa o comando meu_programa situado na directoria corrente.

**..** (dois pontos). Directoria-"pai" da directoria corrente.

### ***Comandos comuns de LINUX - informação de sistema***

**pwd** Exibe o nome da directoria corrente.

**hostname** Exibe o nome da máquina onde estamos a trabalhar (hostname). Usa-se o comando **netconf** para mudar o nome da máquina.

**whoami** Exibe o nosso username (nome de login).

**id *usemame*** Exibe o user id (uid), o group id (gid), id efectivo (se for diferente do uid) e todos os grupos suplementares relacionados com o utilizador especificado na variável username.

**date** Exibe ou modifica a data e hora do sistema. Por exemplo, para mudar a data e hora para 2000-12-31 23:57, usa-se o comando **date** com esta forma: 

>**date 123123572000**  

Para modificar o relógio de hardware (hardware clock) a partir do relógio do sistema, usa-se o comando setclock.

**time** Determina o tempo que demora a completar um determinado processo, além de outra informação. Não confundir com o comando **date**. Por exemplo, podemos saber quanto tempo demora a exibir o conteúdo de uma directoria, usando o comando time da seguinte forma:

>**time ls**  

**who** Exibe uma lista com os utilizadores que estão "logados" (logged in) à máquina.  

**rwho -a** Exibe uma lista com todos os utilizadores que estão ligados à nossa rede. O serviço rwho deve estar a correr de modo a este comando poder funcionar. Se não estiver, corre-se o comando **setup** como root para "ligar" o serviço **rwho**.

**finger _username_** Exibe informação detalhada sobre um determinado utilizador, especificado na variável *username*. Por exemplo, **finger root** dá-nos toda a informação sobre o utilizador root.  

**last** Exibe uma lista com os últimos utilizadores que se ligaram (logged in) ao sistema. Se usarmos o comando **last** em conjunto com **less**, podemos "navegar" nessa lista: **last | less**. Se, por outro lado, usarmos o comando dessa forma: **last -n**, obtemos uma lista com os últimos n logins ao sistema.  

**uptime** Tempo que passou deste o último reboot.

**ps** (= print status). Lista os processos que estão a correr neste momento pelo utilizador corrente.

**ps aux | more ps aux | less** Lista todos os processos que estão a correr na máquina neste momento, inclusivamente aqueles que não têm controlo no terminal, juntamente com a informação sobre o utilizador que iniciou cada um deles.

**ps aux | grep exemplo** Lista todos os processos chamados "exemplo". O comando **grep** "filtra" o resultado do comando **ps aux** (através da pipe "|"), aparecendo só as linhas que contém o texto "exemplo". 

**top** Exibe uma lista com os processos que estão a correr na máquina neste momento, ordenados decrescentemente por tempo de CPU gasto.

**uname -a** Informação sobre o servidor.

**free** Informação de memória (em kilobytes).

**df -h** (= disk free). Exibe informação sobre os discos de todos os sistemas de ficheiros (filesystems), numa linguagem entendida pelos humanos... :-)´

**du / -bh | more** (= disk usage). Exibe uma lista detalhada do uso do disco para  ada subdirectoria, começando pela directoria /, em linguagem legível.

**cat /proc/cpuinfo** Informação sobre o CPU. Note-se que os ficheiros na directoria /proc não o são na realidade. Tratam-se somente de "ganchos" (hooks) para visualizar informação disponível no kernel.

**cat /proc/interrupts** Exibe uma lista com os interrupts em uso.

**cat /proc/version** Versão do LINUX e outra informação.

**cat /proc/filesystems** Exibe uma lista com os sistemas de ficheiros (filesystems) em uso neste momento.

**cat /etc/printcap** Exibe o setup das impressoras ligadas ao sistema.

**lsmod** (como root). Exibe uma lista com os módulos de kernel carregados neste momento.

**set | more** Exibe o ambiente corrente do utilizador.

**echo $PATH** Exibe o conteúdo da variável de ambiente "PATH". Este comando também pode ser usado para visualizar outras variáveis de ambiente. Usa o "set" para ver todo o ambiente.

**dmesg** Exibe as mensagens de boot (boot messages). Na realidade, exibe o conteúdo do ficheiro **/var/log/dmesg**.

### ***Operações básicas*** 

**comando --help | more comando --help | less** Exibe uma ajuda simples ao comando (aplica-se à maior parte dos comandos LINUX). "--help" é semelhante ao switch "/h" do DOS. As pipes "more" e "less" usam-se quando a informação ocupa mais do que um ecran, sendo que a opção "more" permite ver página a página, sem no entanto podermos voltar atrás, e a opção "less", permite-nos navegar linha a linha, para a frente e para trás.

**ls** Exibe o conteúdo da directoria corrente. Em LINUX, o comando **dir** é um "alias" do comando **ls**. Muitos utilizadores utilizam o comando **ls** como um "alias" do comando **ls --color**.

**ls -al | more** Exibe o conteúdo da directoria corrente, todos os ficheiros (incluindo aqueles que começam "."), e num formato longo.

 **cd *directoria*** (= change directory). Muda para uma determinada directoria. Usar s6 o comando **cd** significa mudarmos directamente para a nossa home directory. O comando **cd -** leva-nos para a directoria anterior à corrente e é um modo conveniente de navegação entre duas directorias.

 **cp *fonte destino*** Copia ficheiros entre a fonte e o destino.

 **mcopy *fonte destino*** Copia um ficheiro de/para um sistema de ficheiros DOS (não é necessário usar previamente o comando **mount**). Por exemplo, **mcopy a:\autoexec.bat ~/lixo**. Usar o comando **man mtools** para comandos relacionados, como por exemplo: **mdir, mcd, mren, mmove, mdel, mmd, mrd, mformat,...**.

 **mv *fonte destino*** Move ou altera o nome dos ficheiros. O mesmo comando é usado para mover ou alterar nomes de directorias ou ficheiros.

 **ln *fonte destino*** Cria um hard link chamado *destino* que aponta para o ficheiro chamado *fonte*. O link aparenta ser uma cópia do ficheiro original, mas na realidade, apenas uma cópia do ficheiro é mantida, sendo que existem duas (ou mais) entradas para o ficheiro na directoria. Qualquer alteração ao ficheiro *fonte* é imediatamente visível no *destino*. Quando uma entrada na directoria é removida, as outras mantém-se.  
 Limitações dos hard links: os ficheiros têm de estar obrigatoriamente no mesmo filesystem. É impossível criar hard links para directórios ou ficheiros especiais.

 **ls -s *fonte destino*** Cria um link simbólico (symbolic link) chamado destino a apontar para o ficheiro *fonte*. O link simbólico apenas especifica o caminho (path) para o ficheiro *fonte*. Ao contrário dos hard links, a fonte e o destino não precisam de pertencer ao mesmo filesystem.  
 Limitações dos symbolic links: Se o ficheiro original for removido, o link "parte-se" (broken link). Os symbolic links podem também criar referências circulares (como as de bases de dados e folhas de cálculo).

 **rm *ficheiro*** Remove (apaga) o ficheiro especificado na variável ficheiro.

 **mkdir *directoria*** Cria uma directoria chamada directoria.

 **rmdir *directoria*** Remove a directoria especificada na variável directoria.

 **rm -r *ficheiros*** (recursive remove). Remove ficheiros, directorias e sub-directorias. Semelhante ao comando DOS **deltree**. Cuidado ao usar este comando como root: podemos apagar todo o nosso sistema, se usarmos este comando na directoria /, e não existe (ainda) um comando undelete em LINUX. Mas, se realmente quisermos executar este comando, aqui está como: __rm .rf/*__.

 **cat *ficheiro* | more cat *ficheiro* | less** Exibe o conteúdo de um ficheiro de texto chamado *ficheiro*. Para ficheiros demasiadamente longos, é conveniente usar os comandos **head** e **tail**, que exibem o princípio e o fim do ficheiro em questão. Se, por engano, tentarmos visualizar o conteúdo de um ficheiro binário, e só aparecerem caracteres esquisitos, usa-se o comando **reset** para voltar ao normal.

 **less *ficheiro*** Para navegar no conteúdo de um ficheiro de texto. Para terminar a nossa navegação, carrega-se na tecla q.

 **pico *ficheiro*** Edita o ficheiro denominado *ficheiro*.

 **pico -w *ficheiro*** Edita um ficheiro chamado *ficheiro*, desactivando a opção "long line wrap". Útil para editar ficheiros de configuração, por exemplo, o ficheiro **/etc/fstab**.

 **lynx *ficheiro.html*** Exibe um ficheiro html ou navega na internet a partir do modo texto.

**tar -zxvf *ficheiro.tar.gz*** Descompacta (untar) um ficheiro (*.tar.gz ou *.tgz), habitualmente retirado da internet.  
*.tar.gz ou *.tgz - tarred and compressed tarball.

**tar -xvf *ficheiro.tar*** Descompacta um ficheiro (*.tar).  
*.tar - tarred but uncompressed tarball.

**gunzip *ficheiro.gz*** Descompacta um ficheiro "zipado" (zipped) (*.gz ou *.z). Usa-se o **gzip** (ou o zip ou compress) para compactar os ficheiros.

**bunzip2 *ficheiro.bz2*** Descompacta um ficheiro (*.bz2) compactado com o utilitário bzip2. Normalmente é um método de compressão mais eficiente do que o obtido com o gzip.

**unzip *ficheiro.zip*** Descompacta um ficheiro (*.zip) compactado com um utilitário compatível com o pkzip do DOS.

**find / -name *"ficheiro"*** Procura o ficheiro chamado ficheiro a partir da directoria /. A variável filename pode conter wildcards (*,?).

**locate *ficheiro*** Procura o ficheiro que contém o texto *ficheiro*. Mais fácil de usar e mais rápido que o comando **find**.

**pine** Um bom cliente de mail em modo texto. Outro cliente de mail excelente é o **elm** Permite ler as mensagens enviadas, por exemplo, por um processo cron.

**talk *username1*** "Fala" (talk) com outro utilizador ligado neste momento à nossa máquina (ou outra máquina através do comando **talk username1@outramaquina**). Para o outro utilizador aceitar o "convite", necessita digitar o comando **talk username2**. Para evitar que tentem "falar" connosco, usa-se o comando **mesg n** para recusar os pedidos. Pode ser útil o uso dos comandos **who** e **rwho** para ver quem está ligado ao sistema.

**mc** Inicia o gestor de ficheiros Midnight Commander.

**telnet *servidor*** Conecta-se a outra máquina usando o procolo TELNET. Use o nome da máquina remota ou o seu endereço IP. O Telnet vai conectar-se à outra máquina, pedindo-nos um login e uma password, de modo que temos de ter uma conta nessa máquina. Este comando não é muito seguro, uma vez que todas as transferências dados são feitas em modo texto, incluindo a nossa password!

**rlogin *servidor*** (= remote login). Conecta-se a outra máquina. O login name da sessão corrente é usado para entrar na máquina remota. Se se pretender entrar num outro username, adiciona-se a opção **-l username**.

**rsh servidor** (= remote shell). Uma outra maneira de nos conectarmos a uma máquina remota. Tal como o comando **rlogin**, é usado o login name da sessão corrente, a menos que se use a opção **-l**. 

**ftp servidor** Acede a outra máquina via protocolo FTP. Também existe o ncftp, que acrescenta algumas funcionalidades extra ao FTP normal, e o gftp para GUI. O FTP é bom para copiar ficheiros para/de um servidor. Deve-se tentar o utilizador "anonymous" (quando não temos conta aberta no sistema remoto). Após a conecção estar feita, use o comando **?** para exibir uma lista de comandos disponíveis.  
Os comandos principais são: **ls** (exibir o conteúdo da directoria corrente do sistema remoto), **ascii, binary** (para mudar o modo de transferência de ficheiros para texto ou binário), **get** (copia um ficheiro do sistema remoto para o sistema local), **mget** (copia vários ficheiros ao mesmo tempo, do sistema remoto para o sistema local), **put** (copia um ficheiro do sistema local para o sistema remoto), **mput** (copia vários ficheiros do sistema local para o sistema remoto), **bye** (desconecta-se do sistema remoto).

**minicom** Programa minicom (parecido com o "Procomm for Linux").

**/programa** Corre um executável na directoria corrente, se esta não estiver na variável de ambiente PATH.

**xinit** Inicia um servidor barebone X-windows (sem o gestor de janelas).

**stratx** Inicia um servidor X-window, juntamente com o gestor de janelas por defeito.

**stratx ..:1** Inicia outra sessão de X-windows no ecran 1 (por defeito, inicia no ecra 0). Podemos ter vários terminais GUI a correr correntemente. "Salta-se" entre eles com as teclas `<CTRL><ALT><F7>`, `<CTRL><ALT><F8>`, etc.

**xterm** (no terminal X). Corre um terminal X-window simples. Use o comando **exit** para sair.

**xboing** (no terminal X). Jogo para correr no ambiente X. Provavelmente, muitos jogos e programas parecidos estão instalados na nossa máquina.

**gimp** (no terminal X). Editor de imagens poderoso. Demora algum tempo a aprender, mas é excelente para artistas. Use o botão do rato do lado direito para obter menus.

**netscape** (no terminal X). Corre o browser Netscape (necessita de ser instalado antes).

**netscape -display host:0.0** (no terminal X). Corre uma sessão de Netscape na máquina remota host na sessão 0 ecran 0. A nossa máquina deve ter permissão para executar o netscape na máquina remota (podemos obter permissão correndo o **comando xhost maquina local** no terminal X da máquina remota).

**shutdown -h now** (como root). Desliga o sistema e não reinicializa.

**shutdown -r now** (como root). Desliga e reinicializa o sistema. Pode, em alternativa, usar a combinação de teclas `<CTRL><ALT><DEL>` para executar o comando na máquina.

**halt reboot** (como root). Usado para desligar o sistemas e não reinicializar (halt) ou para fazer um reboot ao sistema (reboot). Mais fácil de usar (e decorar) do que os dois comandos anteriores.

**man topico** Exibe o conteúdo das páginas do manual do sistema sobre o assunto topico. Tente usar o comando **man man** primeiro. Carregue na tecla q para cancelar a visualização. O comando **info topic** funciona aproximadamente como o comando **man** e pode conter informação mais actualizada. As páginas do manual podem ser de difícil leitura.  
Use o comando **topic --help** para páginas de ajuda mais curtas e fáceis de ler. Se necessitar de mais ajuda, consulte a directoria **/usr/doc**.

**apropos *topico*** Exibe uma lista de comandos que tenham alguma relação com o topico.

### ***Ferramentas de gestão de rede***

**netconf** (como root). Um utilitário baseado em menus para a gestão (setup) da nossa rede. Usado na distribuição Red Hat.

**linuxconf** (como root). Utilitário de configuração do nosso sistema linux. Usado na distribuição Red Hat.

**setup netconfig** (como root). Ferramentas com a mesma função das duas mencionadas acima, mas estas são usadas na distribuição Slackware de linux.

**ping máquina** Verifica a ligação a outra máquina, podendo a variável máquina ser o nome da máquina ou o endereço IP. Para terminar, use o `<CTRL>`c.

**route -n** Exibe a tabela de "routeamento" (routing table).

**ipfwadm -F -p m** Configura a política de reencaminhamentos de IPs da firewall para passar a fazer "masquerading". Não é muito seguro mas é simples. A partir da versão 2.2 do linux, deve-se usar o ipchains, sendo necessário ter o kernel configurado para suportar IP firewalls e que o routing de IP esteja activado.

**ifconfig** (como root). Exibe informação sobre os interfaces de rede correntemente activos (ethernet, ppp, etc). A primeira interface ethernet deve ser a eth0, a segunda a eth1, etc. A primeira interface ppp (modems) é a ppp0, a segunda ppp1, etc. A intrface "lo" é a "loopback only" com o endereço 127.0.0.1 que deve estar sempre activa. Usa a opção ifconfig --help para mais informações sobre como configurar as interfaces.

**ifup interface** Acciona uma interface de rede. Exemplo: ifup eth0 ou iph ppp0. Utilizadores normais só podem accionar ou desactivar uma interface de rede se tiverem permissões para isso e só as interfaces ppp (use o comando netconf).

**ifdown interface** Desactiva uma interface de rede.

**netstat | more netstat | less** Exibe informação sobre o estado da nossa rede. 

### ***Controlo de processos***

**ps** (= print status). Exibe uma lista com os processos activos no sistema com os respectivos identificadores - PID (Process ID). Use **ps -aux** para exibir uma lista semelhante mas com mais informação - todos os processos e respectivos utilizadores. Use **top** para "manter" a listagem visível e "on-line".

**fg PID** Passa um processo que está a correr em "background" para "foreground".

**bg PID** Processo inverso ao anterior: passa um processo para "background".

**kill PID** **Força** o final do processo. Para saber qual o PID do processo que queremos "matar", usa-se o comando **ps**.

**killall *nome_programa*** "Mata" programas pelo nome.

**xkill** Usado num terminal x. "Mata" um processo GUI com o rato - "aponte" o cursor do rato à janela com o processo que queremos "matar" e clique.

**lpc** (como root). Verifica e controla a(s) impressora(s).

**lpq** Exibe o conteúdo da "queue" da impressão. Em KDE (X- Window), podemos usar o "Print Queue" GUI disponível nos utilitários.

**lprm job#** Remove um trabalho de impressão da "queue".

**nice *nome_programa*** Corre o *nome_programa* ajustando a sua prioridade. Como a prioridade não é especificada neste exemplo, ela é ajustada com o valor 10 (o processo vai correr mais lentamente) a partir do valor de defeito (usualmente o 0 - zero). Quanto mais baixo for o número, mais alta é a prioridade. Este número pode variar entre -20 e 19, sendo que só o utilizador root pode definir prioridades com valores negativos. Use o comando **top** para exibir as prioridades dos processos activos.

**renice -1 PID** (como root). Muda a prioridade de um processo activo para -1. Utilizadores normais só podem mudar valores de prioridade para os seus processos, e só para valores superiores ao actual (tornando-os mais lentos).

### ***Comandos básicos de administração***

**printtool** (como root num terminal X). Ferramenta de configuração de impressoras. Os "settings" ficam no ficheiro **/etc/printcap**.

**setup** (como root). Configura o rato, placa de som, teclado, X-windows e serviços de sistema.

**alias ls= "ls --color"** Cria um "alias" para o comando ls. Ponha o "alias" no ficheiro /etc/bashrc se quiser que esteja sempre disponível para todos os utilizadores. O comando alias dá-nos uma lista com todos os "aliases" do nosso sistema.

**adduser utilizador** (como root). Cria uma nova conta. Por exemplo, adduser barbara. Não esquecer de definir uma password para o utilizador como passo seguinte. O "home-directory" do utilizador passa a ser /home/utilizador. Irá estar associado a cada utilizador um identificador - UID (User ID).

**useradd utilizador** (como root). Igual ao comando adduser.

**userdel utilizador** (como root). Remove uma conta do sistema, não apagando no entanto, o "gome-directory" e o email não entregue.

**groupadd grupo** Cria um novo grupo de utilizadores do sistema. A este grupo, tal como a qualquer utilizador, irá estar associado um identificador -GID (Grupo ID).

**passwd** **Muda** a password na conta actual. O utilizador root pode alterar a password de qualquer utilizador, usando o comando passwd utilizador.

**chmod perm ficheiro** (= change mode). Muda as permissões de acesso a um ficheiro e/ou directoria do utilizador actual (o root pode mudar permissões de qualquer ficheiro no sistema) Há três tipos de acesso: leitura (read - r), escrita (write - w) ou execução (execute - x) para três classes de utilizadores: dono (u), membros do grupo do dono (g), outros utilizadores no sistema (o). Podemos ver quais as permissões de determinado ficheiro usando o comando ls -l ficheiro.

**chown novo_dono ficheiro chgrp novo_grupo ficheiro** Muda o dono (chown = change owner) ou grupo (chgrp = change group) a que pertence determinado ficheiro. Deve-se usar estes dois comandos sempre que copiamos um ficheiro para ser usado por outra pessoa.

**su** (= substitute user id). Assume a identidade do "superuser" root (pedindo-nos a respectiva password). Escreva exit para voltar ao utilizador anterior. Não trabalhe habitualmente como root numa máquina. Este utilizador serve para executar tarefas de administração e o comando su serve para facilitar o acesso a este utilizador.

**rpm -ivh ficheiro.rpm** (= Red Hat Package Manager, como root). Instala o conteúdo de um "pacote" rpm da Red Hat e mostra informação sobre o que foi feito.

**rpm -qpi ficheiro.rpm** Lê a informação sobre o conteúdo de um "pacote" rpm que ainda não tenha sido instalado no sistema.

**rpm -Uvh ficheiro.rpm** Faz o upgrade de um determinado "pacote".

**glint gnorpm kpackage** (num terminal X, como root). Frontend GUI para instalar "pacotes" rpm em ambiente X-window. 

**kernelcfg** (como root num terminal X). Programa GUI para acrescentar/remover módulos de kernel. Pode-se fazer o mesmo da linha de comandos usando o comando insmod.

**lsmod** **Exibe** uma lista dos módulos de kernel correntemente instalados no sistema.

**modprobe -l | more** Exibe uma lista com todos os módulos disponíveis para o kernel.

**insmod parpot** (como root). Insere módulos no kernel (um módulo é (mais ou menos) o equivalente aos "device **insmod ppa** drivers" de DOS). Este exemplo demonstra como inserir os módulos para suportar uma zip drive externa via porta paralela.
