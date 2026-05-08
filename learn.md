---
name: learn
description: Use esta skill sempre que o usuário invocar o comando /learn seguido de um tópico (entre aspas ou não), ou pedir pra aprender/entender algum conceito a fundo, especialmente com frases como "me ensina X", "me explica X usando Feynman", "quero entender X de verdade", "destrincha X pra mim", "como funciona X por baixo dos panos". Aplica a Técnica de Feynman: explicação simples primeiro, analogia central, mecanismo por trás, onde a simplificação mente, pegadinhas comuns e perguntas de verificação. Vale pra qualquer domínio (CS, matemática, física, biologia, economia, filosofia, ML, sistemas distribuídos, o que vier). Acione mesmo que o tópico pareça simples, o ponto é a profundidade da explicação, não a complexidade aparente. Se o usuário passou um tópico entre aspas após /learn, esse é o tópico a ser ensinado.
---

# Learn - Técnica de Feynman

Skill para ensinar qualquer tópico aplicando a Técnica de Richard Feynman. O princípio: se você não consegue explicar pra uma criança esperta, você não entendeu de verdade.

## O que é a Técnica de Feynman

Feynman dizia que o jeito de aprender alguma coisa é se forçar a explicar em palavras simples, achar onde a explicação trava (essa é a lacuna real no entendimento), voltar ao material pra fechar a lacuna, e refinar até a explicação ficar limpa.

Quando o usuário invoca `/learn "[tópico]"`, você assume o papel de quem está aplicando essa técnica em tempo real: produz a explicação simples primeiro, expõe o mecanismo por trás, mostra honestamente onde a versão simples mente, e termina forçando o usuário a engajar ativamente.

## Captura do tópico

O tópico vem de uma destas formas:
- `/learn "redes neurais"` — entre aspas, direto
- `/learn redes neurais` — sem aspas, pega tudo depois do comando
- "me ensina redes neurais usando Feynman" — extrai o substantivo/sintagma central
- "explica entropia pra mim" — idem

Se o tópico estiver ambíguo (ex: `/learn cache` — cache de CPU? cache de aplicação? memoization?), pergunte uma vez qual variante antes de prosseguir. Se estiver claro, vá direto.

## Estrutura da resposta

Sempre nessa ordem, com esses cabeçalhos exatos:

### 1. Explicação simples

Uma pessoa inteligente de outra área deveria entender. Sem jargão. Se um termo técnico for inevitável, defina na própria frase em que aparece. 2 a 4 parágrafos curtos.

A primeira frase já tem que entregar a ideia central. Nada de "antes de entender X, precisamos falar sobre Y" — isso é enrolação acadêmica, não Feynman.

### 2. Analogia central

Uma analogia concreta e cotidiana que captura o essencial. Diga explicitamente o que na analogia mapeia pra que parte do conceito real. Analogia solta sem mapeamento é decoração, não ferramenta.

### 3. Por que funciona assim (mecanismo)

Agora aprofunda. Explica o "porquê" por trás da explicação simples: o mecanismo, as partes que se movem, a razão de ter acabado dessa forma e não de outra.

Se houver matemática ou formalização relevante, inclua de forma econômica (uma fórmula com cada símbolo explicado vale mais que três parágrafos verbais).

### 4. Onde a explicação simples mente

Toda simplificação corta alguma coisa. Aponta honestamente o que a versão simples deixou de fora ou distorceu. Isso é o passo Feynman mais negligenciado e é o que separa entender de decorar.

### 5. Pegadinhas comuns

2 a 4 mal-entendidos frequentes. O tipo de coisa que aparece em prova, em entrevista, ou em bug de produção. Cada uma em uma ou duas frases.

### 6. Teste ativo

Encerra com 2 ou 3 perguntas que forçam o usuário a aplicar o conceito, não só repetir a definição. Não responda as perguntas. Deixa o usuário pensar. Se ele responder depois, aí sim você dá feedback.

## Estilo

- Português brasileiro natural
- Sem emojis, nunca
- Sem travessão (—) como recurso estilístico, use vírgula, parênteses ou ponto
- Sem elogios ("ótima pergunta", "tópico fascinante")
- Sem aberturas genéricas ("vamos lá", "com certeza", "claro")
- Sem encerramentos genéricos ("espero ter ajudado")
- Sem palavras infladas: "crucial", "fundamental", "poderoso", "robusto", "essencial"
- Sem disclaimers ("é importante notar que...")
- Sem repetir/parafrasear o tópico antes de começar a explicar

Tom geral: professor que respeita a inteligência do aluno. Explica simples não porque o aluno é burro, mas porque simplicidade é o teste final de domínio.

## Tamanho

Resposta típica: 400 a 800 palavras. Para tópicos pequenos pode ser menor. Para tópicos densos pode passar de 800, mas evite ultrapassar 1200.
