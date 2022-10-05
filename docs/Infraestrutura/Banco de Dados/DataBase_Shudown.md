# Erro Database Shutdown

<!-- Começo --> 
*Caso der erro de ***database shutdown*** utilizar o comando a baixo, ele vai fazer o banco ficar online*
<!-- Fim -->

### **Primeiro exemplo - Deixando ele Online**
```
gfix -user "sysdba" -password "senhadobanco" -online G:\exemplo.fdb
```


### **Segundo exemplo - Desligando o Banco**
```
gfix  -user "sysdba" -password "senhadobanco" -shut -force 0 G:\exemplo.FDB

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
