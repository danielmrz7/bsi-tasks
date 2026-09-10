# Tarefa 02 - MER e Projeto de Banco de Dados Relacional

## Q1. Elementos básicos de um Modelo Entidade-Relacionamento (MER)

O Modelo Entidade-Relacionamento é composto fundamentalmente por três elementos básicos:

1. **Entidades:** Representam objetos, seres ou conceitos do mundo real que possuem uma existência independente e sobre os quais desejamos armazenar dados (ex.: `Cliente`, `Funcionario`). No diagrama, são representadas por retângulos.
2. **Relacionamentos:** Representam associações lógicas entre duas ou mais entidades, indicando como elas interagem entre si (ex.: um `Funcionario` *trabalha em* uma `Squad`). No diagrama conceitual, são representados por losangos.
3. **Atributos:** São as propriedades ou características que descrevem as entidades ou os relacionamentos (ex.: o `nome` e o `email` de um `Funcionario`). Podem ser simples, compostos, multivalorados ou derivados.

## Q2. Notações para Diagramas ER

Existem diferentes notações padronizadas para representar Modelos Entidade-Relacionamento graficamente. Abaixo estão algumas das principais e como representam conceitos comuns:

* **Notação de Chen (Original):** Utiliza retângulos para entidades, losangos para relacionamentos e círculos (elipses) para os atributos conectados às entidades. As cardinalidades são indicadas por letras (`1:N`, `M:N`) ou pares numéricos sobre as linhas.
* **Notação de Pé de Galinha (Information Engineering / Crow's Foot):** Muito utilizada em projetos relacionais modernos e ferramentas como o Mermaid.js. As entidades são caixas contendo os atributos, e os relacionamentos são linhas com símbolos nas pontas que indicam a cardinalidade (ex.: barras verticais para "um", e ramificações em forma de pé de galinha para "muitos").
* **UML (Unified Modeling Language - Diagrama de Classes):** Utiliza classes para representar entidades, atributos dentro do corpo da classe e associações com multiplicidades explícitas (ex.: `1..*` ou `0..1`) nas pontas das linhas.