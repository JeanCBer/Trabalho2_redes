# Trabalho 2: Integração de habilidades - 2022/1
**Disciplina: Redes de Computadores 1**

**Curso: Engenharia Elétrica**

**Nome/RA:Jean Carlos Berwanger / 1809954**


## Tarefa 1:  Sub-Redes
| Sub- Rede |             IPv6 - Sub-Rede            |  IPv4 - Sub-Rede  |  IPv4 - Máscara   | IPv4 - Broadcast  |    
|:---------:|:--------------------------------------:|:-----------------:|:-----------------:|:-----------------:|
| Matriz    | 2001:DB8:ACAD:3600::/64 | 200.200.54.0   | 255.255.255.192 | 200.200.54.63  |
| Filial 1  | 2001:DB8:ACAD:3601::/64 | 200.200.54.64  | 255.255.255.224 | 200.200.54.95  |
| Filial 2  | 2001:DB8:ACAD:3602::/64 | 200.200.54.96  | 255.255.255.224 | 200.200.54.127 |
| Filial 3  | 2001:DB8:ACAD:3603::/64 | 200.200.54.128 | 255.255.255.224 | 200.200.54.159 |
| Filial 4  | 2001:DB8:ACAD:3604::/64 | 200.200.54.160 | 255.255.255.224 | 200.200.54.192 |
| Filial 5  | 2001:DB8:ACAD:3605::/64 | 200.200.54.192 | 255.255.255.224 | 200.200.54.223 |
| pb-vit    | 2001:DB8:ACAD:36FF::0:0/112 | 200.200.54.224 | 255.255.255.252 | 200.200.54.227 |
| vit-fb    | 2001:DB8:ACAD:36FF::1:0/112 | 200.200.54.228 | 255.255.255.252 | 200.200.54.231 |
| fb-ita    | 2001:DB8:ACAD:36FF::2:0/112 | 200.200.54.232 | 255.255.255.252 | 200.200.54.235 |
| ita-pb    | 2001:DB8:ACAD:36FF::3:0/112 | 200.200.54.236 | 255.255.255.252 | 200.200.54.239 |
| cv-ita    | 2001:DB8:ACAD:36FF::4:0/112  | 200.200.54.240 | 255.255.255.252 | 200.200.54.243 |


## Tarefa 2: Endereçamento de Dispositivos
| Dispositivo           | Interface |   IPv4       | IPv4 - Máscara | IPv4 - Gateway |      IPv6/Prefixo         |     IPv6 - Gateway      |IPv6 Link-local  |
|-----------------------|-----------|--------------|----------------|----------------|---------------------------|-------------------------|-----------------|
| PC1                   | NIC       |200.200.54.3  |255.255.255.192 |  200.200.54.1  | 2001:DB8:ACAD:3600::3/64  | 2001:DB8:ACAD:3600::1/64|    EUI-64       |
| PC2                   | NIC       |200.200.54.4  | 255.255.255.224| 200.200.54.1   | 2001:DB8:ACAD:3600::4/64  | 2001:DB8:ACAD:3600::1/64|    EUI-64       |
| PC3                   | NIC       |200.200.54.67 | 255.255.255.224| 200.200.54.65  | 2001:DB8:ACAD:3601::3/64  | 2001:DB8:ACAD:3601::1/64|    EUI-64       |
| PC4                   | NIC       |200.200.54.68 | 255.255.255.224| 200.200.54.65  | 2001:DB8:ACAD:3601::4/64  | 2001:DB8:ACAD:3601::1/64|    EUI-64       |
| PC5                   | NIC       |200.200.54.99 | 255.255.255.224| 200.200.54.97  | 2001:DB8:ACAD:3602::3/64  | 2001:DB8:ACAD:3602::1/64|    EUI-64       |
| PC6                   | NIC       |200.200.54.100| 255.255.255.224| 200.200.54.97  | 2001:DB8:ACAD:3602::4/64  | 2001:DB8:ACAD:3602::1/64|    EUI-64       |
| Switch-Matriz         | SVI       | 200.200.54.2 | 255.255.255.192| 200.200.54.1   |                           |                         |
| Switch-Filial1        | SVI       |200.200.54.66 | 255.255.255.224| 200.200.54.65  |                           |                         |
| Switch-Filial2        | SVI       |200.200.54.98 | 255.255.255.224| 200.200.54.97  |                           |                         |
| Roteador-Pato Branco  | Fa0/0     |200.200.54.1  | 255.255.255.224|                | 2001:DB8:ACAD:3600::1/64  |                         |    FE80::1      |
| Roteador-Pato Branco  | Se0/0/0   |200.200.54.225| 255.255.255.252|                |2001:DB8:ACAD:36FF::0:1/112|                         |    EUI-64       | 
| Roteador-Pato Branco  | Se0/0/1   |200.200.54.238| 255.255.255.252|                |2001:DB8:ACAD:36FF::3:2/112|                         |    EUI-64       |
| Roteador-Fco. Beltrão | Fa0/0     |200.200.54.65 | 255.255.255.224|                |2001:DB8:ACAD:3601::1/64   |                         |    FE80::1      |
| Roteador-Fco. Beltrão | Se0/0/0   |200.200.54.233| 255.255.255.252|                |2001:DB8:ACAD:36FF::2:1/112|                         |    EUI-64       |
| Roteador-Fco. Beltrão | Se0/0/1   |200.200.54.230| 255.255.255.252|                |2001:DB8:ACAD:36FF::1:2/112|                         |    EUI-64       |
| Roteador-Vitorino     | Se0/0/0   |200.200.54.229| 255.255.255.252|                |2001:DB8:ACAD:36FF::1:1/112|                         |    EUI-64       |
| Roteador-Vitorino     | Se0/0/1   |200.200.54.226| 255.255.255.252|                |2001:DB8:ACAD:36FF::0:2/112|                         |    EUI-64       |
| Roteador-Itapejara    | Se0/0/0   |200.200.54.237| 255.255.255.252|                |2001:DB8:ACAD:36FF::3:1/112|                         |    EUI-64       |
| Roteador-Itapejara    | Se0/0/1   |200.200.54.234| 255.255.255.252|                |2001:DB8:ACAD:36FF::2:2/112|                         |    EUI-64       |
| Roteador-Itapejara    | Fa0/1     |200.200.54.241| 255.255.255.252|                |2001:DB8:ACAD:36FF::4:1/112|                         |    EUI-64       |
| Roteador-Coronel      | Fa0/0     |200.200.54.97 | 255.255.255.224|                |2001:DB8:ACAD:3602::1/64   |                         |    FE80::1      |
| Roteador-Coronel      | Fa0/1     |200.200.54.242| 255.255.255.252|                |2001:DB8:ACAD:36FF::4:2/112|                         |    EUI-64       |

