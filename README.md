# ruby-socket.io

A Ruby client for Node.js's Socket.IO, enabling real-time, event-based communication between Ruby applications and Socket.IO servers.

![Socket.IO Logo](https://socket.io/images/logo.svg)

## Features

* **WebSocket Support**: Establishes persistent connections using the WebSocket protocol.
* **Event-Driven**: Utilizes an event-based model for handling messages and connections.
* **Lightweight**: Minimal dependencies for ease of integration.

## Installation

To install the gem:

```bash
gem install socket.io-client-simple
```

Alternatively, add it to your Gemfile:

```ruby
gem 'socket.io-client-simple', '< 1.0'  # for Socket.IO v0.9.x
gem 'socket.io-client-simple'           # for Socket.IO v1.4.x
```

Then run:

```bash
bundle install
```

## Usage

Here's a basic example to get started:

```ruby
require 'socket.io-client-simple'

socket = SocketIO::Client::Simple.connect 'http://localhost:3000'

socket.on :connect do
  puts "Connected to server!"
end

socket.on :disconnect do
  puts "Disconnected from server."
end

socket.on :chat do |data|
  puts "Received message: #{data['msg']}"
end
```

For more examples, check out the [samples directory](https://github.com/thiagofeijodev/ruby-socket.io/tree/main/samples).

## Documentation

* [RubyGems: socket.io-client-simple](https://rubygems.org/gems/socket.io-client-simple)
* [Original Project by shokai](https://github.com/shokai/ruby-socket.io-client-simple)

## Contributing

We welcome contributions! To get started:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to your fork (`git push origin feature-name`).
6. Create a new Pull Request.

Please ensure your code adheres to the existing style and includes appropriate tests.

## License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/thiagofeijodev/ruby-socket.io/blob/main/LICENSE) file for details.
