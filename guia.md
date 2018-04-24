% Tutorial de Instalação de Pirate Box
% Roteador TP-Link WR703N


# Material necessário

* Roteador TP-Link Wr703N ([confirmar se o modelo é compatível com OpenWrt](https://wiki.openwrt.org/toh/tp-link/tl-wr703n))
* Cabo de Rede
* Pendrive Vazio (formatado com FAT 32)
* Computador (Linux, Mac, ou então Windows com o software Putty)
* Adaptador de tomada (caso necessário)

# Passo 1 - Baixar arquivos necessários para instalação

* Fazer download de firmware específico para o roteador

    * http://stable.openwrt.piratebox.de/auto/
    * Procurar por WR703N, arquivo com final .bin


* Baixar Software do PirateBox

    * http://stable.openwrt.piratebox.de/auto/install_piratebox.zip

# Passo 2 - Preparar arquivos

* Descompactar o Software do PirateBox (install_piratebox.zip) no Pendrive
* Ejetar o pendrive

* Conectar o Pendrive ao roteador


# Passo 3 - Instalar firmware

* Conectar o computador via cabo ao roteador 

* Acessar o endereço de administração do roteador no navegador (firefox,
  chrome, internet explorer....) : 192.168.1.1

  * Usuário/Senha padrão: admin/admin

# Passo 3 - Instalar firmware

![Sessão Administrativa - Retirado de
http://lpb.canb.auug.org.au/hack/wr703n-notes.html](sessaoadm.png)

# Passo 3 - Instalar firmware


* Acessar a sessão de atualização
    * 16o item no menu
    * 3o item no submenu
* Indicar arquivo de firmware
    * Clicar no botão ao lado da entrada de texto
    * Selecionar arquivo com final .bin no computador
    * Clicar no botão no meio da página


# Passo 3 - Instalar firmware
* Antes de confirmar, saiba que após o início o roteador não pode ser
      desligado, senão ele pode "brickar"

* Confirme a instalação, clicando no botão em destaque

* Nesse momento será instalado o firmware e o software do piratebox, o tempo médio é de 15 à 20 minutos (podendo chegar à 45 minutos). Nesse período o roteador irá reiniciar várias vezes..

* O processo terá terminado quando as luzes estabilizarem

# Passo 4 - Configurar o  piratebox - Usando Windows

* Conectar-se ao roteador via putty
    * Abrir putty
    * Host 192 168.1.1
    * connection type: telnet
    * Open
* Será aberto um terminal modo texto, estamos dentro do roteador

# Passo 4 - Configurar o  piratebox

* Rodar comando (digitar exatamento o que está à seguir e em seguida pressionar
  \<enter\>)

          box_init_setup.sh

# Passo 4 - Configurar o  piratebox

* Criar senha (opção 1)
    * Digitar 1 
    * Pressinar \<enter\>
    * Quando digitar a senha, não aparece nenhum caracter (é normal)
    * Sugestão de senha: Labjor22

# Passo 4 - Configurar o  piratebox

* Ativar timesave function (opção 2)
    * Digitar 2
    * \<enter\>
    * Indicar data e hora

* Sair
    * Escolher opção de sair
    * \<enter\>

# Passo 4 - Configurar o  piratebox

* Instalar ferramenta de fórum e visualizador de imagem. 
* Executar o comando:

    /opt/piratebox/bin/board-autoconf.sh



# Passo 4 - Configurar o  piratebox
* Instalar UPnP Media Server
* Executar o comando (é somente 1 linha):

    cp /opt/piratebox/src/openwrt.example.minidlna /mnt/ext/etc/config/minidlna

# Passo 4 - Configurar o  piratebox
* Iniciar o UPnP Media Server
* Executar o comando :

    /etc/init.d/minidlna start

* Executar o comando :

    /etc/init.d/minidlna enable

# Passo 5 - Editar nome da rede wifi 

* Executar o comando:

    vi /etc/config/wireless 

* Seguir a sequência de comandos exatamente como indicado:
    * Navegar com as setas do teclado até o lugar do nome da rede "PirateBox - Share Freely"
    * Usar a tecla \<delete\> para apagar
    * Pressionar a tecla  \<i\> Para entrar no modo de edição
    * Digitar nome da rede
    * Pressionar a tecla \<esc\>
    * Digitar :x
    * Pressionar \<enter\>

# Passo 6 - Reiniciar o roteador
* Digitar o comando:

    reboot

