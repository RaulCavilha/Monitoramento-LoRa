# Monitoramento-LoRa

# Projeto LoRa: Telemetria de baixo custo para monitoramento ambiental

## 📜 Descrição do Projeto

Este projeto consiste no desenvolvimento e avaliação de um sistema de telemetria de baixo custo para o monitoramento ambiental de áreas remotas. A solução é baseada na tecnologia LoRa (Long Range) e no protocolo de comunicação MQTT, permitindo a coleta e transmissão de dados em tempo real para qualquer local com acesso à internet.


O sistema é estruturado em três componentes principais:

Estação de Monitoramento (Nó Sensor): Responsável por coletar dados ambientais. No protótipo, foram utilizados um sensor ultrassônico (HC-SR04) para medir o nível da água e um sensor infravermelho (MLX90614) para a temperatura, controlados por uma placa Arduino Nano. Esta estação opera em modo deep sleep para otimizar o consumo de energia.

Estação Intermediária (Gateway LoRa): Atua como uma ponte, requisitando os dados da estação de monitoramento e os retransmitindo para a estação central. Essa estação também utiliza um Arduino Nano e um módulo LoRa, ajudando a centralizar informações de múltiplos sensores e a aumentar o alcance da rede.

Estação Central (Servidor): Recebe os dados, realiza o tratamento e os disponibiliza online. Esta estação é implementada com um Raspberry Pi 4, que se conecta a um módulo LoRa para receber os dados e os publica em um broker MQTT (como o HiveMQ) em formato JSON.

---

## ✨ Funcionalidades

* **Código do Nó Sensor:** Lê dados de um sensor qualquer (ex: temperatura) e os envia via LoRa.
* **Código do Gateway:** Recebe os dados dos nós sensores e os encaminha para uma plataforma ou banco de dados.
* **Script de Análise/Visualização:** Processa ou exibe os dados coletados.

---

## 🛠️ Tecnologias e Hardware

* **Linguagem:** Python, C++ (Arduino)
* **Bibliotecas:** [Nome da biblioteca LoRa usada, ex: RadioHead, LoRaLib]
* **Hardware:**
    * [Modelo do microcontrolador, ex: ESP32, Arduino Uno]
    * [Módulo LoRa, ex: SX1276, RFM95W]
    * [Sensores utilizados, ex: DHT11, BME280]

---

## 🚀 Como Começar

Siga estas instruções para ter uma cópia do projeto rodando localmente.

### Pré-requisitos

O que é necessário para rodar seus códigos?

* Arduino ID
* Python
* Bibliotecas Arduino:
    * ...
* Bibliotecas Python:

### Instalação

Um guia simples de como configurar o ambiente.

1.  **Clone o repositório:**
    ```sh
    git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
    ```
2.  **Configure o Hardware:** Descreva como conectar os módulos e sensores.
3.  **Carregue o código no microcontrolador:** Abra o arquivo `.ino` na Arduino IDE, configure a placa e a porta correta, e faça o upload.

---

## Usage

Instruções sobre como usar seus três códigos.

### 1. Código do Nó Sensor (`Servidor_LoRa.ino`)

Este código deve ser carregado no seu dispositivo sensor.

### 2. Código do Gateway (`Cliente_LoRa.ino`)

Este código deve ser carregado no dispositivo que atuará como gateway.

### 3. Script de Visualização no HiveMQ (`MQTT_LoRa.py`)

---

## 🤝 Como Contribuir

1.  Faça um "Fork" do projeto.
2.  Crie uma nova "Branch" (`git checkout -b feature/sua-feature`).
3.  Faça o "Commit" de suas mudanças (`git commit -m 'Adiciona alguma feature'`).
4.  Faça o "Push" para a "Branch" (`git push origin feature/sua-feature`).
5.  Abra um "Pull Request".

---
