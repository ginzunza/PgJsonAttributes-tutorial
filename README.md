# PgJsonAttributes-tutorial
##Tutorial sobre cómo guardar y desplegar atributos tipo Json en Rails <br>
Para el siguiente tutorial se asume que el motor de base de datos es postgresql.

Una de las ventajas que nos proveen los atributos Json es el hecho que, para entidades que puedan poseer una cantidad de atributos variable, estos pueden ser ingresados y desplegados, sin necesidad de seguir una estructura rígida. A continuación un ejemplo concreto de sobre como utilizar este tipo de atributos.
###Modelo
Si en el esquema se tiene el siguiente modelo:
```ruby
create_table "tool_models", force: true do |t|
    t.json    "his_attributes"
end
```

