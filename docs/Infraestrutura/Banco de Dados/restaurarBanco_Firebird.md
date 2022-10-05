# Script para Restaurar Banco Firebird

> Gbak(função do firebird) tem as duas formas de gerar o backup e restaurar Backup.


### **Acessando pelo Terminal os comandos Firebird**
> Primeiro abra o terminal menu iniciar + R e Digite cmd e aperte o atalho ctrl+shift+enter ele vai acessar como administrador
```{.py3 hl_lines="1 3" linenums="1"}
cd firebird_3_0

cd bin
``` 
### **Primeiro exemplo - Gerando um backup**
```{.py3 hl_lines="" linenums="1"}
User = sysdba | Pass = masterkey
```
```{.py3 hl_lines="" linenums="1"}
gbak –user SYSDBA –pas masterkey 000.00.00.00:c:\dados.fdb c:\backup.fbk
```
### **Segundo exemplo - Restaurando um backup**
```{.py3 hl_lines="" linenums="1"}
gbak -c -v C:\exemplo.fbk  C:\exemplo.new -user sysdba -pas masterkey

```


<!-- ## Custom fences Diagrama
``` mermaid
classDiagram
    Genexus ev3 <|-- Genexus 17
    class Genexus ev3{
        +String Ruim
        +metodo(self): bool
    }
``` -->
