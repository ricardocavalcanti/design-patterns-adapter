# 💡 Design Pattern: Adapter (Java)

Este repositório demonstra a aplicação do padrão de projeto Adapter utilizando Java puro. 
No exemplo, diferentes serviços de notificação (Email, Push e Alerta) são adaptados para uma interface comum `NotificationSender`.

---

## 🎯 Objetivo

- Permitir que classes com interfaces incompatíveis trabalhem juntas.
  
---
## 📁 Estrutura do Projeto

```bash
design-patterns-adapter/
├── src/
│   └── br/
│       └── com/
│           └── pattern/
│               ├── adapter/
│               │   ├── NotificationSender.java      (interface alvo)
│               │   ├── EmailService.java             (serviço legado 1)
│               │   ├── PushService.java              (serviço legado 2)
│               │   ├── AlertService.java             (serviço legado 3)
│               │   ├── EmailAdapter.java             (adapter para Email)
│               │   ├── PushAdapter.java              (adapter para Push)
│               │   └── AlertAdapter.java             (adapter para Alert)
│               ├── service/
│               │   └── NotificationService.java      (usa NotificationSender)
│               └── Main.java                         (exemplo funcional)
├── .gitignore
├── 
```

---

## ⚙️ Tecnologias

- Java 17
- Maven

---

## ▶️ Como executar
### Compile
- mvn compile

### Execute
- mvn exec:java -Dexec.mainClass="br.com.pattern.strategy.br.com.pattern.Main"

---

## 🧪 Exemplo de saída
Pagamento CLT: 5000.0
Pagamento PJ: 7000.0
Pagamento Estágio: 1200.0

---

## 📚 Conceitos aplicados

- Encapsulamento: O adapter encapsula a adaptação entre duas interfaces incompatíveis, escondendo a complexidade da conversão.

- Polimorfismo: Permite que o adapter seja usado no lugar da interface esperada, oferecendo a mesma interface para o cliente.

- Abstração: A interface comum define o contrato que o adapter e o cliente usam, garantindo que o cliente não precise conhecer detalhes da implementação adaptada.

- Delegação: O adapter delega chamadas para o objeto adaptado, convertendo as chamadas conforme necessário.

- Reutilização de código: Permite usar classes existentes sem modificá-las, adaptando-as para trabalhar em um novo contexto.

- Baixo acoplamento: O cliente depende da interface comum, e não das implementações concretas, facilitando mudanças e extensões

---







