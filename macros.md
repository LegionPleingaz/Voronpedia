
```elixir
[gcode_macro PREHEAT]
gcode:
  {% if params.TEMP is defined %}
    SET_IDLE_TIMEOUT TIMEOUT=18000
    SET_HEATER_TEMPERATURE HEATER=heater_bed TARGET={params.TEMP|default(100)|int}
  {% else %}
    {action_raise_error("TEMP param must be set")}
  {% endif %}

[gcode_macro PREHEAT_END]
gcode:
    #Restore IDLE_TIMEOUT to config value
    SET_IDLE_TIMEOUT TIMEOUT={printer.configfile.settings.idle_timeout.timeout}
```
