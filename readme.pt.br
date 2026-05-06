# claude-skill-learn

> **Ensina qualquer tópico ao Claude Code usando a Técnica de Feynman.** Um slash command. Qualquer domínio.

[🇺🇸 Read in English](./README.md)

---

## Índice

1. [O que é isso](#o-que-é-isso)
2. [Uso](#uso)
3. [Estrutura da resposta](#estrutura-da-resposta)
4. [Instalação](#instalação)
5. [Contribuindo](#contribuindo)

---

## O que é isso

Uma skill customizada para o Claude Code que aplica a Técnica de Feynman em qualquer tópico que você queira aprender.

A ideia do Feynman: se você não consegue explicar pra uma pessoa inteligente de outra área, você não entendeu de verdade. A skill força esse processo: explicação simples primeiro, analogia concreta com mapeamento explícito, mecanismo por trás, onde a versão simples mente, pegadinhas comuns, e perguntas que forçam você a aplicar o conceito.

---

## Uso

```
/learn "transformers"
/learn garbage collector
/learn como funciona um índice de banco de dados
```

Funciona pra qualquer domínio: CS, matemática, física, ML, economia, filosofia, sistemas distribuídos.

---

## Estrutura da resposta

1. **Explicação simples** — sem jargão, a ideia central em linguagem clara
2. **Analogia central** — concreta e cotidiana, com mapeamento explícito pro conceito
3. **Como funciona de verdade** — o mecanismo, o "porquê" por trás da versão simples
4. **Onde a versão simples mente** — o que a simplificação cortou ou distorceu
5. **Pegadinhas comuns** — mal-entendidos que aparecem em provas, entrevistas ou bugs de produção
6. **Teste ativo** — 2 a 3 perguntas que exigem aplicar o conceito, não só repetir

---

## Instalação

**Opção A: nível de projeto (só neste projeto)**

```bash
mkdir -p .claude/commands
cp learn.md .claude/commands/learn.md
```

**Opção B: global (disponível em qualquer projeto)**

```bash
mkdir -p ~/.claude/commands
cp learn.md ~/.claude/commands/learn.md
```

Depois invoca dentro do Claude Code:

```
/learn "seu tópico aqui"
```

---

## Estrutura

```
claude-skill-learn/
├── learn.md       # O arquivo da skill
└── README.md
```
