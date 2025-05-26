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

| #   | Benefício                                        | Valor para o Cliente |
| --- | ------------------------------------------------ | -------------------- |
| 1   | Interface adaptada para usuários idosos          | Essencial            |
| 2   | Acesso remoto à literatura                       | Essencial            |
| 3   | Recursos de acessibilidade integrados            | Essencial            |
| 4   | Facilidade na navegação e compra                 | Essencial            |
| 5   | Acesso rápido e simplificado ao suporte técnico  | Essencial            |
| 6   | Eliminação da necessidade de deslocamento físico | Importante           |
| 7   | Tutoriais integrados de uso da plataforma        | Recomendável         |

## 3.3 Descrição geral do produto

### 3.3.1 Requisitos Funcionais

| Código | Requisito Funcional (Funcionalidade) | Descrição                                                                                   |
| ------ | ------------------------------------ | ------------------------------------------------------------------------------------------- |
| RF1    | Gerenciar Usuários                   | Processamento de Cadastro, Alteração, Exclusão e Consulta de dados de usuários idosos       |
| RF2    | Gerenciar Acervo                     | Processamento de Listagem, Filtragem, Busca e Visualização detalhada de e-books disponíveis |
| RF3    | Gerenciar Aquisição de E-books       | Processamento de Seleção, Pagamento e Aquisição de e-books pelo usuário                     |
| RF4    | Gerenciar Biblioteca Pessoal         | Processamento de Acesso, Organização e Visualização dos e-books adquiridos pelo usuário     |
| RF5    | Gerenciar Leitura                    | Processamento de Abertura, Navegação, Marcação e Personalização da experiência de leitura   |
| RF6    | Gerenciar Preferências               | Processamento de Configuração, Salvamento e Aplicação de preferências de acessibilidade     |
| RF7    | Gerenciar Ajuda                      | Processamento de Exibição de tutoriais, dicas e suporte contextual ao usuário               |
| RF8    | Gerenciar Favoritos                  | Processamento de Marcação, Visualização e Organização de e-books favoritos                  |

### 3.3.2 Requisitos Não Funcionais

| Código | Requisito Não Funcional (Restrição)                                                                                                                                                                  |
| ------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| RNF1   | A interface deve utilizar elementos amplos, com boa legibilidade e navegação intuitiva, priorizando as necessidades dos usuários idosos. (Usabilidade)                                               |
| RNF2   | O sistema deve oferecer opções de alto contraste, ajuste de fonte e compatibilidade com leitores detela para atender usuários com diferentes limitações visuais. (Acessibilidade)                    |
| RNF3   | O sistema deve funcionar adequadamente em diferentes dispositivos (desktop, tablet e smartphone) com adaptação automática da interface. (Compatibilidade)                                            |
| RNF4   | O tempo de resposta do sistema não deve exceder 3 segundos para qualquer operação, evitando frustração do usuário. (Desempenho)                                                                      |
| RNF5   | O sistema utilizará um código de verificação enviado por e-mail para autenticação. Esse método facilita o login, permitindo acesso rápido e seguro, sem a necessidade de lembrar senhas. (Segurança) |
| RNF6   | A duração máxima das sessões ativas será limitada a 2 horas, para garantir a segurança e a integridade dos dados do usuário, após o qual será necessário realizar novo login. (Segurança)            |
| RNF7   | O sistema deve fornecer feedback visual e sonoro claro para todas as ações realizadas pelo usuário. (Usabilidade)                                                                                    |
| RNF8   | O código deve ser estruturado para facilitar atualizações futuras, especialmente para incorporação de novos recursos de acessibilidade. (Manutenabilidade)                                           |

### 3.3.3 Usuários

| Ator            | Descrição                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Administrador   | Usuário responsável por gerenciar o catálogo de e-books, podendo cadastrar, remover ou atualizar os livros. Ele também gerencia os usuários, ativando, desativando ou modificando suas contas para garantir o uso adequado da plataforma. O administrador tem controle total sobre a plataforma, assegurando a manutenção e organização dos serviços.                                                   |
| Usuário         | Pessoa da terceira idade que utiliza a plataforma para buscar, comprar e ler e-books. Pode personalizar configurações de acessibilidade como tamanho de fonte, contraste e brilho para melhorar sua experiência de leitura. O usuário navega pelo catálogo, gerencia sua biblioteca pessoal e acessa os livros adquiridos exclusivamente dentro da plataforma.                                          |
| Suporte Técnico | Usuário responsável por responder aos chamados via chat, auxiliando e tirando dúvidas dos usuários com problemas no acesso aos e-books ou ao próprio sistema. O suporte técnico possui acesso limitado, restrito apenas às funções de assistência ao usuário, sem permissões administrativas. Oferece orientação especialmente adaptada às necessidades dos idosos, com instruções claras e detalhadas. | ... |

## 3.4 Modelagem do Sistema

### 3.4.1 Diagrama de Casos de Uso

Conforme apresentado no diagrama da Figura 1, o usuário efetua o Login, se estiver cadastrado, caso não, realize o cadastro. Em seguido o mesmo pode buscar, comprar e ler e-books, além de gerenciar sua biblioteca, personalizar acessibilidade e solicitar suporte. O administrador gerencia o catálogo de e-books, enquanto o suporte técnico recebe chamados e presta atendimento aos usuários.

#### Figura 1: Diagrama de Casos de Uso do Sistema

![Diagrama Casos de Uso](/docs/git-img/diagrama-casos-uso.jpg)

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

** Fluxo Alternativo (1): Erro de Login**

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

A Figura 2 mostra o diagrama de classes do sistema de gerenciamento de eBooks. A classe User deve conter informações como identificação, e-mail e senha, além
de estar associada à sua biblioteca pessoal (PersonalLibrary) e lista de favoritos (Favorites). Um Ebook pode estar presente em várias bibliotecas pessoais e listas de
favoritos, mas cada eBook possui apenas um registro no Catalog, que gerencia todos
os eBooks disponíveis no sistema. A classe Sale registra as vendas, associando o
usuário ao eBook comprado e o valor da transação. Além disso, o sistema conta com
suporte técnico (TechnicalSupport) e configurações de acessibilidade (AccessibilitySettings) para melhorar a experiência do usuário, enquanto o Admin gerencia os eBooks e os usuários do sistema.

#### Figura 2: Diagrama de Classes do Sistema

![Diagrama de Classes](/docs/git-img/diagrama-classes.jpg)

### 3.4.4 Descrições das Classes

| #   | Nome                  | Descrição                                                         |
| --- | --------------------- | ----------------------------------------------------------------- |
| 1   | PersonalLibrary       | Cadastro de eBooks na biblioteca pessoal do usuário               |
| 2   | AccessibilitySettings | Configurações de acessibilidade para leitura de eBooks            |
| 3   | Admin                 | Cadastro de gerenciamento de eBooks e usuários pelo administrador |
| 4   | User                  | Cadastro de informações e perfil do usuário                       |
| 5   | TechinicalSupport     | Suporte técnico para usuários, incluindo chat e tutoriais         |
| 6   | Favorites             | Cadastro de eBooks favoritos do usuário                           |
| 7   | Ebook                 | Cadastro de informações detalhadas dos eBooks                     |
| 8   | Sale                  | Cadastro de vendar e processamento de pagamentos                  |
| 9   | Catalog               | Cadastro geral de eBooks disponíveis para busca                   |
