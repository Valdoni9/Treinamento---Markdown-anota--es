# Liberar computador que está fora do dominio para acessar pasta compartilhada

```` {.py3 hl_lines="" linenums="1" title="Ativar pelo Terminal o seguinte comando abaixo"}
Enable-WindowsOptionalFeature -Online -FeatureName smb1protocol
````