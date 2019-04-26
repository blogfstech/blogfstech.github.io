---
layout: post
title:  "Engenharia de confiabilidade de site (SRE)"
date:   2019-04-26 11:30:00 -0300
categories: post
author: Jonas Thomaz de Faria
---

## Engenharia de confiabilidade de site (SRE)


Tive contato com este termo a pouco mais de 1 mês, e honestamente estava meio perdido sobre o que ele realmente significa: Um framework? Boas práticas? Manual de Ciências da Computação for Dummies?
O objetivo aqui é apresentar SRE: o que é? como usar? E como se preparar para usar.
Basicamente aqui vou usar como referência o livro [Engenharia de Confiabilidade do Google da O'Reilly](https://www.google.com/search?q=Engenharia+de+Confiabilidade+do+Google&oq=Engenharia+de+Confiabilidade+do+Google&aqs=chrome..69i57j0l4.382j0j4&sourceid=chrome&ie=UTF-8) (facilmente acessado através da mesa do Carlão ou comprado na livraria/e commerce da sua preferência).

### O que é SRE?

De acordo com [Ben Treynor](https://www.linkedin.com/in/benjamin-treynor-sloss-207120/), fundador da Equipe de Confiabilidade de Site da Google, Engenharia de Confiabilidade de Sites (SRE é como vou escrever daqui pra frente, porque ,meu deus, é muita coisa) é **"o que acontece quando um engenheiro de software é encarregado do que costumamos chamar de operações"**. A idéia geral aqui é a de engenheiros de software se responsabilizem de forma multidisciplinar na gestão e automação do ambiente de tecnologia visando a criação de software escalável e confiável.

Certo, mas isso parece muito com DevOps não? Sim, SRE é basicamente uma implementação de DevOps com o objetivo específico de equilibrar a necessidade de se disponibilizar novas features do produto com a necessidade de se manter a operação estável. É muito fácil (e óbvio) identificar que falhas nos produtos estão diretamente ligadas a algum tipo de alteração no produto (Uma promoção nova, uma nova feature, comportamento de um novo grupo de usuários), gerando sempre um stress e desconfiança entre o time de desenvolvimento do produto e de operações.

E como resolver isso? A proposta é que a equipe se torne responsável pela disponibilidade, latência, desempenho, eficiência, gerenciamento de mudanças, monitoramento, resposta a emergências e planejamento de capacidade dos de um determinado serviço.


### O que eu preciso aprender e fazer para estar alinhado com o SRE?

SREs precisam ter uma compreensão de um todo dos sistemas e dos serviços que este sistema depende. O membro desta equipe deve gastar até 50% do seu tempo fazendo trabalhos relacionados a "operações" (isso pra gente na FS é bem simples, gastar 50% do tempo com chamados de sustentação), como resolução de problemas, etc. Como o sistema de software que um SRE supervisiona deve ser altamente automatizado e auto-recuperável, o SRE deve gastar os outros 50% de seu tempo em tarefas de desenvolvimento, como novos recursos, dimensionamento ou automação. 

Os engenheiros de confiabilidade devem tomar para si algumas linhas de raciocínio:

1. Operações são um problema de software: A qualidade da operação está ligado diretamente a qualidade do software. Fazer bem este processo depende do quão eficiente são as soluções utilizadas para resolver os problemas da operação. Um if a mais? um códigozinho chumbado? Pode resolver momentaneamente mas certamente a operação vai sofrer com isso em algum momento.

2. Prezar pelos SLOs: 100% de disponibilidade não é uma meta, é um sonho. No entanto a equipe deve ser capaz de definir a disponibilidade e caminhar para que ela seja atendida de maneira apropriada em conjunto com definições "realistas" da empresa.

3. Faça o máximo para fazer o mínimo: Trabalho repetitivo é cansativo (né não Marquinhos?). Se você pode tornar a manutenção/correção mais rápida e menos braçal faça.

4. Automatize o trabalho: A automação anda de mãos dadas com a redução do trabalho. Definir o que automatizar e sob que condições é uma decisão do time de SRE.

5. Agir rápido para reduzir o custo da falha: Quanto mais tarde você descobre um problema, mais difícil é corrigir. A monitoria do processo é fundamental para assegurar que tudo está ocorrendo bem. Procure no momento de executar sua atividade empregar a monitoria adequada para garantir que não seja pego de surpresa.

6. Compartilhar propriedade com os desenvolvedores: SRE visa reduzir os limites. As equipes de desenvolvimento (do código e de infra) do produto devem ter uma visão de toda a pilha - o frontend, o backend, as bibliotecas, o banco, a máquina física - e nenhuma equipe deve ser proprietária de componentes únicos. Isso não quer dizer que todos precisam ter acesso ao banco de produção como root, ou que o deploy em produção deva ser feito por qualquer pessoa a qualquer momento, mas sim que é necessário que todos tenham uma visão de que tudo funciona, como está operando e que possa verificar um determinado ponto da operação quando necessário.

7. Todos devem usar o mesmo Ferramental: Use o mesmo ferramental, independentemente da função. No SRE, você não pode ter equipes diferentes usando diferentes conjuntos de ferramentas. Quanto mais divergência você tem, menos a sua empresa se beneficia de cada esforço para melhorar cada ferramenta individual. 


### Como eu devo me preparar pro SRE?

A implementação do SRE requer planejamento e consenso.

Uma empresa que deseja implementar o SRE precisa estar preparada para customizar o SRE para seu negócio e definir como a adoção do SRE funcionará (definição de métricas, objetivos, etc). Esse processo exige envolvimento total da empresa. Uma vez que uma equipe de SRE está formada ela vai precisar de um grande suporte da gestão.

O modelo SRE de trabalho - e todos os benefícios que vêm com ele - depende de equipes com ampla capacidade de trabalho. Se o trabalho excede essa capacidade, o modelo SRE não pode ser lançado ou mantido. Um membro que quer enfiar o SRE garganta abaixo da equipe é apenas um sysadmin chato.

A adoção de SRE não pode ser apenas por modinha. Precisa de compromisso e acompanhamento para ter sucesso.