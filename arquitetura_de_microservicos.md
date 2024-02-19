# # Arquitetura de Microserviços

## # Contexto

1. Uma aplicação empresarial de nível crítico está sendo desenvolvida;
2. Mudanças precisam ser entregues de forma rápida, frequente e confiável;
3. As equipes estão dividas grupos pequenos e pouco acoplados;
4. Cada equipe entrega o software utilizando práticas de devops;
5. Uma equipe é responsável por um ou mais subdomínios: 
    - Modelos implementáveis de um pedaço de funcionalidade de negócio;
    - Representam o comportamento do sistema (operações);
    - As operações são invocadas via:
        - Requisições sincronas ou assincronas de clientes;
        - Eventos disparados por outros serviços;
        - Tempo;

## # Problema
Como organizar os subdomínios em um ou mais componentes deployaveis?

## # Forças

### # Forças de Energia Escura

- Componentes Simples;
- Automonia da Equipe;
- Rápidas Pipelines de Deploy;
- Suporte para Múltiplas Stacks de Tecnologia;
- Segregar por Característica; 

### # Forças de Matéria Escura

- Interações Simples;
- Interaçôes Eficientes;
- Prefira ACID a BASE;
- Minimizar o Acoplamento de Execução;
- Minimizar o Acoplamento de Tempo de Design;

## # Solução

- Projetar um arquitetura que estruture a aplicação e componentes pouco acoplados, de deploy independente, conhecidos como **serviços**.
- Cada serviço é composto por um ou mais subdomínios;
- Cada serviço deve possuir seu próprio código fonte e pipeline de deploy;