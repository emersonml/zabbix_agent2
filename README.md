# zabbix_agent2

# 186.249.48.235

# criar diretorio
- /srv/volumes/zabbix-agent2/zabbix_agent2.conf
    # add o seguinte conteúdo:
    CONTEUDO=====
    # Configurações básicas do Zabbix Agent 2
    #PidFile=/var/run/zabbix/zabbix_agent2.pid
    PidFile=/tmp/zabbix_agent2.pid  # Mude para /tmp que sempre tem permissão de escrita
    LogType=console
    LogFileSize=0
    DebugLevel=3
    # As linhas 'Server', 'ServerActive' e 'Hostname' serão sobrescritas pelas variáveis de ambiente.
    Server=127.0.0.1
    ServerActive=172.25.0.3:10051
    Hostname=
    ListenPort=10050
    ListenIP=0.0.0.0
    Include=/etc/zabbix/zabbix_agent2.d/plugins.d/*.conf
    Include=/etc/zabbix/zabbix_agent2.d/*.conf
    ControlSocket=/tmp/agent.sock
    =====CONTEUDO FIM

