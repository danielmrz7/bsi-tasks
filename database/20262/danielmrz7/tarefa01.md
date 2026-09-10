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