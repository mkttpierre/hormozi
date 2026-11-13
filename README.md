# Hormozi: um conselheiro de oferta, leads e dinheiro para o seu agente de IA

> Skill em português para Claude Code e Codex. Coloca o método do Alex Hormozi
> dentro do agente: oferta irrecusável, captação de leads e modelo de dinheiro,
> sempre aplicados aos números do **seu** negócio.

Você pergunta "como eu melhoro essa oferta?", "por que ninguém compra?" ou
"como faço o cliente pagar o anúncio nos primeiros 30 dias?". O agente acha o
gargalo, abre só o capítulo certo, faz a conta com os seus números e devolve a
jogada pronta, dizendo de qual livro ela saiu.

---

## De onde vem

A skill foi construída a partir da leitura dos três livros da série
*$100M* do Alex Hormozi:

| Livro | O que cobre | Arquivo |
|---|---|---|
| **$100M Offers** | Oferta irrecusável (*Grand Slam Offer*), equação de valor, preço premium, bônus, garantia, escassez, urgência, nome da oferta | `livros/offers.md` |
| **$100M Leads** | Lead magnet, os 4 núcleos de captação (contato quente, conteúdo, prospecção fria, anúncio), indicação, afiliados, agências, regra dos 100 | `livros/leads.md` |
| **$100M Money Models** | Caixa nos primeiros 30 dias, atração, upsell, downsell, continuidade (assinatura e recompra) | `livros/money-models.md` |

Os resumos são **notas de leitura escritas com palavras próprias**, organizadas
para o agente consultar, sem trechos copiados dos livros. Cada módulo termina
com uma seção "Lacunas do livro": o que o Hormozi não cobre, para o agente
assumir que não sabe em vez de inventar.

Não é material oficial e não tem ligação com o Alex Hormozi nem com a
Acquisition.com. Se a skill te ajudar, compre os livros: eles valem muito
mais que este resumo.

---

## Como funciona

A skill segue cinco passos, sempre na mesma ordem:

1. **Lê o seu negócio.** Se a pasta tem memória do negócio (`_memoria/` com
   empresa, preferências e estratégia), ela usa. Se não tem, trabalha com o que
   você contar. Antes de qualquer conselho, ela precisa saber o que você vende,
   para quem, por quanto e o que é proibido no seu setor.
2. **Acha o gargalo.** Abre o `indice-de-decisao.md` e classifica o problema
   em **oferta**, **leads** ou **dinheiro**, na ordem que o Hormozi usa. Se
   faltar dado que muda a resposta, faz até 5 perguntas do `questionario.md`,
   cada uma com uma recomendação. O resto ela supõe e te avisa o que supôs.
3. **Lê só o capítulo certo.** Nunca carrega os três livros inteiros. O índice
   diz qual arquivo e qual seção abrir. Isso economiza contexto e evita
   conselho genérico.
4. **Monta a resposta** sempre no mesmo formato:
   - **Diagnóstico:** o gargalo e o número que o prova.
   - **Jogada:** o que fazer, em passos, com o capítulo de origem.
   - **Conta:** valor, margem, CAC e caixa de 30 dias com os seus números.
   - **Texto pronto:** nome da oferta, mensagem ou roteiro de upsell, quando couber.
   - **Trava aplicada:** o que foi adaptado por causa da regra do seu setor.
   - **Teste:** uma métrica e um prazo para saber se funcionou.
5. **Revisa** a oferta final contra o `revisao.md` antes de entregar.

### As regras que ela não quebra

- **A regra do seu negócio vence o método.** Setor regulado (saúde,
  suplemento, finanças) não ganha promessa de resultado: a skill troca por uma
  garantia permitida e diz que trocou.
- **Escassez e urgência só se forem verdadeiras.** O próprio Hormozi proíbe a falsa.
- **Desconto é o último recurso.** Antes vêm bônus, mais unidades, parcelamento
  ou corte de recurso.
- **Uma peça por vez.** Ela recomenda o próximo passo do modelo de dinheiro, não
  as dezesseis jogadas de uma vez.
- **O que não está nos livros, ela diz que não sabe.** Direito, imposto e
  fechamento de venda em reunião são lacuna.

---

## O que tem na pasta

```
hormozi/
├── SKILL.md               # o roteiro que o agente segue
├── indice-de-decisao.md   # sintoma → arquivo e seção para abrir
├── questionario.md        # perguntas por ramo (oferta, leads, dinheiro)
├── revisao.md             # checklist final da oferta
└── livros/
    ├── offers.md          # $100M Offers
    ├── leads.md           # $100M Leads
    └── money-models.md    # $100M Money Models
```

---

## Como instalar

**Claude Code** (Mac ou Linux):

```bash
git clone https://github.com/mkttpierre/hormozi ~/.claude/skills/hormozi
```

**Claude Code** (Windows, PowerShell):

```powershell
git clone https://github.com/mkttpierre/hormozi "$env:USERPROFILE\.claude\skills\hormozi"
```

**Codex:** clone na pasta de skills do Codex (`~/.codex/skills/hormozi`).

Para valer só num projeto, clone dentro de `.claude/skills/` da pasta do
projeto. Reabra o agente depois de instalar.

## Como usar

Digite `/hormozi` ou peça do seu jeito. A skill entra sozinha quando o assunto é dela:

- "Monta uma oferta irrecusável para o meu serviço de R$ 1.500."
- "Meu anúncio não se paga. O que o Hormozi faria?"
- "Cria um upsell para quem acabou de comprar o plano básico."
- "Tenho 2.000 clientes antigos parados. Como reativo?"
- "Qual garantia eu consigo dar sem quebrar a empresa?"

Funciona melhor junto com a [`dotcom`](https://github.com/mkttpierre/dotcom),
que cuida do funil e do tráfego. A oferta sai daqui e o caminho do cliente sai de lá.

---

## Licença

MIT. Use, adapte e distribua à vontade. Os livros e o método são do Alex Hormozi.
