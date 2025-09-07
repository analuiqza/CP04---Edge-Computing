# CP-04 - Monitoramento de Vinherias com FIWARE + ESP32 🍷

Ana Luiza De Franco e Rinaldi - RM:564061 
Giovana Gaspar Larocca - RM:564965 
Giovanna Lins Sayama - RM:565901 
Rayssa Luzia Portela Aquino - RM:562024

## Descrição 📝
 Nesse projeto implementamos uma prova de conceito (PoC) de monitoramento IoT para vinherias, utilizando ESP32 + Sensor LDR, MQTT e a plataforma FIWARE como back-end, permitindo:
 - Captura de dados de luminosidade em tempo real (sensor LDR no ESP32).
 - Envio de dados para o Orion Context Broker (FIWARE) hospedado em um Máquina Virtual na Azure.
 - Controle de atuadores (LED onboard do ESP32) por meio de requisições no Postman, traduzidas em comandos MQTT.
 - Visualização de roteamento dos dados atráves do Node-RED e do Broker Mosquitto.

## Requisitos 🛠️
 - Conta Azure com permissão para criar VM.
 - ESP32, sensor LDR, cabos.
 - Arduino IDE e Postman instalados.
 - Wokwi para simulação.

### 1) Criar a VM no Microsoft Azure
   - Acesse o Portal Azure.
   - Create a resource -> Virtual Machine
   - Imagem Ubuntu 22.04 LTS
   - Adicione regras inbound no NSG para: SSH, MQTT, Node-RED, Orion
   - Crie a VM e copie o IP público

### 2) Acessar a VM via SSH no terminal local
   - ssh usuario@IP_PUBLICO

### 3) Preparar a VM - Docker e docker-compose
   - sudo apt update && sudo apt upgrade -y
     sudo apt install y docker.io docker-compose git
     sudo usermod -aG docker $USER
  
     docker --version
     docker-compose --version

### 4) Criar o docker compose para FIWARE + Node-RED + Mosquitto

### 5) Acessar Node-RED e abrir ip publico

### 6) Crie fluxos essenciais no Node-RED

### 7) Registre a entidade no Orion (via Postman)

### 8) Prepare o hardware (ESP32 + sensor LDR)
   - Monte o divisor resistivo:
     3.3v -> LDR -> GND
     Nó A - pino ADC no ESP32 (34)
   - Conecte o ESP32 via USP ao PC. 

### 9) Ajustar e Compilaar o código do ESP32
   - Ajuste o main.io.
   - Abra o Arduino IDE e selecione a placa ESP32.
   - Porta COM correta.
   - Compile e carregue.

### 10) Teste com Postman
   - Envie comandos via Node-RED on/off
   - ESP32 (Serial Monitor) mostra mensagem e liga o LED.
   - Node-RED recebe e faz PATCH para Orion.

### 11) Teste das leituras do LDR
   
### 12) Após testes, feche as portas abertas.

 
