# PgJSONAttributes-tutorial
##Tutorial sobre cómo guardar y desplegar atributos tipo JSON en Rails <br>
Para el siguiente tutorial se asume que el motor de base de datos es postgresql.

Una de las ventajas que nos proveen los atributos JSON es el hecho que, para entidades que puedan poseer una cantidad de atributos variable, estos pueden ser ingresados y desplegados, sin necesidad de seguir una estructura rígida. A continuación un ejemplo concreto de sobre como utilizar este tipo de atributos.
###Modelo

```ruby
create_table "tools", force: true do |t|
    t.json    "his_attributes"
end
```

###Ingreso de datos

```ruby
Tool.create!(his_attributes: {name: "My first tool", height: "2m"}.to_json)
```
En la siguiente linea de código, al atributo "his_attributes", se le ingresa, en formato JSON, el atributo *name* y *height*. Cabe destacar que, es necesario hacer el parsing a JSON, para que así la información sea ingresada a la BD en el formato correcto.

###Acceso a los datos

```ruby
Tool.his_attributes["name"]
#salida: "My first tool"
```
