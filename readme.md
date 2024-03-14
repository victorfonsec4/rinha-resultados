Resultados no arquivo resultados.txt


Metodologia:

No html gerada pra cada repo nas linhas 674 e 702 tem uma distribuicao de latencies,
exemplo de formato:

categories: ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '14', '15', '16', '18', '20', '21', '22', '24', '25', '26', '27', '28', '29', '30', '34', '35'],

data: [
  63.39,36.22,0.24,0.01,0.01,0.01,0.0,0.0,0.01,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0,0.0
],

No exemplo significa que 63.39% dos requests ficaram em 0 ms, 36.22 em 1 ms ... etc


Seu score total eh a soma da multiplicacao desses valores:

resultado = 63.39\*0 + 36.22\*1 +....

Lembrando que os runs sao meio aleatorios para valores baixos, se vc rodar os testes varias vezes esses resultados serao levemente diferentes.

Algumas runs tem outlier bem grandes e faz com que a maior parte dos resultados estejam
agrupado em um unico grupo, por exemplo:

categories: ['10', ... '100'],

data: [
  '99.99', ..., ,'0.01'
],

Seu programa pode ser injustamente punido por essa falta de resolucao

Se o seu programa teve erros o html gerado vai ter linhas diferentes entao ignorei esses resultados

Abracos
