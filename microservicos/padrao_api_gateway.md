# # Padrão API Gateway

## # Problema
Normalmente, os clientes de uma aplicação baseada em microserviços precisam acessar múltiplos serviços individualmente para construir a experiência de uma única página, o que pode resultar em alguns problemas: 

- Diferentes clientes (aplicações web, desktop, mobile e etc) terão problemas de performance diferentes devido a grande quantidade de requisições necessárias;
- Cada serviço pode implementar protocolos de comunicação diferentes, o que força cliente a entender detalhes sobre os quais ele não deveria;
- Diferentes clientes podem possuir diferentes necessidades;

## # Solução

Implementar um API Gateway que se responsabilize por receber as requisições de cada cliente de forma centralizada e resolve-las, como por exemplo, redirecionando a requisição para o serviço correto.

Uma outro solução, conhecido como Backends para Frontends, consiste em implementar uma API Gateway para cada tipo de cliente.

## # Referências Bibliográficas

- https://microservices.io/patterns/apigateway.html