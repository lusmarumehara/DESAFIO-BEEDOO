## Projeto Beedoo Challenge  ![image](https://github.com/user-attachments/assets/13090982-3ac1-4c77-a3c9-e66fba58c084)

A aplicação Beedoo Challenge, desenvolvida em plataforma WEB, foi desenvolvido para a gestão de cursos online permitindo que os instrutores efetuem o cadastro de seus cursos para que os alunos interessados possam visualizar a oferta dos cursos e realizá-los.

O principal objetivo da aplicação é viabilizar de maneira fácil e intuitiva a oferta do cadastro dos cursos aos instrutores bem como a visualização dos mesmos pelos alunos proporcionando seguraça para ambos.
   

## Tomada de Decisão

Ao identificar as duas principais funcionalidades: Cadastro de cursos e Listagem de cursos, iremos focar em requisitos específicos:

Validação e definifição de campos:
Será utilizada uma estrutura para cada campo de maneira apropriada para que o usuário tenha uma melhor experiência na utilização mitigando possíveis erros de inserção e utilizando assim as boas práticas.
Após uma análise identificamos que todos os campos são obrigatórios e a necessidade de validar cada campo a medida que o usuário preenche fornecendo um feedback conforme ele avança no preenchimento do formulário. Do mesmo modo quando houver alguma ação inválida deverá ser implementado mensagens e alertas de erro fornecendo a maneira correta do preenchimento.

Definição da estrutura das User Stories:
A estrutura utilizada será:

Como ( Persona )

Quero ( Ação )

Para ( Intenção )

## User Stories

As User Stories do usuário da aplicação Beedoo Challenge são criadas baseadas nas principais funcionalidades cadastrar, listar e exlcuir cursos na plataforma.
Serão necessário a criação de perfis diferentes para o acesso à plataforma: Admin, instrutor e aluno. Esta necessidade se dá por questões de controle e segurança de como as informações serão acessadas e inseridas na plataforma. Seguiremos com as User Stories baseadas no perfil de Admin pois o mesmo será o único que receberá as permissões full para inserção, consulta e exclusão dos cursos. Este tipo de usuário também será o responsável pela gestão dos perfis de aluno e instrutor, sendo o único que poderá excluir tais perfis.

<b>Feature 'Cadastrar Curso'</b><br>
Como admin <br>
quero criar um novo curso <br>
para adicionar novos cursos na plataforma.

Critérios de Aceite:

Estar somente disponível o acesso para usuários tipo Admin.
O usuário deve inserir todos os dados referentes ao curso, todos os campos são obrigatórios.
O usuário deve ser notificado caso algum campo não tenha sido preenchido de forma adequada com a sugestão de preenchimento correta.
O usuário deve preencher o campo 'Data de Fim' com uma data superior a 'Data de Inicio'
O usuário deve preencher URLs válidas
O usuário deve preencher o número de vagas com um valor positivo maior que 1
O usuário deve visualizar uma mensagem de sucesso ao efetuar o cadastro do curso de forma correta.

<b>Feature 'Listar cursos'</b><br>
Como admin <br>
quero listar todos os cursos cadastrados na plataforma <br>
para visualizar e gerenciar os cursos cadastrados.

Critérios de Aceite:

Estar somente disponível o acesso para usuários tipo Admin.
O usuário deve conseguir consultar todos os dados referentes ao curso, todos os registros cadastrados devem ser mostrados.
O usuário deve poder excluir cursos diretamente da lista de cursos.

<b>Feature 'Excluir cursos'</b><br>
Como admin <br>
quero realizar a exclusão um curso préviamente cadastrado <br>
para manter a plataforma atualizada e limpa.

Critérios de Aceite:

Estar somente disponível o acesso para usuários tipo Admin.
O usuário deve conseguir realizar a exclusão de um curso a partir da lista de cursos disponíveis.
O usuário deve visualizar uma mensagem de confirmação quando um curso for excluído com sucesso.
O curso deve ser retirado da lista de cursos não podendo mais ser visualizado após a exclusão.



1. A página inicial deve listar todos os cursos disponíveis.
2. Cada curso listado deve mostrar pelo menos o nome do curso e a descrição.
3. Ao clicar no nome de um curso, os detalhes completos do curso devem ser exibidos.
