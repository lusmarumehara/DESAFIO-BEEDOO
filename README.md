## Projeto Beedoo Challenge  ![image](https://github.com/user-attachments/assets/13090982-3ac1-4c77-a3c9-e66fba58c084)

A aplicação Beedoo Challenge, desenvolvida em plataforma WEB, foi desenvolvido para a gestão de cursos online permitindo que os instrutores efetuem o cadastro de seus cursos para que os alunos interessados possam visualizar a oferta dos cursos e realizá-los.

O principal objetivo da aplicação é viabilizar de maneira fácil e intuitiva a oferta do cadastro dos cursos aos instrutores,
bem como a visualização dos mesmos pelos alunos proporcionando seguraça para ambos.
   

## Tomada de Decisão  ![image](https://github.com/user-attachments/assets/02ba4cef-56ce-41d4-88c8-337b8ca78a78)


Ao identificar as principais funcionalidades: Cadastro de cursos, Listagem de cursos e exclusão, iremos focar em requisitos específicos:

Validação e definifição de campos:
Será utilizada uma estrutura para cada campo de maneira apropriada para que o usuário tenha uma melhor experiência na utilização mitigando possíveis erros de inserção e utilizando assim as boas práticas.
Após uma análise identificamos que todos os campos são obrigatórios e a necessidade de validar cada campo a medida que o usuário preenche fornecendo um feedback conforme ele avança no preenchimento do formulário. Do mesmo modo quando houver alguma ação inválida deverá ser implementado mensagens e alertas de erro fornecendo a maneira correta do preenchimento.

Definição da estrutura das User Stories:
A estrutura utilizada será:

Como ( Persona )

Quero ( Ação )

Para ( Intenção )

## User Stories  ![image](https://github.com/user-attachments/assets/6a16b4b2-665c-4bd6-9ab1-461a015bab32)


As User Stories do usuário da aplicação Beedoo Challenge são criadas baseadas nas principais funcionalidades cadastrar, listar e exlcuir cursos na plataforma.
Serão necessário a criação de perfis diferentes para o acesso à plataforma: Admin, instrutor e aluno. Esta necessidade se dá por questões de controle e segurança de como as informações serão acessadas e inseridas na plataforma. 
Seguiremos com as User Stories baseadas no perfil de Admin que receberá as permissões full para inserção, consulta e exclusão dos cursos. Este tipo de usuário também será o responsável pela gestão dos perfis de aluno e instrutor, sendo o único que poderá excluir tais perfis. O perfil de instrutor receberá a permissão de inclusão e alteração de cursos. O perfil de aluno receberá a permissão de visualizar e realizar os cursos. Cada perfil visualizará o que lhe é permitido, por exemplo o Admin terá acesso a uma área onde haverá o gerenciamento dos perfis e visualizará a opção exlcuir um curso, o instrutor visualizará a inserção e edição dos cursos e o aluno somente visualizará o curso sem opções de exclusão ou edição.

