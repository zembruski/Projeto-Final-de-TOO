# Sistema de Montadora — UML, Factory, Observer e Modelos de Veículos

Este repositório contém o diagrama UML completo representando a arquitetura de um sistema de produção de veículos utilizando:

✔ Herança e Polimorfismo  
✔ Enum para controle de tipos  
✔ Factory Pattern (criação centralizada de veículos)  
✔ Observer Pattern (departamentos notificados)  
✔ Camadas de Vendas e Estoque  

---

A estrutura modular do projeto separa responsabilidades de forma clara:

| Módulo | Classes Principais | Responsabilidade |
| :--- | :--- | :--- |
| **`models/veiculo.py`** | `Veiculo` (ABC) | Define a interface básica para todos os veículos (Produto Abstrato). |
| **`models/carro.py`** | `Carro`, `TipoCarro` (Enum) | Implementação concreta do `Veiculo` com lógica de preço específica. |
| **`models/moto.py`** | `Moto` | Implementação concreta do `Veiculo` (Preço baseado nas cilindradas). |
| **`models/caminhao.py`** | `Caminhao` | Implementação concreta do `Veiculo` (Preço baseado na capacidade de carga). |
| **`models/factory.py`** | `VeiculoFactory` | Contém o método estático para criar veículos (Simple Factory). |
| **`models/observer.py`** | `Observer`, Observadores Concretos | Define e implementa os comportamentos de notificação. |
| **`models/montadora.py`** | `Montadora` | Gerencia a produção, notifica observadores e lida com a persistência de dados. |
| **`models/vendas.py`** | `SistemaVendas` | Lógica de negócio para vender veículos e gerar relatórios. |
| **`models/estoque.py`** | Funções de persistência | Lida com a serialização e desserialização do estoque (`estoque.json`). |

---

---

## 📐 Diagrama UML (PlantUML)

![Diagrama UML](diagrama.jpg)
