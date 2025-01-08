<p align="center">
  <img height="100" height="auto" src="https://github.com/user-attachments/assets/b88b12d7-60ca-4acc-99cb-e9c66367a156">
</p>

# Titan Testnet — Cassini

Official documentation:
>- [Validator setup instructions](https://titannet.gitbook.io/titan-network-en/galileo-testnet/node-participation-guide/run-titan-agent-on-linux)

Explorer:
>- [Managment](https://test4.titannet.io)

### Minimum Hardware Requirements
 - 2x CPUs; the faster clock speed the better
 - 2GB RAM
 - 50GB of storage (SSD or NVME)

### Recommended Hardware Requirements 
 - 4x CPUs; the faster clock speed the better
 - 4GB RAM
 - 100GB of storage (SSD or NVME)

 - Ubuntu 22.04

Устанавливаем ноду:

``egrep -c '(vmx|svm)' /proc/cpuinfo``

``sudo apt update & sudo apt upgrade -y``

``apt install curl iptables build-essential git wget jq make gcc nano tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev lz4 screen -y``

``sudo snap install multipass``

``multipass --version``

``wget https://pcdn.titannet.io/test4/bin/agent-linux.zip``

``mkdir -p /opt/titanagent``

``unzip agent-linux.zip -d /opt/titanagent``

``screen -S titan``

Переходим на [сайт](https://test4.titannet.io), регистрируемся. Далее вкладка Manage Dashboard > Node Management > Your Key. Копируем код.

``cd /opt/titanagent``

``chmod +x agent``

Вместо <your-key>, вписываем свой код без <>.

``./agent --working-dir=/opt/titanagent --server-url=https://test4-api.titannet.io --key=<your-key>``

На сайте во вкладке Node Management видим добавленый узел. Теперь за работу ноды будут капать токены проекта.

Выйтм с скрина CTRL + A + D

Заново зайти ``screen -r titan``

