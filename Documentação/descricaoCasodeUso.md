# 📄 Descrição de Casos de Uso

---

## ✅ UC01 - Cadastrar Anime

| Campo                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nome do Caso de Uso** | Cadastrar Anime                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Objetivo**            | Permitir que o usuário cadastre um anime assistido com as seguintes informações (Nome, Gênero, Nota, Classificação).                                                                                                                                                                                                                                                                                                                                                                                    |
| **Atores**              | Usuário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Pré-condições**       | Não ter um anime cadastrado com o nome digitado                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Pós-condições**       | O anime é cadastrado no sistema                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Fluxo Principal**     | - O usuário acessa a página de cadastro<br>- Digita as informações necessárias<br>- O sistema valida os dados e confirma o cadastro                                                                                                                                                                                                                                                                                                                                                                     |
| **Fluxo Alternativo**   | - Se já existir um anime com o nome digitado, o sistema informa ao usuário                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Fluxo de Exceção**    | - Se ocorrer um erro ao cadastrar o anime, o sistema mostra uma mensagem de erro ao usuário                                                                                                                                                                                                                                                                                                                                                                                                             |
| **Regras de Negócio**   | - Não pode ter animes com nomes iguais<br>- Os campos de nome, gênero e nota devem ser preenchidos<br>- A classificação é gerada automaticamente:<br>  • 10 a 9.0 = ‘Excelente’<br>  • 8.9 a 7.0 = ‘Bom’<br>  • 6.9 a 6.0 = ‘Mediano’<br>  • 5.9 a 0 = ‘Ruim’<br>- A nota deve ser entre 0.0 e 10.0<br>- Os gêneros são salvos como string separada por `\`<br>- O sistema mostra as opções de gênero ao usuário<br>- A imagem deve ser colocada na pasta `back/public/capa`, nomeada com o ID do anime |

---

## ✏️ UC02 - Editar Anime

| Campo                   | Descrição                                                                                                                                                                           |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nome do Caso de Uso** | Editar Anime                                                                                                                                                                        |
| **Objetivo**            | Permitir que o usuário edite informações dos animes cadastrados                                                                                                                     |
| **Atores**              | Usuário                                                                                                                                                                             |
| **Pré-condições**       | Ter um anime cadastrado                                                                                                                                                             |
| **Pós-condições**       | As informações do anime são alteradas                                                                                                                                               |
| **Fluxo Principal**     | - O usuário acessa a página de edição<br>- Pesquisa o anime pelo nome<br>- O sistema busca as informações<br>- O usuário edita os dados<br>- O sistema valida e salva as alterações |
| **Fluxo Alternativo**   | - Se não houver animes cadastrados, o sistema informa ao usuário<br>- Se o nome não for encontrado, o sistema informa ao usuário                                                    |
| **Fluxo de Exceção**    | - Se ocorrer erro ao buscar ou editar o anime, o sistema mostra mensagem de erro                                                                                                    |
| **Regras de Negócio**   | - Nome alterado não pode ser igual ao de outro anime existente<br>- Nota alterada deve estar entre 0.0 e 10.0<br>- Classificação deve ser recalculada se a nota mudar               |

---

## 🔍 UC03 - Pesquisar Anime

| Campo                   | Descrição                                                                                                              |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| **Nome do Caso de Uso** | Pesquisar Anime                                                                                                        |
| **Objetivo**            | Permitir que o usuário pesquise animes pelo nome, gênero ou classificação                                              |
| **Atores**              | Usuário                                                                                                                |
| **Pré-condições**       | Ter um anime cadastrado no sistema                                                                                     |
| **Pós-condições**       | Os animes que correspondem aos critérios pesquisados são exibidos                                                      |
| **Fluxo Principal**     | - O usuário acessa a lista<br>- Pesquisa por nome, gênero ou classificação<br>- O sistema mostra os animes encontrados |
| **Fluxo Alternativo**   | - Se nenhum anime corresponder, o sistema informa o usuário                                                            |
| **Fluxo de Exceção**    | - Se ocorrer erro na pesquisa, o sistema mostra mensagem de erro                                                       |
| **Regras de Negócio**   | **                                                                                                      |

---

## 👁️ UC04 - Visualizar Anime

| Campo                   | Descrição                                                                                           |
| ----------------------- | --------------------------------------------------------------------------------------------------- |
| **Nome do Caso de Uso** | Visualizar Anime                                                                                    |
| **Objetivo**            | Permitir que o usuário visualize todos os animes cadastrados                                        |
| **Atores**              | Usuário                                                                                             |
| **Pré-condições**       | Ter um anime cadastrado no sistema                                                                  |
| **Pós-condições**       | Informações exibidas em uma tabela (Nome, Gênero, Nota, Classificação), junto com a imagem do anime |
| **Fluxo Principal**     | - O usuário acessa a página de lista<br>- O sistema exibe os animes cadastrados                     |
| **Fluxo Alternativo**   | - Se não houver animes cadastrados, o sistema informa ao usuário                                    |
| **Fluxo de Exceção**    | - Se ocorrer erro ao buscar os animes, o sistema mostra uma mensagem de erro                        |
| **Regras de Negócio**   | *                                                                                   |
