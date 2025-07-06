# Rafael PDITA394
Projeto acadêmico de banco de dados relacional em MySQL, com modelagem e criação das tabelas professor, aluno e disciplina, além da inserção de dados e exportação do dump .sql via MySQL Workbench.

# 📚 Banco de Dados - Faculdade

Este projeto consiste na criação de um banco de dados relacional chamado **Faculdade**, com as tabelas `professor`, `aluno` e `disciplina`. Foi utilizado o MySQL Workbench para modelagem, criação e inserção de dados, além da exportação (`dump`) para um arquivo `.sql`.

---

## 🛠️ Tecnologias Utilizadas

- MySQL 8.0+
- MySQL Workbench
- SQL padrão ANSI
- Git & GitHub

---

## 📦 Estrutura do Banco de Dados

### 🔹 Tabela `professor`
| Coluna         | Tipo         | Restrições                     |
|----------------|--------------|--------------------------------|
| id_professor   | INT          | PRIMARY KEY, AUTO_INCREMENT   |
| nome           | VARCHAR(100) | NOT NULL                      |
| email          | VARCHAR(100) | UNIQUE                        |
| data_admissao  | TIMESTAMP    | DEFAULT CURRENT_TIMESTAMP     |

---

### 🔹 Tabela `aluno`
| Coluna         | Tipo         | Restrições                     |
|----------------|--------------|--------------------------------|
| id_aluno       | INT          | PRIMARY KEY, AUTO_INCREMENT   |
| nome           | VARCHAR(100) | NOT NULL                      |
| curso          | VARCHAR(50)  |                                |
| data_matricula | TIMESTAMP    | DEFAULT CURRENT_TIMESTAMP     |

---

### 🔹 Tabela `disciplina`
| Coluna        | Tipo         | Restrições                                      |
|---------------|--------------|-------------------------------------------------|
| id_disciplina | INT          | PRIMARY KEY, AUTO_INCREMENT                    |
| nome          | VARCHAR(100) | NOT NULL                                       |
| carga_horaria | INT          | DEFAULT 60                                     |
| id_professor  | INT          | FOREIGN KEY → `professor(id_professor)`        |

---

## 📥 Como Executar

1. **Clone este repositório:**

```bash
git clone https://github.com/seu-usuario/faculdade-bd.git
cd faculdade-bd
