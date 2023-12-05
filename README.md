# HTTP Wrapper

El HTTP Wrapper es una gema que proporciona una interfaz simple para realizar solicitudes HTTP utilizando Faraday. Esta gema está diseñada para encapsular la lógica de manejo de errores comunes y proporcionar una interfaz clara para realizar solicitudes a través de Faraday..

## Instalación

```ruby
gem 'http-wrapper'

```
O instálalo manualmente con:
```ruby
gem install http-wrapper
```

## Uso

### Configuración

```ruby

require 'http/wrapper'

# Define las opciones de configuración
base_url = 'https://api.example.com'
api_endpoint = '/endpoint'
headers = { 'Content-Type' => 'application/json' }

# Crea una instancia de Configuration
configuration = Http::Wrapper::Configuration.new(
  base_url: base_url,
  api_endpoint: api_endpoint,
  headers: headers
)

# Crea una conexión Faraday
connection = configuration.connection

# ...continúa con tu lógica de manejo de conexiones...

```

### Realizar una Solicitud

```ruby
require 'http/wrapper'

# Crea una instancia de Client con la configuración previamente definida
client = Http::Wrapper::Client.new(
  base_url: base_url,
  api_endpoint: api_endpoint,
  headers: headers
)

# Realiza una solicitud GET
response = client.request(http_method: :get, endpoint: '/example')

# Maneja la respuesta según sea necesario
puts response

```
## Errores Comunes

El HTTP Wrapper maneja automáticamente los errores HTTP comunes y los encapsula en excepciones específicas para facilitar el manejo.

## License

[MIT](https://choosealicense.com/licenses/mit/)


Si tienes más preguntas o necesitas ayuda con los otros READMEs, no dudes en preguntar.