# Python Port Scanner  

Este é um programa simples em Python para realizar a varredura de portas em um endereço IP alvo. Ele verifica quais portas estão abertas em um intervalo especificado e exibe os resultados.

## Funcionalidades  

- Varre portas em um intervalo definido.  
- Exibe quais portas estão abertas no IP alvo.  
- Usa `socket` para conexões de rede, garantindo eficiência e simplicidade.

## Pré-requisitos  

Certifique-se de ter o Python instalado na sua máquina (versão 3.x recomendada).  

## Como usar  

1. Clone este repositório ou copie o código-fonte para sua máquina.  
2. Execute o script Python no terminal.  

```bash
python port_scanner.py
```

## Exemplo de Execução
```bash
Selecione o IP do Alvo: 192.168.1.1  
Scanning 192.168.1.1 for open ports in range range(1, 1025)...  
Port 22 is open on 192.168.1.1.  
Port 80 is open on 192.168.1.1.

Open ports on 192.168.1.1: [22, 80]  
Como Funciona
is_port_open(target_ip, port)
Verifica se uma porta específica está aberta no IP alvo, tentando estabelecer uma conexão.

scan_ports(target_ip, port_range)
Realiza a varredura de todas as portas dentro do intervalo fornecido, utilizando a função is_port_open.
```
## Execução Principal

Solicita o IP alvo ao usuário.
Define o intervalo de portas (atualmente de 1 a 1024).
Exibe as portas abertas ao final da varredura.
Personalização
Alterar o intervalo de portas
Você pode modificar o intervalo de portas ajustando a linha:

python
Copiar código
port_range = range(1, 1025)  
Timeout de Conexão
O tempo de espera para tentar uma conexão pode ser alterado na função is_port_open:

python
```bash
sock.settimeout(1)  # Tempo em segundos
```
