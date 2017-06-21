# Telegram Integration Pack

StackStorm integration with [Telegram](https://telegram.org) messaging application.

## Configuration

Copy the example configuration in [telegram.yaml.example](./telegram.yaml.example)
to `/opt/stackstorm/configs/telegram.yaml` and edit as required.

It should contain:

* ``apikey`` - Telegram API 

You can also use dynamic values from the datastore. See the
[docs](https://docs.stackstorm.com/reference/pack_configs.html) for more info.

**Note** : When modifying the configuration in `/opt/stackstorm/configs/` please
           remember to tell StackStorm to load these new values by running
           `st2ctl reload --register-configs`

## Sensors

### TelegramSensor

This sensor monitors Telegram every 5s, for new messages.
When a new update is detected, it dispatches a trigger.

## Actions

* ``send_message`` - Send a message to a user or group
