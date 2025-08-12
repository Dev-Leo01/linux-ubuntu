# Códigos ubunto via terminal.
---
## Data: 06/08/2025.
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
## Data: 08/08/2025.
---
* cd = navegar através de diretórios, pastas. 
---
## Configuração da VM (host).
---
* Criação de uma nova pasta na máquina física, no disco local " VirtualBox-PastaCompartilhada "
* Criamos documento de texto com o nome arquivo_teste_host.
* Foi escrito dentro deste arquivo a mensagem: " Este é um teste para pasta compartilhada entre host (máquina física) e guest (virtual). ".
## Configuração da VM (guest).
---
* Virtual Box - Configurações - Pasta Compartilhada - Adicionar - Selecionar pasta no disco local.
    - Iniciar Ubunto.
    - Acessar Terminal.
---
* sudo adduser $USER vboxsf = Adiciona o usuário no grupo vboxsf após isto, dar sudo reboot para reiniciar.
---
* cd /media/sf_VirtualBox-PastaCompartilhada = acessa o diretório da pasta compartilhada.
---
* cd ../ = voltar no diretório, na pasta anterior.
---
* ls = Lista os arquivos na pasta.
---
* echo " Mensagem que voce quer dentro " > ( nome do arquivo tipo "arquivo_teste" e não esqueça da extensão " .txt " no final = Cria um arquivo na pasta compartilhada.
---
* cat + nome do arquivo de texto = Leitura do que está escrito no documento de texto.
---
### Após isto usamos um aplicativo padrão do ubunto para abrir o arquivo e edita-lo.
* nano ( nome do arquivo ) = Usar CTRL + os guias que tem no próprio nano.
---
### Foi instalado um segundo aplicativo que foi instalado " VIM ".
- digite " vim " sem estar no diretório da pasta com partilhada e aparecerá os comandos de instalação.
---
* vim (nome do arquivo) = abre o arquivo de texto.
  - Insert = Editar o texto.
  - ESC = Sair do modo de edição.
---
* :q! = sair sem salvar alterações.
---
* :wq = salvar alterações e sair.
---
* :set number = aparece os números no canto.
---
* vim ~/.vimrc = configurar o vim, onde coloca o :set number para não precisar ficar digitando o comando toda vez que usar o vim.
---
## Data: 11/08/2025.
---
Dentro do diretório: cd /media/sf_VirtualBox-PastaCompartilhada.
---
* ls -l = trás detalhes da listagem ( data,mes, ultimo horário que foi modificado, "vboxsf" por exemplo é o grupo)
---
* groups = ver o grupo em que eu estou (cada palavra que é mostrada é o grupo em que eu estou).
---
* sudo groupadd (nome do grupo) = cria um grupo.
    - Voltar ao diretório raiz /$ usando o "../". Executar o comando "cd etc", usar o comando "ls".
    - cat group - ler os grupos que existem. Os numeros que aparecem ao lado são como identificações.
---
* 2 Alternativas para adicionar um usuário em um grupo.
  - sudo adduser $USER nome_do_grupo (Ubuntu/Debian Desktop).
  - sudo usermod -aG nome_de_usuário nome_do_grupo.
     - Consegue adicionar um mesmo usuário para vários grupos de uma só vez, basta colocar o nome de todos os grupos que o usuário irá ser adicionado depois do nome de usuário. exemplo: <br> sudo usermod -aG nome_de_grupo1 nome_de_grupo2 nome_de_usuário.
---
Fomos ao diretório raiz e foi digitado:
- sudo mkdir home/pasta_alunos
  - mkdir = criar novo diretório
Navegamos até o home - cd /home. Usamos o ls -l e vimos que o grupo da pasta alunos era root então executamos o seguinte comando:
* sudo chown :alunos pasta_aluno ou seja:
  - sudo chown :nome_do_grupo nome_da_pasta
    - chown = mudar o grupo proprietário de um diretório.
Depois executamos o comando ls -l e vimos que foi mudado o grupo.
---
drwxr-xr-x  2 root  alunos 4096 ago 11 21:30 pasta_alunos <br>
drwxr-x--- 16 senac senac  4096 ago 11 20:23 senac
---
- root é o usuário proprietário.
- alunos é o grupo proprietário.
- 4096 = tamanho.
--- 
  - d = diretório.
  - r = ler.
  - w = gravar dados.
  - x = executar.
  - "-" = sem permissão.
---
1° Letra = diretório. <br>
próximos 3 caracteres = proprietário.<br>
próximos 3 caracteres = grupo.<br>
próximos 3 caracteres = outros.<br>
