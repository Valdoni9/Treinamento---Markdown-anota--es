# Exemplo de conversão Banco Fullconvert

> Acessar *Conexão de Área de Trabalho Remota* 000.000.0.000: PC Conversão win 10
> User Pass


### **Acessando FullConvert**
```{.py3 hl_lines="1 3 5 7 9" linenums="1"}
Primero Passo acessar
FullConvert 
Segundo Passo selecionar
New Project Copy
Terceiro Passo selecionar
Database
Quarto Passo selecionar
Firebird ou Access etc..
Quinto Passo Selecionar
O Local para onde vai a conversão database
```
### **Selecionando Firebird como exemplo**
```{.py3 hl_lines="1 3 5 8 11 16" linenums="1"}
Firebird
User: user
Pass: pass
Selecionar o Local database
Next
Conversão
Postgresql
Server: 0.0.0.0
User: exemplo
Pass: exemplo
Nome do banco será nome do cliente_nomedobanco_dataformatoamericano
Next
Yes
Finish
Selecionar a opção (Project options) e inserir o link abaixo 
----Mapping--- (data type Mapping)=>Colocar dentro (double precision=numeric(25,2)
Back
Copy database
Banco Convertido Parabéns

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
