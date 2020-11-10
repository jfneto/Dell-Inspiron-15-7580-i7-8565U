# Dell-Inspiron-15-7580-i7-8565U
Inspiron 15 7000 Series - 7580 (i7-8565U)

## Details - Inspiron 15 7000 Series - 7580

  * 8th Generation Intel Core i7-8565U Processor
  * SSDR 128 + HD 1T (NVMe 512gb)
  * 16GB (2x8GB) 2666MHz DDR4 Memory
  * 802.11ac 2x2 WiFi and Bluetooth (????)
  * Audio Realtech 3254 (ALC295)
    * Sem patch no DSDT: 
      ~~O unico `layout id` que funcionou foi o 77 e sem o fone, detalhe quando o fone era conectado trocava corretamente para o dispositivo fone mas depois disso travava e o som não voltava mais a ser todado no autofalante.~~
    * Com Patch DSDT: 
      ~~Passou a reconhecer o audio *(Testei de certeza apenas os layouts 13, 14, 15, 28. Por isso irei repassar todos para ter certeza.)* ele passou a reconhecer quando o fone é plugado e voltar para o autofalante ao remover o fone corretemante, porém ainda não emite som no fone, (Já vi em alguns forums gringos que tem gente com esse codec com o mesmo problema).~~
      O DSDT com patch + a AppleALC atual reconhecem o id 77. Porém para o audio do fone funcionar corretamente precisa instalar o `ALCPlugFix` contido na pasta mojave/Tools/ALCPlugFix basta executar o `install.command` e reiniciar, que o fone será reconhecido e funcionará perfeitamente.
      
> O Path DSDT que usei foi: `Hpet Fix` e `IRQ Fix`. Também removi os fixes da config.plist `Fix ipic` `Fix hpet` `Fix tmr` `Fix rtc`      

  * Intel 620UHD 
  
    Utilizei o hacktoshtool para gerar uma confg.plist que forçou o reconhecimento correto. Me base-ei neste link para fazer funcionar. Eu selecionei meu processador como `coffee lake` já que não tem `whiskey lake`.    
    http://hackintoshbrasil.com/forum/viewtopic.php?f=22&t=88&sid=67d4338f2f0211a864a1261dc24514a4

  * Intel 9260 Wireless Driver (Don't Work) 
    * Estou usando um TPLink823N-V3 com o aplicativo de conexão da propria TPLink.
    * Existe um port do driver linux para o mac, ainda não esta acabado, mas se alguém que programe quiser dar uma ajuda, aqui tá o link do meu fork https://github.com/jfneto/IntelWifi
    
  * NVIDIA GeForce MX150 2GB GDDR5 (Don't Work)
     
## Layout teclado

  A Apple alterou as teclas aspas e pipe a solução paliativa foi utilizar o layout abaixo. 
  Usar o layout de teclado `Brasil ABNT2.bundle` que esta na pasta `Layout de Teclado Corrigido` e inserir na pasta `/Library/Keyboard Layouts`, reiniciar para carregar as configurações corretamente (Algumas vezes logoff não recarrega) ir em configurações de teclado e selecionar o layout `Brasil PC` é o que está funcionando para mim.

  ~~* https://sourceforge.net/projects/layoutabnt2/~~


  
  