<b>![image](https://github.com/user-attachments/assets/07556581-7200-47ab-8c6c-2d7406b96e37)
Feature 'Cadastrar Curso'</b><br>
COMO usuário admin ou instrutor, <br>
QUERO cadastrar um novo curso, <br>
PARA adicionar novos cursos na plataforma.

Critérios de Aceite:

Estar somente disponível o acesso para usuários tipo Admin e instrutor.
O usuário deve inserir todos os dados referentes ao curso, todos os campos são obrigatórios.
O usuário deve ser notificado caso algum campo não tenha sido preenchido de forma adequada com a sugestão de preenchimento correta.
O usuário deve preencher o campo 'Data de Fim' com uma data superior a 'Data de Inicio', e ser notificado caso preencha uma data inválida.
O usuário deve preencher URLs válidas e ser notificado quando preencher de forma inválida.
O usuário deve preencher o número de vagas com um valor positivo maior que 1 e ser notificado quando preencher incorretamente.
O usuário deve visualizar uma mensagem de sucesso ao efetuar o cadastro do curso de forma correta.

<b>![image](https://github.com/user-attachments/assets/6bbae7a0-f1db-49d5-b2a9-d477d76b12dd)
Feature 'Listar cursos'</b><br>
COMO usuário admin ou instrutor ou aluno, <br>
QUERO listar todos os cursos cadastrados na plataforma, <br>
PARA visualizar e gerenciar os cursos cadastrados.

Critérios de Aceite:

Estar disponível o acesso para todos usuários.
O usuário deve conseguir consultar todos os dados referentes ao curso, todos os registros cadastrados devem ser mostrados.
O usuário deve poder excluir cursos diretamente da lista de cursos.

<b>![image](https://github.com/user-attachments/assets/000f8f35-8bc5-4481-b25c-76038cb9f19c)
Feature 'Excluir cursos'</b><br>
COMO usuário admin, <br>
QUERO realizar a exclusão um curso préviamente cadastrado, <br>
PARA manter a plataforma atualizada e limpa.

Critérios de Aceite:

Estar somente disponível o acesso para usuários tipo Admin por motivos de segurança.
O usuário deve conseguir realizar a exclusão de um curso a partir da lista de cursos disponíveis.
O usuário deve visualizar uma mensagem de confirmação quando um curso for excluído com sucesso.
O curso deve ser retirado da lista de cursos não podendo mais ser visualizado após a exclusão.


## Cenários de Testes  ![image](https://github.com/user-attachments/assets/8b5edc21-20b3-4f47-8d3c-6554255f1fdf)



![image](https://github.com/user-attachments/assets/32d61fb4-3dac-4a98-a577-18d6ed4b3f9f)
<b>CENÁRIO CT-001:</b> Cadastro válido <br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho todos os campos de forma válida <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso cadastrado <br>
AND devo poder visualizar o curso na página  Listar de Cursos


![image](https://github.com/user-attachments/assets/d6f820c4-a37d-46f7-8f54-e65647fa3f62)
<b>CENÁRIO CT-002:</b> Cadastro válido de curso online <br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho todos os campos de forma válida <br>
AND seleciono o tipo de curso online <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso cadastrado <br>
AND devo poder visualizar o curso com modalidade online na página  Listar de Cursos

![image](https://github.com/user-attachments/assets/4781b53c-ab1c-4342-9a41-143f65bf62c9)
<b>CENÁRIO CT-003:</b> Cadastro válido de curso presencial<br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho todos os campos de forma válida <br>
AND seleciono o tipo de curso presencial <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso cadastrado <br>
AND devo poder visualizar o curso com modalidade presencial na página  Listar de Cursos

![image](https://github.com/user-attachments/assets/04bf30b3-f363-4b9f-91c8-554aff2ff220)
<b>CENÁRIO CT-004:</b> Cadastro inválido (campo vazio) <br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND deixo todos os campos sem preencher <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso não cadastrado <br>
AND uma mensagem de aviso indicando os campos não preenchidos deverá ser exibida

![image](https://github.com/user-attachments/assets/e87a3afa-dffb-45e8-b78f-fd5d333a4b08)
<b>CENÁRIO CT-005:</b> Cadastro inválido e url da imagem inválida <br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho os campos de forma válida <br>
AND preencho uma URL da imagem inválida <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso não cadastrado <br>
AND uma mensagem de aviso indicando que os campos foram preenchidos de forma incorreta

![image](https://github.com/user-attachments/assets/c3341aa5-1a09-4c0e-ad35-d94f0dd503ef)
<b>CENÁRIO CT-006:</b> Cadastro inválido e datas inválidas <br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho os campos de forma válida <br>
AND preencho uma data inválida <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso não cadastrado <br>
AND uma mensagem de aviso indicando que os campos foram preenchidos de forma incorreta<br>

![image](https://github.com/user-attachments/assets/a9ae8699-6e41-40fe-a004-18ca3f0083b1)
<b>CENÁRIO CT-007:</b> Listar cursos <br><br>
GIVEN que estou logado como usuário instrutor ou admin ou aluno<br>
AND acesso a página 'Listar Curso' <br>
WHEN clico no botão Listar cursos <br>
THEN devo visualizar todos os cursos previamente cadastrados <br>

![image](https://github.com/user-attachments/assets/d125bd1b-c439-4731-a7e6-9d9ab77c5f9e)
<b>CENÁRIO CT-008:</b> Visualizar cursos <br><br>
GIVEN que estou logado como usuário instrutor ou admin ou aluno<br>
AND acesso a página 'Listar Curso' <br>
AND clico no botão Listar cursos <br>
WHEN clico no curso <br>
THEN devo visualizar todos os dados de um curso previamente cadastrado <br>

![image](https://github.com/user-attachments/assets/e3000e02-0575-4785-857c-cd63f9df7fd9)
<b>CENÁRIO CT-009:</b> Excluir cursos <br><br>
GIVEN que estou logado como usuário admin<br>
AND acesso a página 'Listar Curso' <br>
WHEN clico em 'Excluir curso' no registro do curso a ser excluído <br>
THEN uma mensagem de aviso indicando que a exclusão ocorreu com sucesso deverá ser visualizada<br>
AND não devo visualizar o curso na Lista de Cursos<br>

![image](https://github.com/user-attachments/assets/c3341aa5-1a09-4c0e-ad35-d94f0dd503ef)
<b>CENÁRIO CT-0010:</b> Cadastro inválido e número de vagas inválido<br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
AND preencho os campos de forma válida <br>
AND preencho o campo 'Número de vagas' com -1 ou 0 <br>
WHEN clico no botão Cadastrar curso <br>
THEN devo visualizar uma mensagem de curso não cadastrado <br>
AND uma mensagem de aviso indicando que os campos foram preenchidos de forma incorreta<br><br>

![image](https://github.com/user-attachments/assets/c3341aa5-1a09-4c0e-ad35-d94f0dd503ef)
<b>CENÁRIO CT-0011:</b> Teste de reload na tela listar cursos<br><br>
GIVEN que estou logado como usuário instrutor ou admin ou aluno<br>
AND acesso a página 'Listar Cursos' <br>
WHEN realizo a atualização da página (Reload) <br>
THEN devo visualizar novamente a página 'Listar Cursos' corretamente <br>

![image](https://github.com/user-attachments/assets/c3341aa5-1a09-4c0e-ad35-d94f0dd503ef)
<b>CENÁRIO CT-0012:</b> Teste de reload na tela cadastro cursos<br><br>
GIVEN que estou logado como usuário instrutor ou admin<br>
AND acesso a página 'Cadastrar Curso' <br>
WHEN realizo a atualização da página (Reload) <br>
THEN devo visualizar novamente a página 'Cadastrar Curso' corretamente <br>

Link para planilha: 
<a href="https://docs.google.com/spreadsheets/d/1V8pIjj1hTzgkfk3RVs920H_t983XB8TfUg1WmD9YJUc/edit?usp=drive_link" target="_blank">Resultados dos Testes</a>
                                                                                                                                                          
Link para as Evidências:
<a href="https://drive.google.com/drive/folders/1YVBw7kqaa5jpQQ6ukdb8xh-JpB2VN0ne?usp=drive_link" target="_blank">Evidências dos Testes</a>

## Pontos de melhoria  ![image](https://github.com/user-attachments/assets/08917731-c46c-4673-a076-3a5950bf8b93)


Como pontos de melhorias futuras afim de melhorar a experiência do usuário na utilização da plataforma, destaco as seguintes features:

- Implementação de uma tela de login de usuário para diferênciar os tipo de de usuários da plataforma (Admin, Intrutor e Aluno);<br><br>
- Implementação dos tipos de usuários: Admin (full Access), instrutor (Alterar informações do curso) e Aluno (Listar os cursos e realizá-los);<br><br>
- Implementação de opção de editar curso para os perfis Admin e Instrutor;<br><br>
- Implementação de um limite de caracteres para o campo Nome do curso;<br><br>
- Implementação de um limite de caracteres para o campo Descrição do curso;<br><br>
- Implementação de um limite de caracteres para o campo Instrutor do curso;<br><br>
- Implementação de um valor limite no número de vagas do curso para que ele seja positivo;<br><br>
- Implementação de validação para que a data de fim do curso, sempre seja posterior a data de inicio;<br><br>
- Implementação de uma opção para avaliação de curso,	afim de monitorar a qualidade dos cursos ofertados mediante feedback dos alunos;<br><br>
- Implementação de acessibilidade em libras para deficientes auditivos nos cursos;<br><br>
- Implementação de opção de idioma em inglês para toda a plataforma incluindo os cursos, possibilitando assim abertura exponencial no leque de alunos;<br><br>
- Implementação de uma seção de Status do curso para que o aluno possa acompanhar a sua evolução;<br><br>
- Implementação de um botão de compartilhamento do curso;<br><br>
- Implementação de métricas e testes de performance e segurança, garantindo assim a qualidade da experiência do usuário.<br><br>



