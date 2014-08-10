# Ferramentas

## Análise de Desempenho

### [wrk](https://github.com/wg/wrk)

#### Exemplo de Utilização:

Análise durante 30 segundos, utilizando 12 threads e mantendo 400 conexões HTTP abertas.

```
wrk -t12 -c400 -d30s http://127.0.0.1:8080/index.html
```

```
Running 30s test @ http://127.0.0.1:8080/index.html
12 threads and 400 connections
Thread Stats   Avg      Stdev     Max   +/- Stdev
Latency   635.91us    0.89ms  12.92ms   93.69%
Req/Sec    56.20k     8.07k   62.00k    86.54%
22464657 requests in 30.00s, 17.76GB read
Requests/sec: 748868.53
Transfer/sec:    606.33MB
```

## Análise de Tráfego

### iftop

#### Exemplo de utilização:

Análise da interface wlan0 sem a resolução de nomes.

```
iftop -i wlan0 -n
```

![saída do iftop](https://raw.githubusercontent.com/diegosouza/ferramentas-sysadmin/master/imagens/iftop.png)

### nethogs

#### Exemplo de utilização:

Análise de tráfego por processo na interface wlan0.

```
nethogs wlan0
```

![saída do nethogs](https://raw.githubusercontent.com/diegosouza/ferramentas-sysadmin/master/imagens/nethogs.png)

### nload

#### Exemplo de Utilização:

Análise da interface wlan0 somente, mostrando o tráfego em kbytes e o acumulado em mbytes.

```
nload -u K -U M wlan0
```

![saída do nload](https://raw.githubusercontent.com/diegosouza/ferramentas-sysadmin/master/imagens/nload.png)
