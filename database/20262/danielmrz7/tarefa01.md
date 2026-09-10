# Tarefa 01 - Conceitos de BD, ACID e SGBD

**Conceitos de Git e GitHub**

* **Branches:** São tipo universos paralelos do seu código. Você cria uma branch para testar um widget novo em Flutter ou fazer uma feature sem risco de quebrar o código oficial (a branch `main`).
* **Pull Request (Merge Request):** O famoso PR. É você sinalizando no GitHub: "terminei as alterações aqui na minha branch, avalia aí se podemos juntar com o projeto principal".
* **Merge:** É a costura final. O Git pega a sua branch e une o histórico dela com a branch principal.
* **Rebase:** Faz algo parecido com o merge, mas reescreve a história. Ele puxa seus commits e os joga lá na ponta da branch principal, deixando o histórico reto, sem aquelas curvas visuais de merge.
* **Conflitos:** A dor de cabeça clássica. Acontece quando duas pessoas mexem na exata mesma linha de um arquivo. O Git trava e manda você escolher manualmente qual versão deve ficar.

**Q1. Banco de Dados vs. SGBD**

* **Banco de Dados (BD):** São os dados puros armazenados de forma estruturada. Pense nas informações de clientes e funcionários que você organizava naquelas structs em C no projeto SIG-Bike, só que guardadas em larga escala e interligadas.
* **SGBD (Sistema Gerenciador de Banco de Dados):** É o software parrudo que faz o meio de campo. Ele gerencia as regras de negócio, a segurança e a forma como a gente consulta esses dados.

**Exemplos:**
* **SGBDs:** PostgreSQL, MySQL, Oracle, MongoDB.
* **Bancos de Dados:** O banco acadêmico do SIGAA, o banco de um app de delivery, ou um dataset de clima no Kaggle pronto pra ser minerado em Python.


**Q2. O problema de usar Sistemas de Arquivos**

Se a gente guarda tudo em arquivos soltos pelo sistema, surgem vários problemas graves:
* **Redundância:** A mesma informação fica duplicada em vários cantos.
* **Inconsistência:** Você altera o dado em um arquivo, esquece do outro, e a base passa a apresentar informações divergentes.
* **Acesso difícil:** Para criar um filtro ou uma busca diferente, muitas vezes você precisa programar um script do zero só para ler o texto.
* **Zero segurança:** Qualquer processo ou usuário com acesso à pasta pode corromper o arquivo inteiro.

**Q3. Propriedades ACID (com exemplo de Transferência Bancária)**

* **Atomicidade (Tudo ou Nada):** A operação não pode parar na metade. Se você manda 50 reais de transferência pra sua mãe, o dinheiro tem que sair da sua conta e cair na dela. Se falhar, tem que desfazer tudo; senão, o dinheiro sumiria no limbo.
* **Consistência:** O banco precisa respeitar as regras matemáticas e lógicas. Se você não tem limite de cheque especial, uma transferência não pode deixar sua conta negativa.
* **Isolamento:** Duas requisições simultâneas não podem bater cabeça. Se você passar o cartão duas vezes no exato mesmo milissegundo, o sistema não pode ler o saldo antigo para aprovar as duas, ignorando que o dinheiro só dava pra uma.
* **Durabilidade:** Viu a tela de "Sucesso"? Tá salvo de verdade. Se o servidor da TIM ou do banco reiniciar um segundo depois, o dado já tem que estar gravado no disco físico e não pode se perder.