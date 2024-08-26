<p align="center">
  <img height="100" height="auto" src="https://github.com/user-attachments/assets/b88b12d7-60ca-4acc-99cb-e9c66367a156">
</p>

# Titan Testnet — Cassini

Official documentation:
>- [Validator setup instructions](https://titannet.gitbook.io/titan-network-en/cassini-testnet/about-cassini-testnet)

Explorer:
>- [Managment](https://test1.titannet.io/newoverview/activationcodemanagement)

### Minimum Hardware Requirements
 - 8x CPUs; the faster clock speed the better
 - 8GB RAM
 - 5TB of storage (SSD or NVME)

### Recommended Hardware Requirements 
 - 16x CPUs; the faster clock speed the better
 - 16GB RAM
 - 10TB of storage (SSD or NVME)

 - Ubuntu 20.04

Устанавливаем ноду:

``sudo apt update & sudo apt upgrade -y``

``apt install curl iptables build-essential git wget jq make gcc nano tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev lz4 -y``

``apt install docker.io``

``docker pull nezha123/titan-edge``

``mkdir ~/.titanedge``

``docker run --network=host -d -v ~/.titanedge:/root/.titanedge nezha123/titan-edge``

Переходим на [сайт](https://test1.titannet.io/intiveRegister?code=ycYWJQ), регистрируемся. Далее вкладка Console > Node Management > get identity code. Копируем код и не закрываем вкладку пока не привяжем код.

Вместо <CODE>, вписываем свой код без <>.

``docker run --rm -it -v ~/.titanedge:/root/.titanedge nezha123/titan-edge bind --hash=<CODE> https://api-test1.container1.titannet.io/api/v2/device/binding``

Обновляем страницу и видим добавленый узел. Теперь за работу ноды будут капать токены проекта.
