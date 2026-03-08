# Pascal Compiler

**Processamento de Linguagens e Compiladores** · Licenciatura em Ciências da Computação · Universidade do Minho · 2025/2026

---

## Descrição

Compilador para um subconjunto da linguagem Pascal Standard, desenvolvido no âmbito da unidade curricular de Processamento de Linguagens e Compiladores. O sistema traduz código-fonte Pascal para instruções de uma máquina virtual baseada em pilha, implementando todas as fases essenciais de compilação.

## Estrutura do Projeto

```
src/
├── lexer.py        # Analisador léxico (tokenização via PLY)
├── parser.py       # Analisador sintático (construção da AST via PLY)
├── ast.py          # Definição dos nós da árvore sintática abstrata
├── sema.py         # Analisador semântico e tabela de símbolos
├── codegen_vm.py   # Gerador de código assembly para a VM
└── main.py         # Interface de linha de comandos
```

## Funcionalidades

- Tipos de dados: `integer`, `real`, `boolean`, `string` e arrays unidimensionais
- Operações aritméticas, relacionais e lógicas
- Estruturas de controlo: `if-then-else`, `while-do`, `for-to/downto`, `repeat-until`
- Subprogramas: procedimentos e funções com parâmetros por valor
- Operações de entrada/saída: `readln` e `writeln`
- Função built-in `length` para strings
- Análise semântica com verificação de tipos e gestão de escopos
- Persistência da AST para depuração

## Pipeline de Compilação

```
Código Pascal → [Lexer] → Tokens → [Parser] → AST
              → [Analyzer] → AST verificada → [CodeGen] → Código VM
```

## Execução

```bash
pip install ply
python main.py <ficheiro.pas>
```

O compilador produz um ficheiro `.vm` com o código assembly gerado, pronto a executar na máquina virtual fornecida.

## Tecnologias

- Python 3.x
- PLY (Python Lex-Yacc) 3.11
- Máquina virtual baseada em pilha (fornecida)

## Autores

Miguel Silva — A109069  
Tiago Fernandes — A98983


