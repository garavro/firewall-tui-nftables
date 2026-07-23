
# Firewall TUI

<img width="469" height="460" alt="Captura de tela_2026-07-22_21-40-38" src="https://github.com/user-attachments/assets/d039c7b5-d1ce-4bd7-8d87-f03ed74ed701" />

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

- sudo apt update
- sudo apt install nftables iproute2 rsyslog
- sudo install -m 750 firewall-tui /usr/local/sbin/firewall-tui
- sudo install -m 644 firewall-tui.service /etc/systemd/system/firewall-tui.service
- sudo systemctl daemon-reload

## Executar

- sudo firewall-tui

## Comandos

- sudo firewall-tui start
- sudo firewall-tui stop
- sudo firewall-tui restart
- sudo firewall-tui status
- sudo firewall-tui logs
- sudo firewall-tui backup
- sudo firewall-tui restore

## Inicialização automática

- sudo systemctl enable --now firewall-tui.service

## Aviso

- Este programa modifica regras de firewall do sistema. Faça testes localmente antes de utilizá-lo em servidores remotos.

- Caso esteja conectado por SSH, permita a porta SSH antes de ativar o firewall.
