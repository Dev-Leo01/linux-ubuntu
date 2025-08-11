# Códigos ubunto via terminal.
---
* Comando sudo <br> - Concede privilégio de administrador.
---
* apt: <br> - Gerenciador de pacotes.
---
* Acessar o terminal: <br> - Clique no icone do terminal. <br> - Ctrl + Alt + T.
---
- Selecionar códigos usados anteriormente: <br> - setas do teclado.
---
* sudo apt update: <br> - Baixa as atualizações.<br>
---
* sudo apt upgrade: <br> - Instala as atualizações.<br>
---
* sudo apt update && sudo apt upgrade: <br> - Baixa e instala atualizações.<br>
---
* sudo reboot: <br> - Reinicia.<br>
---
* clear: <br> - limpa a tela. <br>
---
* sudo apt install build-essential dkms linux-headers-$(uname -r): <br> - Instala build-essential: ferramenta para compilar código-fonte. <br> - dkms: recompilador de aplicações para compatibilidade com Kernel do convidado ( guest ).
---
* cd /media/$USER/VBox_GAs_7.0.6: <br> - Caminha até o diretório onde está o aplicativo para instalar recursos adicionais de convidado. **$USER** é uma variável de ambiente que referencia o valor do usuário que está logado ( nome de usuário ).
---
* sudo ./VBoxLinuxAdditions.run: <br> - Executa a aplicação disponível no diretório que acessou e instala os recursos.
---
* lsmod | grep vbox: <br> - lsmod: Listar módulos carregados no Kernel. <br> - grep: funciona como um filtro para pesquisar apenas as linhas que contenham o texto que deseja pesquisar ( nesse caso, vbox ). <br> - vbox: prefixo que inicia normalmente os nomes dos módulos do VirtualBox. <br>
---
## Configuração da VM (host)
---
* Criação de uma nova pasta na máquina física, no disco local " VirtualBox-PastaCompartilhada "
* Criamos documento de texto com o nome arquivo_teste_host.
* Foi escrito dentro deste arquivo a mensagem: " Este é um teste para pasta compartilhada entre host (máquina física) e guest (virtual). ".
## Configuração da VM (guest)
---
* Virtual Box - Configurações - Pasta Compartilhada - Adicionar - Selecionar pasta no disco local.
    - Iniciar Ubunto.
    - Acessar Terminal.
* sudo adduser $USER vboxsf - Adiciona o usuário no grupo vboxsf após isto, dar sudo reboot para reiniciar.
* cd /media/sf_VirtualBox-PastaCompartilhada = acessa o diretório da pasta compartilhada.
* ls = Lista os arquivos na pasta.
* comando para criar arquivo
* cat + nome do arquivo de texto = Leitura do que está escrito no documento de texto.
* 