## Tarefa 3: Tabela de Roteamento
### Roteador Pato Branco
#### IPv4
| Rede de Destino |      Máscara   |    Next Hop  | Interface de Saída |
|-----------------|----------------|--------------|--------------------|
| 200.200.54.228  | 255.255.255.252|200.200.54.226|   SE0/0/0          |
| 200.200.54.232  |255.255.255.252 |200.200.54.226|   SE0/0/0          |
| 200.200.54.64   |255.255.255.224 |200.200.54.226|   SE0/0/0          |
| 200.200.54.240  |255.255.255.252 |200.200.54.226|   SE0/0/0          |
| 200.200.54.96   |255.255.255.224 |200.200.54.226|   SE0/0/0          |
#### IPv6
| Rede de Destino/Prefixo    |        Next Hop           | Interface de Saída |
|----------------------------|---------------------------|--------------------|
|2001:DB8:ACAD:36FF::1:0/112 |2001:DB8:ACAD:36FF::0:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::2:0/112 |2001:DB8:ACAD:36FF::0:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3601::/64     |2001:DB8:ACAD:36FF::0:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::4:0/112 |2001:DB8:ACAD:36FF::0:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3602::/64     |2001:DB8:ACAD:36FF::0:2/112|  SE0/0/0           |


### Roteador Francisco Beltrão
#### IPv4
| Rede de Destino |      Máscara   |    Next Hop  | Interface de Saída |
|-----------------|----------------|--------------|--------------------|
| 200.200.54.0    | 255.255.255.192|200.200.54.234|   SE0/0/0          |
| 200.200.54.224  |255.255.255.252 |200.200.54.234|   SE0/0/0          |
| 200.200.54.240  |255.255.255.252 |200.200.54.234|   SE0/0/0          |
| 200.200.54.96   |255.255.255.224 |200.200.54.234|   SE0/0/0          |
| 200.200.54.236  |255.255.255.252 |200.200.54.234|   SE0/0/0          |
#### IPv6
| Rede de Destino/Prefixo    |        Next Hop           | Interface de Saída |
|----------------------------|---------------------------|--------------------|
|2001:DB8:ACAD:3600::/64     |2001:DB8:ACAD:36FF::2:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::0:0/112 |2001:DB8:ACAD:36FF::2:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::4:0/112 |2001:DB8:ACAD:36FF::2:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3602::/64     |2001:DB8:ACAD:36FF::2:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::3:0/112 |2001:DB8:ACAD:36FF::2:2/112|  SE0/0/0           |

