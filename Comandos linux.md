# Comandos Linux:

**VER MANUAL**
```
MAN antes dos comandos utilizado para saber oq faz
```

ALT+SETINHA + MUDA TTY

**Comando para mostrar usuario conectados**

WHO

....................

**Desligar:**

- poweroff
- shutdown -h now

**Criar arquivo:**


touch <nome-do-arquivo>

**Comando de diretório:**

ls: Lista o diretório/

ls -lR: lista todos os diretórios de uma vez
 
ls -l: lista uma maior exibição dos arquivos.
 
ls -r: Lista de Z-A sem o -R listaria de A-Z
 
pwd: Utilizado para descobrir aonde você está localizado no sistema
 
cd: comando utilizado para andar pelo diretório
 
cd /: utilizado para mover se para o diretorio root
 

**Comandos para pastas dentro do mnt**
 

mkdir(name) - criar pasta
 
rmdir (name) - apaga uma pasta
 
rm - apagar um arquivo
 
rm -r - apagar uma pasta e todo o conteudo nela
 
-p mkdir - utilizado para criar varias pastas sem ter a pasta de origem
 
cp (arquivo/pasta de origem) (arquivo/pasta de destino) - copiar arquivo
 
cp -r - copiar pasta
 
mv (arquivo/pasta de origem) (arquivo/pasta de destino) - move arquivos e pastas/... Renomear arquivos: Nome do arquivo - Novo nome do arquivo
 
 **Instalação de programas no Debian**
 
 apt install (Nome do programa) - instalar um programa
 apt search (nome do programa - procurar um programa 
 apt update - buscar uma lista atualizada dos programas disponiveis no servidor

**Trocar de usuário:** 

su - 

**Limpar Terminal:** 

clear 
ctrl + l 

**Ir para modo admin:**
 
su - - entrar no modo root
..................................

 
wget - Baixar um arquivo da internet [HTTP]

TAR - Programa utilizado no Linux, juntar pastas e arquivos

GZIP - GNU Zip - Compactar arquivos e pastas no Linux

BZIP2 - Compacta com outro algoritmo, mais lento que o GZIP

**Para juntar arquivos ou pastas com o TAR**
    tar -cvf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

        -c - Create

**Para juntar um arquivo ou pasta com o TAR e compactar com o GZIP**
    tar -cvzf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

**Para juntar um arquivo ou pasta com o TAR e compactar com o BZIP2**
    tar -cvjf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

**Para extrair um arquivo - TAR - GZIP - BZIP2**
    tar -xvf [nome-do-arquivo]

        -x - Extrair
        -v - Verbose [Verbalizar]
        -f - FILE

**Para visualizar o que tem dentro de um arquivo TAR** 
 
    tar -tvf [nome-do-arquivo]

senai-sc.tar - 20480 B
senai-sc.tar.gz - 469 B

/etc - Pasta onde estão as configurações do Linux

/etc/hostname - Armazena o nome do Servidor

/var/log - Pasta onde ficam os logs do sistema
        auth.log - Armazena informações sobre login dos usuários
        syslog - Registro dos eventos do sistema

cat - Visualizar o conteúdo de um arquivo de texto

more - Visualizar o arquivo em páginas

    cat [nome-do-arquivo] | more

less - 'more' melhorado

grep - Filtrar o que é exibido na tela
    cat [nome-do-arquivo] | grep [o-que-procurar]

| - pipe

tail - Visualizar as últimas 10 linhas de um arquivo
        -f - Monitorando as alterações do arquivo

head - Visualizar as primeiras 10 linhas de um arquivo

Expressão Regular [RegEx]
    * - Subtituir por qualquer valor


PLUS:
    systemctl restart networking

    reboot - Reinicia o sistema operacional
 
 **Editor de Texto no Terminal**
 
    VIM
        Versão melhorado do 'vi'

        vim.tiny -  VIM mais simples, que vem junto com o Debian

        vimtutor - Tutorial que ensina os passos básicos

        Instalar a versão completa do VIM
            apt update
            apt install vim -y

        vim [nome-do-arquivo] - Criar um arquivo no VIM

        VÁRIOS MODOS
            MODO NORMAL [ESC]
                :
                :set number
                :colorscheme [tema] - Trocar as cores do editor

                :w - Salvar o arquivo
                :w [nome-do-novo-arquivo] - Salvar em um novo arquivo

                :wq - Salvar e sair

                :q - Sair do VIM

                :q! - Força a saída

                x - Apagar um caractere do Texto

                dw [delete word] - Apagar a palavra onde o cursor está
                d2w - Apagar as duas palavras a partir do cursor
                d$ - Apagar todos os texto a partir do cursor até o fim da linha
                dd - Apagar a linha inteira
                2dd - Apagar duas linhas

                u [undo] - Desfaz a última alteração
                Ctrl+r - Refaz a última alteração 

                p - Colar o texto copiado com o y

                yy - Copia uma linha inteira
                2yy - Copia duas linhas inteiras

            MODO DE INSERÇÃO [i - Inserção]

            MODO VISUAL [v - Visual]

                y [yank] - Copiar o texto selecionado

    Nano
        Padrão do GNU

        nano [nome-do-arquivo] - Criar um arquivo de Texto

        ^ - Ctrl
        M - Alt

        ^O - Ctrl + O - Salvar as alterações
        ^X - Ctrl + X - Sair do Nano
        M-U - Alt + U - Desfaz a última alteração
 
 #Criação de grupos
 
 **COMANDOS**
 
        addgroup [nome-do-grupo] - Criar um grupo

        delgroup [nome-do-grupo] - Deletar um grupo

        GID - Group ID - Identificação do Grupo

        0 - 1000 -> Reservados pelo sistema

    ARQUIVO
 
        /etc/group - Arquivo armazena os grupos no Linux

Usuário

    COMANDOS
 
        adduser [nome-do-usuário] - Criar um usuário
        adduser [nome-do-usuário] [nome-do-grupo] - Adicionar um usuário ao grupo

        deluser [nome-do-usuário] - Deletar um usuário
        deluser [nome-do-usuário] [nome-do-grupo] - Remover um usuário do grupo

        UID - User ID - Identificação do Usuário

        id [nome-do-usuário] - Verifica informações sobre o usuário

    ARQUIVO
 
        /etc/passwd - Armazenado os usuários do Linux
        /etc/shadow - Armazenado as senhas dos usuários
                SHA-256 --> 256 bits
                SHA-512 --> 512 bits
 
 d rwx r-x r-x root root  jun 25 17:25 colonia-marciana

Tipos de Arquivos e Pastas
    - -> Arquivo
    d -> Diretório/Pasta
    l -> Link/Atalho

    b -> Bloco de Dados
    c -> Caractere
    s -> Socket [comunição entre processos]

Permissões
    r - Read [Leitura] - 4
    w - Write [Escrita] - 2
    x - Execute [Execução]] - 1

