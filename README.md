# Linux (Ubuntu)

#### Atalhos, configurações e outros

## Configuração de ambiente Linux:

- Antes de começar, atualizar o apt get:
netstat -lnp | grep 8080
  ```$ sudo apt update && sudo apt upgrade```netstat -lnp | grep 8080

- Instar o cUrl:

  ```$ sudo apt install curl```

- Instalar o GIT:

  ```$ sudo apt-get install git-all```

### ZSH Termina  
19
l:
  
- Instalar ZS
210
  ```H:

  ```$ apt install zsh```

- Instalar o Oh my ZSH:

  ```$ curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh; zsh```
  * Reiniciar o Ununtu

- Adicionar plugin DNF:

  * Abrir o arquivo '.zshrc' na raiz das pastas pessoais
  * Na parte 'plugins=(git)' adicionar o DNF
  ```
  Ex: plugins=(
               git
               dnf
              )
  ```

- Instalar o plugin zhttps://github.com/wagoodman/divesh-syntax-highlighting (Destaca se a sintaxe do comando esta ok ou não):

  ```
  $ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
  ```
  
  * Adicionar o 'zsh-syntax-highlighting' aos plugns no arquivo '.zshrc'

- Instalar plugin zsh-autosuggestions (Sugere comandos ja executado):

  ```
  $ git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
  ```
  
  * Adicionar o 'zsh-autosuggestions' aos plugins no arquivo '.zshrc'


- Instalar plugin FZF:

  ```
  $ git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install
  ```
  
  * Responder “y” a todas as perguntas  
  * Agora com CTRL + T no terminal é mostrado as pastas para seleção
  * Com CTRL + R, tem a lista dos ultimo comandos executados
  * Documentação: https://github.com/junegunn/fzf

- Instalar Hack font:

  * Fazer donwload da fonte no pacote deste repositorio (https://github.com/rodrigospimentacwb/linux/tree/main/hack-font)
  * Executar os commandos:
  
  ```
    $ sudo mkdir /usr/share/fonts/opentype/hack
    $ cd /usr/share/fonts/opentype/hack
    $ sudo unzip ~/Downloads/hack-font.zip
    $ sudo fc-cache -f -v
  ```
  
  * Alterar a font padrão nas propriedades do terminal
 
 - Instalar o powerlevel9k (Personalização de terminal):
    
    * Rodar o comando:
  
    ```$ git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k```
    
    * Abrir o arquivo '.zshrc' e adiconar na linha 'ZSH_THEME':
    ```
    ZSH_THEME="powerlevel9k/powerlevel9k"
    POWERLEVEL9K_MODE="nerdfont-complete"
    POWERLEVEL9K_SHORTEN_DIR_LENGTH="1"
    POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir rbenv vcs)
    POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(date time)
    ```
    * Documentação: https://github.com/Powerlevel9k/powerlevel9k

  - Adicionar alias no '.zshrc' abaixo de '# navigation alias' (Pode criar n alias para n comandos):
  
    Ex: 
        
    ```
    alias mvntree="mvn org.apache.maven.plugins:maven-dependency-plugin:2.10:tree -Dverbose=true > dependencias.txt
    ```
    
  - Adicionar o Tilix (Criador de abas no terminal):

    ```
    sudo apt-get install -y tilix
    ```
    * Para abrir via teclado, utilizar SHIF + CTRL + T
    * Pode utilizar a fonte hack instalada também
    * Documentação: https://gnunn1.github.io/tilix-web/
  
 Referências:
* [Tutorial 1](https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/)
* [Tutorial 2](https://medium.com/@ivanaugustobd/your-terminal-can-be-much-much-more-productive-5256424658e8)

### Programas DEV:

- Instalando o github desktop:

  https://github.com/shiftkey/desktop

- Instalar o IntellyJ:

  https://www.edivaldobrito.com.br/ide-intellij-idea-no-ubuntu-debian/

  Obs: Instalar plugins 'code with me' e 'EnvFile'

- Instalar SDKMAN (MVN)

  https://sdkman.io/install

- Instalar JDK ZULU (Rodar o comando abaixo para versão 8.0.275.fx-zulu) 
  
  Referêcia: https://www.azul.com/downloads/zulu-community/?package=jdk
  
  ```$ sdk install java 8.0.275.fx-zulu```

- Instalar o maven

  ```$ sdk install maven```

- Instalar docker

  https://docs.docker.com/engine/install/ubuntu/
  
  https://docs.docker.com/engine/install/linux-postinstall/ (evitar docker pedir sudo)
  
  https://docs.docker.com/compose/install/

- Instalar o postman

  https://www.postman.com/downloads/

- Problemas de atalhos com Unbuntu e IntelliJ:

  https://askubuntu.com/questions/412046/unable-to-use-intellij-idea-keyboard-shortcuts-on-ubuntu
  
- Dock Station

  https://dockstation.io/
  
- Notepad++

  https://www.edivaldobrito.com.br/editor-de-codigo-notepad-no-linux/
  
- Vs Code

  https://code.visualstudio.com/download
  
- Dive (Analisar imagem docker)

  https://github.com/wagoodman/dive

## Comandos uteis:

- Instalar o netstat:

  ```sudo apt update && sudo apt install net-tools```  

- Onde esta instalado um programa:

  ```$ whereis nome_do_programa```

- Listar arquivos/diretorios pasta
  
  ```$ ls```

- Criar um arquivo

  ```$ touch nomeArquivo.extenção```

- Limpar a tela do terminal

  ```ctrl+l```

- Abrir terminal

  ```ctrl_alt+t```

- Abrir a pasta do local do terminal

  ```$ nautilus . (ao invez do "." pode passar o nome do arquivo)```

- Salvar configurações atuais como default no linux (antes de reiniciar)

  ```$ alsactl store```

- Pegar ip da maquina

  ```$ ip a (procurar por - ppp0)```

- Liberar porta

  ```$ kill $((lsof -i -n -P | grep 8080) | awk '{print $2}')```
  
  ou
  
  ```
  $ netstat -lnp | grep 8080
  $ kill -9 PID_DO_PROCESSO
  ```

- Desintalar pacote

  ```$ sudo apt-get remove package-name```
  ou
  ```$ sudo apt-get purg package-name```

- Zipar (-r é recursive)

  ```$ zip logs.zip -r 'pasta'```

- Apagar pastasudo chmod ugo+wx /media/username/your_drive

  ```$ sudo rm -R DIRETORIO```

- Adicionar permissão de escrita em nova partição:

  ```$ sudo chmod ugo+wx /media/username/your_drive```
  
- Recarregar fontes do sistema:

  ```$ sudo fc-cache -f -v```

- Buscar diretorios:

  ```find / -type d -name "*tomcat*"```
