# .Net-Maui-Generic-Template

[![Licença](https://img.shields.io/badge/licen%C3%A7a-MIT-blue)](LICENSE)
[![.NET Version](https://img.shields.io/badge/.NET-10.0-blueviolet)](https://dotnet.microsoft.com/pt-br/download)

Um template de projeto .NET MAUI robusto e pronto para uso, pré-configurado com a arquitetura **Model-View-ViewModel (MVVM)**.

## 🎯 Sobre o Projeto

Este template foi criado com o objetivo de acelerar o desenvolvimento de aplicações .NET MAUI. Ele elimina a necessidade de configurar manualmente a estrutura de pastas, projetos e o padrão MVVM, permitindo que você comece a codar a lógica de negócio imediatamente.

É a base perfeita para quem busca um projeto limpo, organizado e escalável, seguindo as melhores práticas de separação de responsabilidades.

## ✨ Funcionalidades

* **Arquitetura MVVM Pré-configurada:** Solução separada em projetos para Model, View, ViewModel e Shared.
* **Pronto para Codar:** Clone o repositório ou instale como template e comece a desenvolver.
* **Multiplataforma:** Configurado para Android, iOS, MacCatalyst e Windows.
* **Estrutura Limpa:** Separação clara de responsabilidades entre as camadas da aplicação.
* **Logging:** O `builder.Logging.AddDebug()` já vem habilitado no `MauiProgram.cs` para facilitar a depuração.
* **Projeto Único:** Utiliza a abordagem de projeto único (`SingleProject`) do .NET MAUI.

## 📂 Estrutura do Projeto

A solução é organizada em múltiplos projetos para garantir uma arquitetura limpa e de fácil manutenção:

* **`Template.Host`**: O projeto principal da aplicação .NET MAUI. É responsável pela inicialização do aplicativo (`MauiProgram.cs`) e referencia todas as outras camadas do projeto.
* **`Template.View`**: Contém todas as páginas (Views) da aplicação, como `MainPage.xaml`. Este projeto referencia o `Template.ViewModel` e o `Template.Shared`.
* **`Template.ViewModel`**: Contém as ViewModels, que implementam a lógica de apresentação e o estado das Views. Referencia o `Template.Model` e o `Template.Shared`.
* **`Template.Model`**: Contém os modelos de dados (POCOs - Plain Old CLR Objects) que representam a estrutura de dados da sua aplicação. Referencia o `Template.Shared`.
* **`Template.Shared`**: Um projeto compartilhado para código que pode ser reutilizado em múltiplas camadas, como conversores, interfaces, constantes ou serviços auxiliares.

## 🚀 Como Usar

Você pode usar este projeto de duas maneiras: instalando-o como um template no Visual Studio ou clonando o repositório.

### Opção 1: Instalar como Template (Recomendado)

A forma mais fácil de reutilizar esta estrutura é exportando-a como um template no seu Visual Studio.

1.  Abra a solução (`Template.Host.sln` ou `.slnx`) no Visual Studio.
2.  No menu superior, vá para **Projeto** > **Exportar Template...**
3.  Selecione **Template de Projeto** e clique em "Avançar".
4.  Escolha o projeto `Template.Host` (ele incluirá automaticamente os outros projetos referenciados).
5.  Dê um nome e uma descrição para o seu template (ex: "Template MAUI MVVM Empresarial").
6.  Marque "Importar automaticamente o template para o Visual Studio".
7.  Clique em "Finalizar".

Após isso, você poderá encontrar seu template na tela "Criar um novo projeto" do Visual Studio sempre que for iniciar uma nova aplicação.

### Opção 2: Clonar o Repositório

Você também pode simplesmente clonar este repositório e renomear os projetos e namespaces manualmente para se adequarem à sua nova aplicação.

```bash
git clone [https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git](https://github.com/SEU-USUARIO/SEU-REPOSITORIO.git)
