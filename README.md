# Guia de Instalação WSL 2 + Docker + Laravel

 1. Etapa 1 – Habilitar o Subsistema do Windows para Linux
 
    1.1 - Digite em seu navegador: http://aka.ms/wsl para acessar a documentação da Microsoft WSL;
    1.2 - Abra o Power Shell como Administrador e execute o comando abaixo:
    
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    
    1.3 - Reiniciar o Computador
    
 2. Abrir a Store Microsft e baixar o sistema operacional desejado, neste exemplo baixei o Ubuntu 20.04 LTS

    ![image](https://user-images.githubusercontent.com/14336962/114484803-3db2b180-9be1-11eb-9661-3d3c83a9b89c.png)
    
 3. Configurar usuário e senha do Linux

 4.  Abra o Power Shell como Administrador, para habilitar o recurso de Máquina Virtual, digitando o seguinte código:

    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    
 5. Próximo passo é baixar o pacote de atualização do kernel do Linux:

    https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
    
 6. Next e Finish para instalar o pacote;
 7. Abra o Power Shell como administrador e digite o comando
    
    wsl --list (para listar as distribuições instaladas no sistema);
    
  8. Agora você precisa definir a versão 2 do WSL na sua distribuição linux:

     wsl --set-version Ubuntu-20.04 2
     
  9. Caso você tenha tido algum problema ao setar a versão 2 do WSL, vc pode verificar a razão da falha utilizando o seguinte comando no power sheall:

     Systeminfo.exe
     
     ![image](https://user-images.githubusercontent.com/14336962/114486362-1d382680-9be4-11eb-8bc8-ec3f591b308b.png)
     
     9.1 - Nesse exemplo acima, tive problemas com a configuração de virtualização do windows, foi necessário habilitar a virtualização no firewall do windows;
     9.2 - Também tive que habilitar a virtualização direto na BIOS da minha placa mãe, essa configuração varia de modelo para modelo.
     9.3 - Para ter certeza estamos na v2 da WSL é necessário aparecer Conversão Concluída após rodar o comando -> wsl --set-version Ubuntu-20.04 2

     ![image](https://user-images.githubusercontent.com/14336962/114487715-743efb00-9be6-11eb-8a04-1ca722967dcf.png)
     
     9.4 - Por último para realmente verificar em que versão esta sua distribução linux, você pode executar o comando:
      
       wsl -l -v
       
       ![Uploading image.png…]()

     

     

 
 


