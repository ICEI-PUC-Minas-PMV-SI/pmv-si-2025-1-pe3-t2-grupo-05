# 3. DOCUMENTO DE ESPECIFICAÇÃO DE REQUISITOS DE SOFTWARE
## 3.1 Objetivos deste documento
Descrever e especificar as necessidades dos usuários idosos que devem ser atendidas pelo projeto LDI - Livraria Digital para Idosos, apresentando os requisitos funcionais e não funcionais necessários para o desenvolvimento adequado da plataforma. 

## 3.2 Escopo do produto

### 3.2.1 Nome do produto e seus componentes principais
3.2.1 Nome do produto e seus componentes principais 

O produto será denominado LDI - Livraria Digital para Idosos. Ele terá os seguintes componentes principais: 

- Módulo de Usuários 

- Módulo de Catálogo 

- Módulo de Vendas 

- Módulo de Leitura 

- Módulo de Configurações de Acessibilidade 

### 3.2.2 Missão do produto
Disponibilizar uma plataforma de venda e leitura de e-books especialmente adaptada às necessidades dos idosos, facilitando o acesso à literatura digital com uma interface amigável e acessível, promovendo a inclusão digital deste público. 

### 3.2.3 Limites do produto
O LDI não permite o download dos e-books para dispositivos externos, restringindo a leitura apenas dentro da plataforma. O sistema não oferece empréstimo de livros, apenas venda. Não são contemplados recursos de redes sociais ou comunidades de leitores. O LDI não realiza entregas de livros físicos ou conversão de livros digitais para formato impresso. 

### 3.2.4 Benefícios do produto

| # | Benefício | Valor para o Cliente |
|--------------------|------------------------------------|----------------------------------------|
|1	| Interface adaptada para usuários idosos  |	Essencial |
|2 | Acesso remoto à literatura  | Essencial | 
|3 | Recursos de acessibilidade integrados | Essencial | 
|4	| Facilidade na navegação e compra 	| Essencial | 
|5	| Acesso rápido e simplificado ao suporte técnico  	| Essencial | 
|6	| Eliminação da necessidade de deslocamento físico  	| Importante | 
|7	| Tutoriais integrados de uso da plataforma 	| Recomendável | 

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| RF1 | Gerenciar Curso de Aperfeiçoamento |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Cursos de Aperfeiçoamento |
| RF2 |	Gerenciar Professor	| Processamento de Inclusão, Alteração, Exclusão e Consulta de professores |
| RF3	| Gerenciar Matrícula |	Processamento de Inclusão, Alteração, Exclusão e Consulta de Matrículas de alunos em Cursos de Aperfeiçoamento |
| ... |	...	| ... |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição) |
|--------------------|------------------------------------|
| RNF1 | O ambiente operacional a ser utilizado é o Windows XP. |
| RNF2 | O sistema deverá executar em um computador configurado com uma impressora de tecnologia laser ou de jato de tinta, a ser usada para impressão dos relatórios. |
| RNF3 |	Segurança	O produto deve restringir o acesso por meio de senhas individuais para o usuário. |
| ... |	... |	... |

### 3.3.3 Usuários 

| Ator | Descrição |
|--------------------|------------------------------------|
| Coordenador |	Usuário gerente do sistema responsável pelo cadastro e manutenção de cursos de aperfeiçoamento. Possui acesso geral ao sistema. |
| Secretaria |	Usuário responsável por registros de alunos, professores, turmas e gerência de matrículas. |
| ... |	... |	... |

## 3.4 Modelagem do Sistema

### 3.4.1 Diagrama de Casos de Uso
Conforme apresentado no diagrama da Figura 1, o usuário efetua o Login, se estiver cadastrado, caso não, realize o cadastro. Em seguido o mesmo pode buscar, comprar e ler e-books, além de gerenciar sua biblioteca, personalizar acessibilidade e solicitar suporte. O administrador gerencia o catálogo de e-books, enquanto o suporte técnico recebe chamados e presta atendimento aos usuários. 

#### Figura 1: Diagrama de Casos de Uso do Sistema.