### Roteador Vitorino
#### IPv4
| Rede de Destino |      Máscara   |    Next Hop  | Interface de Saída |
|-----------------|----------------|--------------|--------------------|
| 200.200.54.0    | 255.255.255.192|200.200.54.230|   SE0/0/0          |
| 200.200.54.64   |255.255.255.224 |200.200.54.230|   SE0/0/0          |
| 200.200.54.96   |255.255.255.224 |200.200.54.230|   SE0/0/0          |
| 200.200.54.232  |255.255.255.252 |200.200.54.230|   SE0/0/0          |
| 200.200.54.236  |255.255.255.252 |200.200.54.230|   SE0/0/0          |
| 200.200.54.240  |255.255.255.252 |200.200.54.230|   SE0/0/0          |
#### IPv6
| Rede de Destino/Prefixo    |        Next Hop           | Interface de Saída |
|----------------------------|---------------------------|--------------------|
|2001:DB8:ACAD:3600::/64     |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3601::/64     |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3602::/64     |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::2:0/112 |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::3:0/112 |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::4:0/112 |2001:DB8:ACAD:36FF::1:2/112|  SE0/0/0           |

### Roteador Itapejara D' Oeste
#### IPv4
| Rede de Destino |      Máscara   |    Next Hop  | Interface de Saída |
|-----------------|----------------|--------------|--------------------|
| 200.200.54.0    |255.255.255.192 |200.200.54.238|   SE0/0/0          |
| 200.200.54.64   |255.255.255.224 |200.200.54.238|   SE0/0/0          |
| 200.200.54.96   |255.255.255.224 |200.200.54.242|   Fa0/1            |
| 200.200.54.224  |255.255.255.252 |200.200.54.238|   SE0/0/0          |
| 200.200.54.228  |255.255.255.252 |200.200.54.238|   SE0/0/0          |
#### IPv6
| Rede de Destino/Prefixo    |        Next Hop           | Interface de Saída |
|----------------------------|---------------------------|--------------------|
|2001:DB8:ACAD:3600::/64     |2001:DB8:ACAD:36FF::3:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3601::/64     |2001:DB8:ACAD:36FF::3:2/112|  SE0/0/0           |
|2001:DB8:ACAD:3602::/64     |2001:DB8:ACAD:36FF::4:2/112|  Fa0/1             |
|2001:DB8:ACAD:36FF::0:0/112 |2001:DB8:ACAD:36FF::3:2/112|  SE0/0/0           |
|2001:DB8:ACAD:36FF::1:0/112 |2001:DB8:ACAD:36FF::3:2/112|  SE0/0/0           |

### Roteador Coroneu Vivida
#### IPv4
| Rede de Destino |      Máscara   |    Next Hop  | Interface de Saída |
|-----------------|----------------|--------------|--------------------|
| 200.200.54.0    | 255.255.255.192|200.200.54.241|   Fa0/1            |
| 200.200.54.64   |255.255.255.224 |200.200.54.241|   Fa0/1            |
| 200.200.54.224  |255.255.255.252 |200.200.54.241|   Fa0/1            |
| 200.200.54.228  |255.255.255.252 |200.200.54.241|   Fa0/1            |
| 200.200.54.232  |255.255.255.252 |200.200.54.241|   Fa0/1            |
| 200.200.54.236  |255.255.255.252 |200.200.54.241|   Fa0/1            |
#### IPv6
| Rede de Destino/Prefixo    |        Next Hop           | Interface de Saída |
|----------------------------|---------------------------|--------------------|
|2001:DB8:ACAD:3600::/64     |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
|2001:DB8:ACAD:3601::/64     |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
|2001:DB8:ACAD:36FF::0:0/112 |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
|2001:DB8:ACAD:36FF::1:0/112 |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
|2001:DB8:ACAD:36FF::2:0/112 |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
|2001:DB8:ACAD:36FF::3:0/112 |2001:DB8:ACAD:36FF::4:1/112|  Fa0/1             |
## Topologia - Packet Tracer
- [ ] ![Trabalho2-Topologia-JeanCarlosBerwanger](Trabalho2-Topologia-JeanCarlosBerwanger_VersãoFinal.pkt)


## Arquivos de Configuração dos Dispositivos Intermediários (roteadores e switches)
- [ ] ![Roteador Pato Branco](r-pb-jcb.txt)
- [ ] ![Roteador Francisco Beltrão](r-fb-jcb.txt)
- [ ] ![Roteador Vitorino](r-vit-jcb.txt)
- [ ] ![Roteador Itapejara D'Oeste](r-ita-jcb.txt)
- [ ] ![Roteador Coronel Vivida](r-cv-jcb.txt)
- [ ] ![Switch Pato Branco](sw-pb-jcb.txt)
- [ ] ![Switch Francisco Beltrão](sw-fb-jcb.txt)
- [ ] ![Switch Coronel Vivida](sw-cv-jcb.txt)


