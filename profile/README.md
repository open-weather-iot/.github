# Open Weather IoT. Bem-vindo!

<p align="center">
  <img src="img/pcb.jpeg" width="400">
  <img src="img/estacao-completa.jpeg" width="400">
</p>

Aqui você pode encontrar os módulos que compõem o projeto de estação meteorológica IoT de código aberto.

Cada base da estação meteorológica é composta pelos seguintes sensores:
- 🌡️ [Temperatura](https://github.com/open-weather-iot/temperature-module): PT100 com conversor RTD (resistance-to-digital) MAX31685
- 💧 [Umidade Relativa](https://github.com/open-weather-iot/humidity-module): HDC1080
- ☁️ [Pressão atmosférica](https://github.com/open-weather-iot/pressure-module): BME680
- 🌬️ [Direção](https://github.com/open-weather-iot/wind-direction-module) e [Intensidade do Vento](https://github.com/open-weather-iot/wind-velocity-module): instrumentos de medição construídos manualmente com base no HMC5883L para uso como sensor de efeito hall
- ⚡ [Tensão interna, da bateria e do painel solar](https://github.com/open-weather-iot/power-supply-module): ADCs internos da placa

Todos os módulos foram desenvolvidos em MicroPython e procuram, na medida do possível, seguir o [guia de padronização](https://github.com/open-weather-iot/template-module) para facilitar contribuições, integração e entendimento do projeto. Mudanças no guia de padronização podem ser feitas para melhorias ou caso alguma particularidade de um sensor específico não seja contemplada. O [código final](https://github.com/open-weather-iot/owi-station) integra todos os sensores.

Através do protocolo LoRaWAN, a estações meteorológicas enviam em intervalos regulares as medições efetuadas para a estação base.

Por ter uma estrutura modular, o projeto permite que instrumentos de medição sejam facilmente adicionados, substituídos ou removidos. Até mesmo o protocolo de comunicação pode ser substituído.

A [API](https://github.com/open-weather-iot/owi-api) foi desenvolvida em NodeJS com TypeScript e utiliza o banco de dados MongoDB. Está hospedada no serviço [Render](https://render.com/) no endereço [https://owi-server.onrender.com](https://owi-server.onrender.com). Atualizações no repositório da API são automaticamente refletidas no Render dentro de alguns minutos.

Foram desenvolvidos alguns [exemplos](https://github.com/open-weather-iot/owi-client-examples) de utilização dos dados disponibilizados pela API em R e Python.

<p align="center">
  <img src="img/jupyter-notebook-examples.png">
</p>

Está disponível um dashboard no Grafana ([link privado para a organização](https://owi.grafana.net/d/9qq-1uI4k/open-weather-iot), [link público](https://owi.grafana.net/public-dashboards/372bdd2f0d964c989c6aa860281985cb)) que consome os dados da API através de uma conexão websocket. No momento da escrita, 14 dez 2022, ainda não é suportado o data source "WebSocket API" em dashboards públicos, logo, não exibirá nenhum dado no link público.

<p align="center">
  <img src="img/grafana-dashboard.png">
</p>

> 🎓 Este projeto foi desenvolvido durante a disciplina **Laboratório Experimental do Campus Inteligente** da **UNICAMP**, lecionada pelo professor [@fruett](https://github.com/fruett).
