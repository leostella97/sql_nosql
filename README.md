# Bancos de Dados Relacionais (SQL) e Não Relacionais (NoSQL)
## Este documento contém uma explicação sobre o papel dos <b>bancos de dados SQL (relacionais)</b> e <b>NoSQL (não relacionais)</b>, seus conceitos e como eles se aplicam.

## 1. O que é *SQL (Structured Query Language)*
### Definição:
*SQL (Structured Query Language)* é uma linguagem usada para consultar e manipular bancos de dados relacionais. Os bancos de dados relacionais armazenam dados em tabelas que se relacionam entre si por meio de _chaves (primárias e estrangeiras)_.
*Principais Características:*
- *Estrutura fixa (Esquema rígido):* Os dados são organizados em tabelas com colunas e tipos de dados predefinidos. Isso impõe um esquema rígido, o que significa que todos os registros (linhas) devem seguir esse modelo.
- *Consultas poderosas:* Usando a linguagem SQL, é possível fazer consultas complexas, combinar dados de várias tabelas com JOINs, agrupar e filtrar resultados.
- *Transações: Suporta transações _ACID (Atomicidade, Consistência, Isolamento e Durabilidade)_*, garantindo segurança em operações de escrita e leitura.

Exemplos de *Bancos de Dados Relacionais (SQL)*:
<br>
• MySQL
<br>
• PostgreSQL
<br>
• Oracle Database
<br>
• SQL Server
<br>
• SQLite
<br>
• PHPMyAdmin (SQL com interface gráfica)

### Exemplo de consulta SQL:
<code>SELECT nome, idade
FROM usuarios
WHERE idade > 18
ORDER BY nome ASC;
</code>

Neste exemplo, estamos *consultando* a tabela <code>usuarios</code> e retornando as colunas <code>nome</code> e <code>idade</code> para os usuários com mais de 18 anos, ordenados ordenado pelo nome.

### Quando Usar SQL:
• Quando os dados têm uma estrutura fixa e bem definida.
<br>
• Quando você precisa de transações complexas e garantias ACID.
<br>
• Quando as relações entre dados (chaves estrangeiras) são importantes, como em sistemas de bancos, e-commerce, etc.


## 2. O que é NoSQL (Not Only SQL)?
### Definição:
NoSQL se refere a uma classe de sistemas de banco de dados que _não seguem o modelo de tabelas relacionais_. Os bancos NoSQL podem usar _diferentes modelos de dados, como documentos, colunas, grafos e chave-valor_.

### Principais Características:
- *Flexibilidade de esquema:* Bancos NoSQL geralmente _não possuem um esquema fixo_. Isso significa que diferentes registros podem ter *diferentes campos e formatos*.
- *Escalabilidade horizontal:* NoSQL é projetado para ser _facilmente escalável horizontalmente_, distribuindo dados em múltiplos servidores.
- *Desempenho em grandes volumes de dados:* Geralmente, os bancos NoSQL têm _melhor desempenho_ em grandes volumes de dados e em sistemas de alta disponibilidade.
- *Capacidade de armazenar dados semi-estruturados ou não estruturados:* Como arquivos _JSON, XML, dados de redes sociais_, etc.

## Tipos de Bancos de Dados NoSQL:
- *Bancos de Dados de Documentos:* Armazenam dados como documentos JSON ou BSON.
    Exemplos: MongoDB, CouchDB
- *Bancos de Dados de Chave-Valor:* Armazenam pares de chave e valor.
    Exemplos: Redis, DynamoDB
- *Bancos de Dados de Colunas:* Organizam dados por colunas em vez de linhas.
    Exemplos: Cassandra, HBase
- *Bancos de Dados de Grafos:* Modelam dados como grafos, com vértices e arestas.
    Exemplos: Neo4j, ArangoDB

### Exemplo de Inserção NoSQL (MongoDB):
<code>{
    "nome": "Leonardo Stella",
    "idade": 25,
    "email": "leonardo@lesttech.com.br",
    "telefone": "+55 (13) 90000-0000"
}
</code>