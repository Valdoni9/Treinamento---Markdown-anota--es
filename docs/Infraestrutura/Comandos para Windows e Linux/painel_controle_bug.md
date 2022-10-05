# Comandos para retirar o bug do painel de controle que fica fechando sozinho

### Utilizar os comandos dentro do Terminal do Windows
````{.py3 hl_lines="" linenums="1" title="COMANDOS"}
Ren igfxCPL.cpl igfxCPL.cpl.bak

Taskkill /f /im explorer.exe

Explorer.exe

````