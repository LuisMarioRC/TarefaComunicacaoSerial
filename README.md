# Controle de Display, LED RGB e Matriz de LEDs - RP2040  
## Tarefa: Comunicação Serial e Controle de Hardware  
### Descrição  
Este repositório contém o código-fonte de um projeto desenvolvido em Linguagem C, utilizando o Pico SDK, para implementar a interação entre botões, um display OLED SSD1306, LEDs RGB e uma matriz 5x5 de LEDs WS2812. O projeto explora o uso de comunicação serial UART e I2C, interrupções, e debounce em um microcontrolador Raspberry Pi Pico.  

A solução implementa estratégias para:  
1. Controle de LEDs RGB e LEDs endereçáveis WS2812.  
2. Interação com botões por meio de interrupções e debounce.  
3. Exibição de caracteres no display SSD1306 utilizando o protocolo I2C.  
4. Recebimento de caracteres via UART.  

## Funcionalidades  
1. **Exibição de Caracteres no Display**:  
   - Recebe caracteres do Serial Monitor via UART.  
   - Exibe o caractere no display SSD1306 em tempo real.  
   - Números (0-9) acionam a exibição de símbolos correspondentes na matriz de LEDs WS2812.  

2. **Controle de LEDs RGB**:  
   - Botão A alterna o estado do LED verde (ligado/desligado).  
   - Botão B alterna o estado do LED azul (ligado/desligado).  
   - Mensagens informativas são exibidas no display SSD1306 e no Serial Monitor.  

3. **Matriz de LEDs WS2812**:  
   - Exibe símbolos associados aos números digitados no Serial Monitor.  

4. **Tratamento de Botões**:  
   - Implementação de interrupções para alternar estados.  
   - Debounce via software para evitar múltiplos acionamentos.  

## Pré-requisitos  
1. **Hardware Necessário**:  
   - Raspberry Pi Pico (RP2040).  
   - LED RGB conectado às GPIOs 11, 12 e 13.  
   - Botões pushbutton conectados às GPIOs 5 e 6.  
   - Display OLED SSD1306 (128x64) conectado via I2C (GPIOs 14 e 15).  
   - Matriz 5x5 de LEDs WS2812 conectada à GPIO 7.  

2. **Ambiente de Desenvolvimento**:  
   - Visual Studio Code ou editor compatível.  
   - Pico SDK configurado.  
   - Compilador GCC para C.  
   - Ferramentas de gravação e execução no Raspberry Pi Pico.  

## Como Usar  
1. **Clone o repositório**:  
    ```bash  
    git clone https://github.com/LuisMarioRC/TarefaComunicacaoSerial.git 
    ```  

2. **Navegue até o diretório do projeto**:  
    ```bash  
    cd TarefaComunicacaoSerial 
    ```  

3. **Compile o código com o Pico SDK**:  
   - Certifique-se de que o Pico SDK está configurado corretamente.  
   - No terminal, execute:  
     ```bash  
     mkdir build  
     cd build  
     cmake ..  
     make  
     ```  

4. **Grave o programa no Raspberry Pi Pico**:  
   - Conecte o Pico ao computador.  
   - Entre no modo BOOTSEL e transfira o arquivo `.uf2` gerado na pasta `build`.  

5. **Execute o programa**:  
   - Utilize o Serial Monitor para enviar caracteres.  
   - Pressione os botões para interagir com os LEDs RGB.  
   - Observe a matriz de LEDs exibindo símbolos numéricos.  

## Requisitos Implementados  
1. Uso de interrupções para botões.  
2. Debounce via software para evitar falsos acionamentos.  
3. Controle de LEDs RGB e WS2812.  
4. Utilização do display SSD1306 com suporte a fontes maiúsculas e minúsculas.  
5. Comunicação serial via UART para entrada de caracteres.  

## Testes e Demonstração  
1. **Simulação no Wokwi**:  
   - Configure o simulador conforme as especificações do hardware.  
   - Copie o código para o projeto e teste as funcionalidades.  

2. **Demonstração Física**:  
   - Grave um vídeo demonstrando o funcionamento.  
   - Explique brevemente as funcionalidades implementadas.  
## Vídeo

Confira a demonstração prática no link: [Link do vídeo](https://www.youtube.com/watch?v=Ub32Qpi0m00).

### Líder do Projeto  
- <b><a href="https://github.com/LuisMarioRC">Luis Mario</a></b> 
