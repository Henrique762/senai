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
ls -l: lista uma maior exibição dos arquivos./
ls -r: Lista de Z-A sem o -R listaria de A-Z/
pwd: Utilizado para descobrir aonde você está localizado no sistema/
cd: comando utilizado para andar pelo diretório/
cd /: utilizado para mover se para o diretorio root/

**Comandos para pastas dentro do mnt**

mkdir(name) - criar pasta/ 
rmdir (name) - apaga uma pasta/
rm - apagar um arquivo/ 
rm -r - apagar uma pasta e todo o conteudo nela/
-p mkdir - utilizado para criar varias pastas sem ter a pasta de origem/ 
cp (arquivo/pasta de origem) (arquivo/pasta de destino) - copiar arquivo/ 
cp -r - copiar pasta/
mv (arquivo/pasta de origem) (arquivo/pasta de destino) - move arquivos e pastas/ 
 
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

Para juntar arquivos ou pastas com o TAR
    tar -cvf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

        -c - Create

Para juntar um arquivo ou pasta com o TAR e compactar com o GZIP
    tar -cvzf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

Para juntar um arquivo ou pasta com o TAR e compactar com o BZIP2
    tar -cvjf [nome-do-arquivo-novo] [aquivos/pasta a ser juntado]

Para extrair um arquivo - TAR - GZIP - BZIP2
    tar -xvf [nome-do-arquivo]

        -x - Extrair
        -v - Verbose [Verbalizar]
        -f - FILE

Para visualizar o que tem dentro de um arquivo TAR 
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
 Editor de Texto no Terminal
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
 

