# Firewall TUI

Firewall interativo para Linux, executável totalmente pelo terminal e baseado em nftables.

## Recursos

- Interface interativa no terminal
- Suporte a IPv4 e IPv6
- Gerenciamento de portas TCP e UDP
- Proteção contra rajadas de conexões
- Limitação de ping
- Logs pelo journalctl e rsyslog
- Backup e restauração das regras
- Inicialização automática com systemd
- Validação das regras antes da aplicação

## Requisitos

- Linux
- Bash
- nftables
- iproute2
- systemd
- rsyslog opcional

## Instalação

```bash
sudo apt update
sudo apt install nftables iproute2 rsyslog
sudo install -m 750 firewall-tui /usr/local/sbin/firewall-tui
sudo install -m 644 firewall-tui.service /etc/systemd/system/firewall-tui.service
sudo systemctl daemon-reload
