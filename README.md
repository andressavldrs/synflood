# synflood
Esta tarefa visa implementar um ataque de SYN FLOOD. 

Para esta tarefa, você terá que utilizar o LINUX. O trabalho pode ser em dupla. 

Vamos fazer dois ataques: 

1) Usando a ferramenta  HPING3 (http://wiki.hping.org/)

    O Hping3 permite realizar um ataque SYN FLOOD de forma simples (via linha de comando). Vide http://www.binarytides.com/tcp-syn-flood-dos-attack-with-hping/)

2) Via um programa em python (seu) que realize (envie mensagens TCP) para inundar o servidor (ataque SYN FLOOD). Para esta parte, você terá que utilizar RAW SOCKETS e criar um pacote com as devidas FLAGs sentadas e enviar para o servidor a ser atacado. 

    Quem atacar: sugiro vc realizar este teste e fazer o ataque ao seu roteador em uma rede LOCAL (SUA!). Provavelmente o seu roteador deva ter uma interface web e deve estar ouvindo na parta 80. Assim, você poderá realizar o ataque e tentar, de outra máquina fazer o acesso a mesma página. Se tudo correr bem (mal), o seu roteador terá dificuldades em responder a requisição da segunda máquina. Você também pode criar um servidor em fazer o ataque usando o loopback. 

O que vc deve apresentar: 

Relatório explicando:

  a) como o SYN FLOOD funciona ( que é, quais sintomas e quanto tempo o servidor deixa cada conexão aberta aguardando um ACK final).

  b) Mostar como o HPING3 funciona (os comandos utilizados e o cenário de testes) e como ele faz o ataque (capturar e mostrar o nro de mensagens SYN geradas por segundo). Mostrar a capturar e detalhar o pacote da camada TCP). 

  c) Mostrar e detalhar como vc desenvolver o seu programa para realizar a mesma tarefa. Mostrar a captura e comparar com o da ferramenta. 

  d) Realizar os passos b e c para um servidor em python (Server.py). Utilizar ambos o HPING3 e seu programa em python. Use o 

    $ netstat -tuna | grep :<PORT> | grep SYN_RECV

  para mostrar o resultado. 

  e) Qual o efeito que a linha abaixo tem em seu sistema Linux no caso de um ataque SYN Flood? 

    $ net.ipv4.tcp_syncookies = 1
