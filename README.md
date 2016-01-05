# PgJsonAttributes-tutorial
Tutorial sobre cómo guardar y desplegar atributos tipo Json en Rails
Para el siguiente tutorial se asume que el motor de base de datos es postgresql.

Si, en el esquema, se tiene el siguiente modelo:
```ruby
create_table "tool_models", force: true do |t|
    t.json    "his_attributes"
end
```
