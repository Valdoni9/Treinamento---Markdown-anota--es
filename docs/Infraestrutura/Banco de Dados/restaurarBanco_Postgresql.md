# Script para Restaurar Banco Postgresql

> pg_restore(função do Postgresql) comando para resturar banco.


### **Acessando pelo Terminal os comandos Postgre**
> Primeiro abra o terminal menu iniciar + R e Digite cmd e aperte o atalho ctrl+shift+enter ele vai acessar como administrador

### **Restaurando banco postgre**
```
pg_restore --dbname=DBNAME --no-tablespaces --host=HOSTNAME --port=5432 --username=USERNAME --verbose -F d -j 6 /mnt/backup

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
