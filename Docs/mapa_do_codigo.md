# Mapa do Código

---

## Ideia Principal

Mini Strace - Observa *Chamadas de Sistema (SysCalls)* de Outros Programas.

---
## Tópicos:

### Onde o programa começa?

O programa é iniciado no *src/main.c*, na qual chama a CLI a partir da função *parse_args()* que está dentro do arquivo *src/cli.h*, referenciado no inicio do arquivo main. A CLI intepreta os argumentos passados pelo usuário (formato: ./toytrace trace ...).

### Onde o processo alvo é criado?

O processo alvo é criado no runtime de tracing, no arquivo *src/trace_runtime.c* dentro da função *launch_tracee()* na qual ainda será implementada na SEMANA 2.
Saída Atual: "erro: TODO Semana 2: implementar launch_tracee()"

### Onde o "runtime" chama o "callback"?

O runtime chama o callback durante a execução da função *trace_program()* no arquivo *src/trace_runtime.c*, na qual, ao retornar, chama o callback através da função *trace_observer()* dentro do main.

### Quais arquivos o grupo deve modificar?

- trace_runtime.c 
- formatter.c
- pairer.c

### Qual TODO aparece primeiro ao executar o scaffold?

- erro: TODO Semana 2: implementar launch_tracee()

### Qual a principal dúvida técnica do grupo no momento?

Entender como os arquivos se conectam entre si.