![dcu](https://cdn.discordapp.com/attachments/1241910175514886175/1361141234017767716/image.png?ex=67fdad0e&is=67fc5b8e&hm=179a15f1141672255f38f4c8b181a0fe11c5032512216dde0f4140603caac018&)
 
### 3.4.2 Descrições de Casos de Uso

Cada caso de uso deve ter a sua descrição representada nesta seção. Exemplo:

#### Fluxo usuário (CSU01) 
 

**Sumário**: Este caso de uso descreve como um usuário interage com a livraria digital para pesquisar, comprar e ler e-books de forma acessível. 

**Ator Primário**: Usuário 

**Ator Secundário**: Suporte Técnico  

**Pré-condições**: O usuário deve estar cadastrado no sistema; O usuário deve estar autenticado (login realizado com sucesso); O sistema deve estar funcional e acessível. 

 

**Fluxo Principal**: 

1) O usuário acessa a biblioteca digital e faz login. 

2) O usuário navega no catálogo de e-books do sistema. 

3) O idoso pode realizar as seguintes ações:
   
   - Pesquisar um e-book por nome, autor ou categoria. 
   - Visualizar detalhes do e-book, incluindo sinopse e preço. 
   - Adquirir o e-book (caso já não tenha adquirido). 
   - Ler o e-book diretamente no sistema, com opções de acessibilidade. 

 4) O sistema processa a solicitação e exibe a interface de leitura com opções como: 

    - Aumentar o tamanho da fonte. 
    - Aumentar ou diminuir brilho da tela. 
    - Mudar o contraste da tela. 
    - Ativar a leitura em voz alta. 

 5) O idoso pode continuar navegando ou encerrar a sessão. 

**Fluxo Alternativo (1): Erro de Login**

1. Se o usuário apresentar erro de Login: 
   - O usuário deverá realizar o cadastro no sistema. 

**Fluxo Alternativo (3): Pesquisa sem Resultados** 

3. Se nenhum e-book for encontrado na pesquisa: 
   - O sistema exibe uma mensagem informando não haver resultados compatíveis.
   - O idoso pode tentar outra pesquisa ou sair do sistema. 

**Fluxo Alternativo (3): Erro no Pagamento** 

3. Se houver uma falha no pagamento do e-book: 
   - O sistema exibe uma mensagem de erro. 
   - O idoso pode tentar outro método de pagamento ou buscar suporte. 
   - O idoso pode cancelar a compra. 

**Fluxo Alternativo (3): Problema de Acessibilidade** 

3. Se o idoso tiver dificuldade para visualizar ou ouvir o conteúdo: 
   - O sistema fornece um guia rápido de acessibilidade. 
   - O idoso pode acionar o suporte técnico para assistência. 

**Pós-condições**: O idoso consegue acessar os e-books adquiridos sempre que fizer login; O histórico de leituras é salvo para que ele possa retomar a leitura de onde parou; O sistema melhora a experiência do usuário com acessibilidade otimizada. 

### 3.4.3 Diagrama de Classes 

A Figura 2 mostra o diagrama de classes do sistema. A Matrícula deve conter a identificação do funcionário responsável pelo registro, bem com os dados do aluno e turmas. Para uma disciplina podemos ter diversas turmas, mas apenas um professor responsável por ela.

#### Figura 2: Diagrama de Classes do Sistema.
 
![dcu](https://cdn.discordapp.com/attachments/1241910175514886175/1361140446004510830/image.png?ex=67fdac53&is=67fc5ad3&hm=3e2fff56cc6cc4a505a9e886db2affa5cbea5cc22ecdcd53ba45c00ee5592ba8&)
 


### 3.4.4 Descrições das Classes 

| # | Nome | Descrição |
|--------------------|------------------------------------|----------------------------------------|
| 1	|	Aluno |	Cadastro de informações relativas aos alunos. |
| 2	| Curso |	Cadastro geral de cursos de aperfeiçoamento. |
| 3 |	Matrícula |	Cadastro de Matrículas de alunos nos cursos. |
| 4 |	Turma |	Cadastro de turmas.
| 5	|	Professor |	Cadastro geral de professores que ministram as disciplinas. |
| ... |	... |	... |
