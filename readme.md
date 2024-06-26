# Arquitetura MVC do projeto

O objetivo deste documento é mostrar o processo de criação do padrão de arquitetura MVC no projeto que está sendo desenvolvido para a Dell. Assim, o padrão MVC é um padrão de arquitetura de software que define regras para que o desenvolvimento seja ágil, escalável e trabalhado em equipes. O padrão MVC é separado em três camadas: Model, View e Controller.
<br><br>
Primeiramente, o Model é a camada que representa a lógica da aplicação, que faz a comunicação com o banco de dados, fazendo a seleção dos dados na tabela. Após isso, a View que é a camada de apresentação, que é responsável por exibir os dados para o usuário. Por fim, o Controller, que é a camada intermediária entre a Model e a View, que é responsável por receber as requisições do usuário (que foram recebidas no router e encaminhadas para o controller) e enviar para a Model, e após isso, enviar para a View. Com isso, uma aplicação com uma arquitetura bem definida e um padrão de projeto que, deve ser seguido durante o desenvolvimento do projeto.

## Figura 1: Arquitetura MVC
<img src="./assets/MVCProject.png" alt="Arquitetura MVC" width="75%"/>
<br>
<a href="https://www.figma.com/file/6AUz2hstC2mqUE3F6AagAh/MVCProject?type=whiteboard&node-id=0%3A1&t=6qMOblp313ePnieX-1" target="">Link para leitura</a>
<br>
Primeiramente, temos a camada de Model que faz a comunicação com as tabelas do banco de dados, e na representação estão contido os atributos. "Mounter Teams Model" é a classe que faz a comunicação com a tabela "mounter_teams" do banco de dados, e tem os atributos: id, nome e descrição. Logo em seguida temos a "User Model" que faz a comunicação com a tabela "users" do banco de dados, e tem os atributos: id, nome, email, senha, regra (verifica se é administrador ou não) e mounterTeamId. Seguindo a mesma lógica, tem-se os models de Modelos (se é um notebook Dell Latitude 3540, por exemplo), os manuais (que são os manuais de montagem dos notebooks), as tarefas (que são as tarefas que os montadores devem fazer) e a tabela de favoritos (que é a tabela que armazena os favoritos dos montadores). Esses são os *models* que estão sendo utilizados e que fazem a comunicação com o banco de dados.
<br><br>
Partindo para o Controller, para cada respectivo model citado acima, levando em consideração que o controller vai pegar as informações e passar para a nossa terceira camada da aplicação que é a View. A view é a camada responsável por pegar as informações que o Controller pegou do Model e passar para o cliente (navegador) e então, a aplicação será renderizada.
<br><br>
Por fim, o Router que é a camada responsável por receber as requisições do cliente e encaminhar para o Controller correto, e após isso, o Controller vai pegar as informações do Model e passar para a View, que vai renderizar a aplicação. Com isso, uma aplicação com uma arquitetura bem definida e um padrão de projeto que, deve ser seguido durante o desenvolvimento do projeto.