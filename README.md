<h1>Projeto de API REST utilizando Spring Boot 3</h1>
<p>Este é o README do projeto que desenvolvi usando o Spring Boot 3 para criar uma API REST com autenticação via Token e integração com MySQL. Neste projeto, demonstro como criar uma aplicação web moderna que fornece serviços RESTful seguros e armazena dados em um banco de dados MySQL.</p><h2>Objetivo</h2><p>O objetivo deste projeto é criar uma API REST que permita aos usuários realizar operações CRUD (Create, Read, Update, Delete) em recursos específicos, autenticando-se por meio de tokens e persistindo os dados em um banco de dados MySQL.</p>
<h2>Tecnologias Utilizadas</h2>
<ul>
<li>Spring Boot 3: Framework Java que simplifica o desenvolvimento de aplicativos com a configuração mínima.</li>
<li>Spring Security: Fornece recursos de autenticação e autorização, permitindo proteger os endpoints da API.</li>
<li>Token JWT (JSON Web Token): Utilizado para autenticação segura e eficiente na API.</li>
<li>MySQL: Sistema de gerenciamento de banco de dados relacional para armazenar os dados da aplicação.</li>
</ul>
<h2>Configuração</h2>
<ol>
<li>
<p><strong>Clonando o repositório:</strong></p>
<pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>bash</span><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-bash">git <span class="hljs-built_in">clone</span> https://github.com/jcanella/APIRestSpringBoot.git
<span class="hljs-built_in">cd</span> APIRestSpringBoot
</code></div></div></pre></li><li><p><strong>Configurando o Banco de Dados:</strong></p><p>Abra o arquivo <code>src/main/resources/application.properties</code> e configure as propriedades do banco de dados:</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>bash</span><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-bash">spring.datasource.url=jdbc:mysql://localhost:3306/nome_do_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
</code></div></div></pre></li><li><p><strong>Configurando o Token JWT:</strong></p><p>No arquivo <code>src/main/resources/application.properties</code>, defina a chave secreta para assinar os tokens JWT:</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs">app.jwtSecret=chave_secreta_aqui
app.jwtExpirationMs=86400000
</code></div></div></pre></li><li><p><strong>Executando o Projeto:</strong></p><p>Use o Maven para executar o projeto:</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>arduino</span><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-arduino">mvn spring-boot:run
</code></div></div></pre></li></ol><h2>Testando a API</h2><p>Você pode usar ferramentas como o Postman ou o cURL para testar os endpoints da API. Certifique-se de incluir o token JWT recebido após a autenticação nos cabeçalhos das solicitações autenticadas.</p><h2>Considerações Finais</h2><p>Este projeto demonstra como criar uma API REST segura com autenticação via token usando o Spring Boot 3 e integrando-se ao MySQL. Fique à vontade para expandir este projeto adicionando mais recursos, melhorando a segurança ou implementando outras funcionalidades de acordo com suas necessidades.</p><p>Espero que este README tenha fornecido uma visão geral clara do projeto. Se tiver alguma dúvida ou precisar de mais assistência, não hesite em entrar em contato!</p>
