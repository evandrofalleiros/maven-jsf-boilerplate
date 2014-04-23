maven-jsf-boilerplate
=====================

Este é um boilerplate Maven construído para auxilar no processo de criação e construção de projetos JSF2. A criação repetitiva de projetos com tal descrição é dolorosa, visto que as configurações iniciais são, muitas vezes, bem complicadas. O presente boilerplate irá poupá-lo desse processo todo. Despenda mais tempo com sua aplicação e sua lógica de negócio, ao invés de passar horas, dias, semanas, configurando projetos.<br>

O boilerplate tem incorporado o plugin <a href="http://www.eclipse.org/jetty/documentation/current/jetty-maven-plugin.html"><em>jetty-maven-plugin</em></a>. Este plugin é muito útil para testes e para o desenvolvimento rápido de aplicações JSF2. Também estão presentes no arquivo pom.xml as seguinte dependências: Hibernate (JPA2), MySQL JDBC Driver e PrimeFaces (UI e Mobile) <br>


Analise o arquivo pom.xml para visualizar todas as dependências utilizadas. Caso for utilizar outras dependências, adicione-as ao pom.xml.

=====================

<h1> Como usar </h1>

Para clonar o boilerplate, utilize o seguinte comando Git:

<code> 
  git clone https://github.com/evandrofalleiros/maven-jsf-boilerplate.git
</code>

Após clonarmos o boilerplate, devemos instalar as dependências através do Maven:

<code>
  mvn install
</code>

Agora, com todas as dependências instaladas, o projeto já está pronto para uso. Para o deploy da aplicação, utilize o comando Maven:

<code>
  mvn compile -D jetty.port=9999 jetty:run
</code>

Com isso, o projeto é embutido no Jetty, na porta 9999, e pode ser acessado pela URL <em>http://localhost:9999/</em>. A porta 8080 é padrão quando a diretiva <em>jetty.port=9999</em> não é passada para o <em>mvn</em>:

<code>
  mvn compile jetty:run
</code>

No Eclipse, é possível dar o deploy utilizando o plugin <a href="http://www.eclipse.org/m2e/">Maven m2e</a>. Para tal, acesse o menu <strong>Run -> Run Configurations ...</strong> e crie uma nova configuração <strong>Maven Build</strong>. Na aba <strong>Main</strong>, coloque o valor <strong><em>jetty:run</em></strong> no campo <strong>Goals</strong>. Posteriormente, selecione o botão <strong>Run</strong> para executar o deploy.

Bom proveito.

