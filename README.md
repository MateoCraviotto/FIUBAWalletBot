Telegram Bot for FIUBAWallet
====================

# EN
Telegram Bot to interact with the [FIUBAWallet](https://github.com/MateoCraviotto/FIUBAWallet) REST API.

Project for the Software Engineering II course in FIUBA. It consists in a virtual wallet with basic transactions such as virtual currency transfer and expense sharing. The whole project was done in three weeks using Xtreme Programming (Agile Methodology), getting the requirements from a Product Owner and developing the features using Test-Driven Development (TDD) in one week sprints.

## Setup

1. Register a new bot with Telegram's BotFather

* Go to https://web.telegram.org/#/im?p=@BotFather
* Send `/newbot`
* Follow the steps to get the token from the BotFather

2. Copy the file `.env.example` to `.env` and replace `<YOUR_TELEGRAM_TOKEN>` with the obtained token

3. Run the tests with `bundle exec rake`

4. Run the app locally with `ruby app.rb`

## Collaborators
- Mateo Craviotto
- Juan Cruz Roussilian
- Gabriel Belletti
---
# ES
Bot de Telegram para interactuar con la REST API [FIUBAWallet](https://github.com/MateoCraviotto/FIUBAWallet).

Proyecto para la materia 95.21 Métodos y Modelos de la Ingeniería de Software 2, FIUBA. Consiste en una billetera virtual con características simples como transacciones en moneda virtual entre usuarios, además de la posibilidad de compartir gastos, entre otras. El proyecto en su totalidad fue realizado en tres semanas usando la metodología Xtreme Programming, donde se obtenían los requerimientos del Product Owner y se desarrollaba en sprints de una semana usando Test-Driven Development (TDD).

## Setup

1. Registrar un nuevo bot con el BotFather de Telegram

* En Telegram https://web.telegram.org/#/im?p=@BotFather
* Enviarle el comando `/newbot`
* Seguir los pasos y al final el BotFather responde con un token

2. Copiar el archivo `.env.example` a `.env` y reemplazar `<YOUR_TELEGRAM_TOKEN>` con el token del paso anterior

3. Correr los tests con `bundle exec rake`

4. Levantar la app localmente con `ruby app.rb`

## Integrantes
- Mateo Craviotto
- Juan Cruz Roussilian
- Gabriel Belletti

## Testing

Los tests utilizan WebMock. Para testear el cliente, siempre usar `app.run_once` de lo contrario el bot se queda esperando mensajes y el test no finaliza nunca.

## Llamadas a otras API por HTTP

Se puede utilizar la gema incluida en el repo [Faraday](https://github.com/lostisland/faraday#faraday)

## Correr con docker en modo produccion

docker-compose -f docker-compose.prod.yml --env-file ./.env up --build

## Más información

Para utilizar otras funcionalidades de Telegram como los Keyboards especiales ver la doc en: https://github.com/atipugin/telegram-bot-ruby
