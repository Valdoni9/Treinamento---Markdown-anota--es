# Ativar Duas VPN no mesmo PC

### Solução

```{.py3 hl_lines="6 10 22 23 24" linenums="1" title="Cliente Windows conectando OpenVPN em duas redes diferentes"}

Adicione uma segunda conexão de rede tap

c:\> cd "C:\Program Files\TAP-Windows\bin"

and call

C:\Program Files\TAP-Windows\bin\>  addtap.bat

Verifique o nome da conexão.
C:\Program Files\OpenVPN\bin> openvpn --show-adapters
Available TAP-WIN32 adapters [name, GUID]:
'Local Area Connection 2' {DD2A53C5-63BD-492A-A7F4-94E724007B2A}
'Local Area Connection 3' {EF7623C03-542A-34E8-B633-E3B742983E3}

Put your .ovpn config  and certificates files to the C:\Program Files\OpenVPN\config folder and add the nobind to each config so that a dynamic (UDP) source port is used for each VPN session respective openvpn process.

When a static assignment between a VPN and specific interface is necessary add the TAP Interfacename as parameter of the dev-node option to the openvpn config file:

dev tun1
dev-node "Local Area Connection 3"
port 4097

Nos arquivos de configuração .ovpn adicione a seguinte linha alterando a porta para cada arquivo.

Fonte:

https://michlstechblog.info/blog/openvpn-connect-to-multiple-vpns-on-windows/

```
### [Link da documentação](https://www.curysolucoes.com.br/hesk/knowledgebase.php?article=43)
