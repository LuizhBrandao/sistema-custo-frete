# Sistema de Cálculo de Logística e Fretes (POO e Design Patterns)

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![JUnit5](https://img.shields.io/badge/Junit5-25A162?style=for-the-badge&logo=junit5&logoColor=white)
![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![POO](https://img.shields.io/badge/POO-Orientação_a_Objetos-8A2BE2?style=for-the-badge)
![SOLID](https://img.shields.io/badge/SOLID-Princípios-4682B4?style=for-the-badge)
![Design Patterns](https://img.shields.io/badge/Design_Patterns-Strategy-2E8B57?style=for-the-badge)

Este projeto é uma implementação técnica focada em Programação Orientada a Objetos (POO), arquitetura limpa e tratamento avançado de exceções. Desenvolvi esta solução em Java para consolidar conceitos universais de design de software aplicados a regras de negócio reais, estruturando cálculos dinâmicos para categorias distintas de uma frota de veículos (Carros, Caminhões e Bicicletas).

##  O Meu Foco e Aprendizados
Nesta implementação, atuei na construção de um domínio sólido utilizando:
- **Polimorfismo e Herança**: Criação de uma abstração central (`Veiculo`) que dita o contrato de cálculo financeiro (`obterValorTotal()`), permitindo que implementações específicas encapsulem e giram as suas próprias regras de negócio.
- **Padrão Strategy (SOLID - Open/Closed Principle)**: Isolei as regras de tarifas de bibliotecas externas através da interface `TabelaTaxa`. O sistema central está protegido contra mudanças nas tabelas, garantindo baixo acoplamento e altíssima manutenibilidade.
- **Fail-Fast e Logs**: Implementei validações de estado diretamente nos construtores. Caso uma regra seja violada (ex: um caminhão com carga acima do limite), o sistema regista a tentativa através da API de `Logger` e lança Exceções Customizadas.

##  Estrutura e Execução
O projeto não possui dependências externas (como base de dados), garantindo que a execução e a validação do domínio sejam imediatas:
- **`Main.java`**: Simula a instanciação polimórfica de uma frota e o cálculo do valor global.
- **Testes de Unidade (JUnit)**: O projeto conta com uma suite de testes para aferir e auditar todas as regras matemáticas e o bloqueio de estados inválidos na criação dos objetos.