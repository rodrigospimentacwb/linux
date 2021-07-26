# Linux (Ubuntu)

#### Atalhos, configurações e outros

## Instalando o ZSH (Terminal):

* [Tutorial 1](https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/)
* [Tutorial 2](https://medium.com/@ivanaugustobd/your-terminal-can-be-much-much-more-productive-5256424658e8)

- Instalar plugin FZF:
 
  https://github.com/junegunn/fzf

- Instalando o FiraCode:

  https://blog.programster.org/ubuntu-install-fira-code-font

- Instalando o github desktop:

  https://github.com/shiftkey/desktop

- Instalar o IntellyJ:

  https://www.edivaldobrito.com.br/ide-intellij-idea-no-ubuntu-debian/

  Obs: Instalar plugins 'code with me' e 'EnvFile'

- Instalar SDKMAN (MVN)

  https://sdkman.io/install

- Instalar JDK ZULU (Rodar o comando abaixo para versão 8.0.275.fx-zulu) 
  
  Referêcia: https://www.azul.com/downloads/zulu-community/?package=jdk
  
  ```$ sdk install java 8.0.275.fx-zulu"```

- Instalar o maven
sudo chmod ugo+wx /media/username/your_drive
  ```$ sdk install maven```

- Instalar docker

  https://docs.docker.com/engine/install/ubuntu/
  
  https://docs.docker.com/engine/install/linux-postinstall/ (evitar docker pedir sudo)

- Instalar o postman

  https://www.postman.com/downloads/

- Git ssh ativação (opcional):
  
  https://docs.github.com/pt/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
  
  ```$ ssh -T git@github.com```


- Problemas de atalhos com Unbuntu e IntelliJ:

  https://askubuntu.com/questions/412046/unable-to-use-intellij-idea-keyboard-shortcuts-on-ubuntu

## Comandos uteis:

- Onde esta instalado um programa:

  ```$ whereis nome_do_programa```

- Listar arquivos/diretorios pasta
  
  ```$ ls```

- Criar um arquivo

  ```touch nomeArquivo.extenção```

- Limpar a tela do terminal

  ```ctrl+l```

- Abrir terminal

  ```ctrl_alt+t```

- Abrir a pasta do local do terminal
sudo chmod ugo+wx /media/username/your_drive
  ```nautilus . (ao invez do "." pode passar o nome do arquivo)```

- Salvar configurações atuais como default no linux (antes de reiniciar)

  ```alsactl store```

- Pegar ip da maquina

  ```ip a (procurar por - ppp0)```

- Liberar porta

  ```kill $((lsof -i -n -P | grep 8080) | awk '{print $2}')```

- Desintalar pacote

  ```$ sudo apt-get remove package-name```
  ou
  ```$ sudo apt-get purge package-name```

- Zipar (-r é recursive)

  ```zip logs.zip -r 'pasta'```

- Apagar pastasudo chmod ugo+wx /media/username/your_drive

  ```sudo rm -R DIRETORIO```

- Adicionar permissão de escrita em nova partição:

  ```sudo chmod ugo+wx /media/username/your_drive```
