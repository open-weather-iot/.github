# Open Weather IoT. Bem-vindo!

Aqui você pode encontrar os módulos que compõem o projeto de estação meteorológica IoT _open-source_.

Cada base da estação meteorológica é composta pelos seguintes sensores:
- Temperatura: PT100 com conversor RTD (resistance-to-digital) MAX31685
- Umidade Relativa: HDC1080
- Pressão atmosférica: BME680
- Direção e Intensidade do Vento: instrumento de medição construído manualmente baseado no HMC5883L para uso como sensor de efeito hall

Através do protocolo LoRaWAN, a estações meteorológicas enviam em intervalos regulares as medições efetuadas para a estação base.

Por ter uma estrutura modular, o projeto permite que instrumentos de medição sejam adicionados, substituídos ou removidos. Até mesmo o protocolo de comunicação pode ser substituído.

> 🎓 Este projeto nasceu durante a disciplina **Laboratório Experimental do Campus Inteligente** da **UNICAMP**.
