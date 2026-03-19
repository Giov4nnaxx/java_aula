# 🎓 Gestão Acadêmica

Sistema de gerenciamento acadêmico desenvolvido em Java (console), com foco em controle de alunos e turmas, aplicando boas práticas de programação e organização de código.

---

## 📌 Funcionalidades

### 👩‍🎓 Alunos

* Cadastro de alunos
* Listagem de alunos por turma
* Edição de dados do aluno
* Desativação de alunos
* Validação de idade (mínimo 14 e máximo 130 anos)
* Validação de data de nascimento

### 🏫 Turmas

* Cadastro de turmas
* Listagem de turmas
* Edição de turmas
* Desativação de turmas
* Regra de integridade:

  * Não permite desativar turma com alunos ativos sem confirmação
  * Opção de desativar todos os alunos da turma automaticamente

---

## 🧠 Regras de Negócio

* Apenas alunos **ativos** são considerados nas operações
* Não é possível cadastrar aluno:

  * Com idade menor que 14 anos
  * Com idade maior que 130 anos
* Não é permitido manter alunos ativos em turmas inativas
* Exclusão lógica (soft delete) utilizando atributo `ativo`

---

## 🛠️ Tecnologias Utilizadas

* Java
* Programação Orientada a Objetos (POO)
* Java Time API (`LocalDate`, `Period`)
* Estruturas de dados (`ArrayList`)
* Stream API (filtros e validações)

---

## 🧱 Estrutura do Projeto

```
📁 src
 ┣ 📄 Main.java            → Controle do menu e fluxo do sistema
 ┣ 📄 Aluno.java           → Entidade Aluno
 ┣ 📄 Turma.java           → Entidade Turma
 ┣ 📄 AlunoService.java    → Regras e operações de alunos
 ┣ 📄 TurmaService.java    → Regras e operações de turmas
```

---

## 🔄 Organização do Código

O sistema segue o princípio de **separação de responsabilidades (SRP)**:

* `Main`: responsável apenas pela interação com o usuário
* `AlunoService`: contém toda a lógica relacionada aos alunos
* `TurmaService`: contém toda a lógica relacionada às turmas

---

## ⚙️ Conceitos Aplicados

* Encapsulamento
* Separação de responsabilidades
* Regras de negócio
* Validação de dados
* Uso de lambdas e Stream API
* Soft delete (desativação em vez de remoção)

---

## 💡 Melhorias Implementadas

* Filtro de alunos por turma
* Verificação de alunos ativos antes de desativar turma
* Uso de `anyMatch` para validações
* Uso de `forEach` para operações em lote
* Validação de idade com `Period`
* Código mais limpo com métodos reutilizáveis

---

## 🚀 Possíveis Evoluções

* Interface gráfica (JavaFX ou Swing)
* Persistência em banco de dados
* API REST (Spring Boot)
* Sistema de login
* Relatórios acadêmicos

---

## 📚 Objetivo do Projeto

Este projeto foi desenvolvido com fins educacionais para prática de:

* Lógica de programação
* Estruturação de sistemas
* Boas práticas em Java
* Simulação de regras reais de negócio

---

## 👩‍💻 Autora

Desenvolvido por **Giovanna Santana**
