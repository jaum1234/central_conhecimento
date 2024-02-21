# # Forças de Energia Escura

- Metáfora que representa as forças repulsivas que devem ser tratadas ao projetar uma arquitetura;
- São elas:
    - Componentes simples;
    - Autonomia de equipe;
    - Pipeline de implantação rápida;
    - Suporte para múltiplas técnologias;
    - Segragação por característica;

## # Componentes Simples

- Conjunto de subdomínios;
- Deve ser fácil de entender e manter;
- As requisições tratadas por um componente devem ser similares em natureza;
- Isso pode ser alcançado projetando componentes modulares ou componentes menores;

## # Segregação por Característica

- **Necessidade de Recurso:** 
    - Alguns sobdomínios podem exigir menos ou mais recursos do que outros, como CPU, GPU, espaço de armazenamento, memória e etc;
    - Quando um componente consiste em dois subdomínios com necessidade de recursos diferentes, escalar recursos para um subdomínio pode subutilizar recursos para outro subdomínio;

- **Regulações:** Alguns subdomínios podem ser afetados por regulações que atrasam o processo de desenvolvimento, o que pode interferir diretamente no desenvolvimento de outros subdomínios caso façam parte do mesmo serviço.

- **Criticalidade de Negócio:**
- **Segurança**
- **Tipo de Subdomínio DDD:**
