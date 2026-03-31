Automação de Testes Web: Chronos Academy 🌐
Este projeto consiste em uma suíte de testes automatizados para ambiente Web, desenvolvida para validar as funcionalidades do portal Chronos Academy. A estrutura utiliza padrões de projeto avançados para garantir a manutenção e escalabilidade dos scripts.

🛠️ Tecnologias Utilizadas
Java: Linguagem base para o desenvolvimento da automação.

Selenium WebDriver: Ferramenta core para a manipulação e interação com elementos do navegador (Web).

Page Factory (@FindBy): Extensão do Selenium utilizada para otimizar a localização de elementos e inicialização de objetos.

JUnit/TestNG: Framework para orquestração e execução dos testes.

Maven: Gerenciador de dependências do projeto.

🏗️ Padrão de Arquitetura
O projeto utiliza o padrão Page Objects com uma separação clara de responsabilidades, conforme visualizado na estrutura de pastas:

maps: Armazena exclusivamente o mapeamento de elementos da página (seletores XPath, ID, etc.) utilizando a anotação @FindBy.
pages: Contém a lógica de interação (ações como clicar, escrever, capturar texto).
core: Configurações centrais, como a inicialização do Driver (WebDriver).
tests: Onde residem os scripts de teste e as validações (asserções).

📋 Mapeamentos Implementados
Os arquivos de mapeamento focam na identificação precisa de elementos para os fluxos de navegação:

PrincipalMap
txtTitulo: Identifica o título principal na seção 2 da página.
btnTitulo: Mapeia o botão de ação principal para navegação.

CursoMap
h2Titulo: Localiza o título específico dentro da seção de cursos.

💻 Exemplo de Implementação (Page Factory)
Java
@FindBy(xpath = "//section[2]//h4")
public WebElement txtTitulo;

@FindBy(xpath = "//div[3]/div/div/div[2]//a")
public WebElement btnTitulo;
🚀 Como Executar o Projeto
Clone este repositório:

Bash
git clone https://github.com/seu-usuario/AutomacaoSemComplicacaoWeb.git
Importe o projeto em sua IDE (IntelliJ ou Eclipse) como um projeto Maven.
Certifique-se de ter o ChromeDriver (ou o driver do navegador de preferência) configurado.
Execute os testes através do comando:

Bash
mvn test