COMANDOS
    chmod - Comando para alterar permissões de pasta/arquivos

        chmod [nº-da-permissão] [pasta/arquivo]

     Octal
        7    -> rwx
        6    -> rw-
        5    -> r-x
        4    -> r--
        3    -> -wx
        2    -> -w-
        1    -> --x
        0    -> ---

    chgrp - Comando para alterar o GRUPO DONO da pasta/arquivo

        chgrp [nome-do-grupo] [pasta/arquivo]

    chown - Comando para alterar o USUÁRIO DONO da pasta/arquivo

        chown [nome-do-usuário] [pasta/arquivo]

PESQUISAR
Como alterar o grupo dono e o usuário dono de uma pasta de uma vez só? Comando chown (Usuário dono):(Grupo dono) (arquivo)
 
# HARDWARE NO LINUX
 
 SIGLAS
    PID - Process ID

COMANDOS
    history - Mostra o histórico de comandos realizados no termina

    find - Pesquisar o nome de arquivos/pastas
        -name - Nome do arquivo
        -iname - Ignora o case sensitive

    df [Disk Free] - Visualizar o tamanho/disponível/utilizado de um disco
        -h - Human Readable [Humanamente Legível]

    du [Disk Unit] - Visualizar o tamanho total de uma pasta/arquivo
        -h - Human Readable [Humanamente Legível]
        -s - Exibe de forma resumida o tamanho da pasta [summary]

    top - O gerenciador de tarefas do Linux
        htop - Versão melhorada do top

    cat /etc/issues - Versão do Sistema Instalado

    cat /proc/version - Versão do Kernel [núcleo]

    arch - Mostra a arquitetura do seu processador
        i686 - 32 bits
        x86 - 32 bits
        x64 - 64 bits
        amd64 - 64 bits
        arm - Mobile

SIMBOLOS

- Pega a saída de um comando e salva para um arquivo de texto
        Exemplo:
            df -h / > tamanho-do-barra.txt

    >> - Pega a saída de um comando e salva para um arquivo de texto, porém mantém o conteúdo do arquivo
            df -h / >> tamanho-do-barra.txt
 
 # Aula 84 -

1° Identificar -
 comando pra visualizar interfaces de rede do Linux: ip add

1° linha é o nome da interface de rede
TX - quanto vc manda
RX - quanto vc recebe 


1° interface lo: loopback 

enp0s3 - interface NAT (que acessa a internet) 

link/ether - mac address 

inet - ip 
brd - broadcast
inet6 - ipv6 

o ifconfig faz parte de um pacote chamado 'net-tools' 
tem que instalar! 
apt install net-tools

ifconfig - só mostra interfaces configuradas
ip add - mostra todas
ifconfig -a - mostra todas (estando ou não configuradas)

Arquivo onde estão as configurações das interfaces: 

/etc/network/interfaces (só DO DEBIAN) 



# Criar host-only - configurando 

# - comentários 
allow-hotplug - tirar o cabo e colocar dnv
auto-hotplug - configura automaticamente 

Configurar inet: static 
auto enp0s
iface [nome-da-interface] inet [modo] 
			DHCP OU STATIC

ex: iface enp0s inet static 

configurar ip: address [IP]
address 192.168.56.10/24

configurar máscara: o que não precisar 
netmask [máscara] 

configurar gateway: 
gateway [gateway] 

systemctl - controlador de processos 
	systemctl restart  [serviço] - para e inicia o serviço 
	system ctl reload [serviço] - atualiza configurações
	systemctl start [serviço] - inicia 
	systemctl restart [serviço] - reinicia 

journalctl -xe -
	
Abrir o Firewall do Windows
    Windows + R
    firewall.cpl

Instalar o Servidor de SSH no Debian
    apt install openssh-server

Verificar se o Serviço de SSH está rodando
    systemctl status ssh

Reiniciar o serviço de SSH
    systemctl restart ssh
    systemctl reload ssh

Visualizar quem está logado no momento dentro do Servidor
    who
    who -u - Informações detalhadas

Porta TCP padrão do SSH - 22

Por padrão o usuário ROOT não pode ser usado para login através do SSH

ARQUIVO
    /etc/ssh/sshd_config - Arquivo de configuração do SSH no Debian

