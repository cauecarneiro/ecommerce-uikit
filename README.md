# EcommerceUIKit

Estudo de UIKit que monta as três telas de um app de e-commerce (produtos, carrinho e perfil), cada uma com uma técnica diferente.

Estudo · iOS 26 · 2026

## O que faz

- **Home (Storyboard):** lista de produtos de exemplo em uma `UITableView`, com preço em reais; ao tocar em um produto, abre um alerta "Deseja adicionar ao carrinho?" (o botão Adicionar ainda não grava nada).
- **Carrinho (SwiftUI dentro do UIKit):** lista de itens de exemplo com quantidade, total, exclusão por deslize e botão "Finalizar Compra".
- **Perfil (ViewCode):** menu em seções ("Minha Conta" e "Configurações") montado só por código.
- Navegação por barra de abas (`UITabBarController`) com as três telas.

## Meu papel

Estudo solo. Os cinco commits do repositório são de Cauê Carneiro (de 14 a 21/05/2026), e os arquivos têm os dados de produto escritos no código.

## Como foi feito

- **Três jeitos de montar tela no mesmo app:** `Home/Home.storyboard` com `HomeViewController` (Storyboard), `Cart/CartViewController` hospedando `CartView` (SwiftUI com ciclo de vida UIKit, via `UIHostingController`) e `Profile/ProfileViewController` (ViewCode com Auto Layout).
- **Ciclo de vida UIKit:** `AppDelegate`, `SceneDelegate` e `MainTabBarController` montam o app sem SwiftUI no topo.
- **Tabela com `UITableViewDataSource` e `UITableViewDelegate`**, usando `defaultContentConfiguration` nas células e `NumberFormatter` com a localidade `pt_BR`.
- Dados de produto fixos no código, sem rede nem persistência.

## Tecnologias

Swift, UIKit, SwiftUI (embutido via `UIHostingController`), Storyboard, ViewCode, Auto Layout.

## Como rodar

Abra `EstudoDeCasoUIKit.xcodeproj` no Xcode (alvo de implantação iOS 26.2), escolha um simulador e rode (Cmd+R).

---
Feito por Cauê Crillanovick · [portfólio](https://cauecarneiro.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/cau%C3%AA-carneiro)
