# Roteiro em áudio: Como a IA mudou o trabalho do N3

Duração-alvo: cerca de 14 minutos. Um bloco por slide, na ordem do deck (20 slides). Voz: Piper, Cadu.

Público: equipe LBC, que já conhece a rotina do suporte e do desenvolvimento. Por isso o roteiro não explica o que é N2, N3, ticket ou versão; vai direto ao que mudou.

Marcações para a gravação: [pausa] é uma pausa curta, [pausa longa] uma pausa maior, e o texto entre asteriscos é falado com ênfase.

## 01 · Capa

Bom dia, pessoal! [pausa] Que bom ver todo mundo aqui.

Vocês conhecem a nossa rotina tão bem quanto eu. Então eu vou direto ao ponto. [pausa] Hoje eu quero mostrar o que mudou no N3 desde que a inteligência artificial entrou de verdade no nosso dia a dia.

E eu falo em nome de um time incrível: o Felipe, o Flaubert, o Wesley, o Danilson e eu, Rafael. [pausa] Vamos lá!

## 02 · Setembro a novembro, em três números

Começo pelo resultado. [pausa]

Desde o fim de setembro, o N3 entrega *sessenta por cento mais* tickets por semana.

O N2 recebia a solução em oito dias e meio. Hoje recebe em *menos de dois dias*.

E só em outubro, *trinta e cinco* correções nossas entraram em versão. A média era quinze. [pausa longa]

Guardem esses três números. Daqui a pouco vocês vão ver de onde cada um veio.

## 03 · Até agosto, cada chamado começava do zero

Todo mundo aqui já viveu isso. [pausa]

O chamado chegava, a gente abria aquele código antigo, sem documentação, e investigava do zero. Corrigia, liberava, e pronto.

E o que a gente aprendia? [pausa] Ficava na cabeça de quem fez. No próximo chamado parecido, *começava tudo de novo*.

O preço disso? *Oito dias e meio* para o ticket voltar ao N2 com solução.

## 04 · Desde setembro, o que aprendemos fica registrado

Em setembro, a gente mudou. [pausa] A IA passou a trabalhar *junto com* o analista, em quatro passos.

Ela faz o levantamento antes de abrir o código. Lê o que a gente já sabe daquele assunto. Ajuda na correção, com revisão e teste. E no fim, [pausa] *registra o que aprendemos*.

Assim, o próximo chamado do mesmo assunto já começa sabendo. [pausa] E fica claro: quem decide, e quem responde pelo ticket, *continua sendo a gente*.

## 05 · A documentação cresceu toda semana

Olhem essa curva. [pausa] É o nosso conhecimento crescendo, semana a semana.

*Cento e setenta e três* contribuições em oito semanas. E ela acelera, porque cada documento novo deixa o próximo mais fácil.

Hoje são cinquenta e cinco assuntos do sistema documentados, com a ajuda de onze pessoas.

## 06 · As skills que o N3 criou e as que adotou

E boa parte desse conhecimento virou skill. [pausa]

O N3 criou o fluxo inteiro do chamado: análise, consulta, code review, testes e encerramento. Criou as skills de casos de teste, de papel timbrado e de resumo técnico, para a evidência sair pronta para o N2 e para o cliente. E documentou assuntos do sistema, como cadastro de clientes, contas a pagar, faturamento, reforma tributária, RFID e LBCOleo.

E a gente não começou do zero. [pausa] Integramos skills prontas de outros times: a do Delphi 3, a de commit, a de liberação, o robô de testes, a de otimização segura e a do CNPJ alfanumérico.

Das cinquenta e cinco skills da LBC, *vinte e sete* têm a mão do N3.

## 07 · Em outubro, 35 tickets do N3 entraram em versão

Agora os números. E esse vem direto do histórico do código. [pausa]

De março a agosto, a gente liberava entre doze e vinte e uma correções por mês. Em outubro? [pausa] *Trinta e cinco*.

E novembro só parece menor porque tem muita coisa pronta, esperando liberação.

## 08 · Todas as semanas desde 21 de setembro bateram a meta

Esse é o gráfico de que eu mais me orgulho. [pausa]

Antes, a média era de dezessete tickets por semana, e a meta era batida em dezenove de trinta semanas.

Desde vinte e um de setembro? Média de vinte e oito. Meta batida em *nove de nove semanas*. [pausa longa]

E a meta subiu duas vezes nesse período: de quinze para dezoito, e depois para vinte. [pausa] *E a gente continuou batendo*.

## 09 · Outubro foi o mês com mais tickets no N3: 141

Agora olhando o ano inteiro, pelas nossas planilhas mensais. [pausa]

De janeiro a agosto, a média foi de setenta e quatro tickets por mês. De setembro a novembro, *cento e nove*.

E outubro foi o recorde do ano: *cento e quarenta e um* tickets.

Desde outubro, a planilha marca quais tickets foram feitos com IA. [pausa] Foram *setenta e sete por cento*.

## 10 · Bugs antigos passaram a ser corrigidos: de 5 para 17 por mês

E aqui está, para mim, a mudança mais importante. [pausa]

O bug legado, aquele problema antigo que a gente acabava contornando com orientação, passou de cinco para *dezessete* por mês. As melhorias em versão mais que dobraram.

O BDFix de intervenção, que já está documentado, caiu de dezenove horas para *cinco horas e meia*.

E eu quero ser transparente: [pausa] a mediana geral do desenvolvimento à solução subiu, de trinta e nove para setenta e quatro horas. Por quê? Porque a gente passou a *corrigir de verdade*, em versão. E isso leva mais tempo do que uma orientação. [pausa] A gente trocou o contorno rápido pela correção que *não volta*.

## 11 · As redes com mais chamados

E como isso aparece nas redes que mais chamam a gente? [pausa]

A Rede Praia é o melhor exemplo. Foi de dois para oito tickets por mês, e mesmo assim o tempo caiu *pela metade*.

A Revenda JF e a Walsoft também ganharam volume e ficaram mais rápidas.

Na Araújo e Lamboglia e na Pioneiro, o tempo subiu. Porque os casos viraram correção em versão, que espera liberação. [pausa] O ganho delas é o problema *não voltar*.

## 12 · O N2 recebe a solução em menos de 2 dias

Agora, aquele número do começo. [pausa]

Na amostra do Movidesk, o tempo entre o envio ao N3 e a solução caiu de oito dias e meio para *um vírgula nove dia*.

E mais pedidos do N2 viraram correção no sistema: de sessenta e cinco para setenta e sete por cento.

É uma medida diferente da planilha, e com uma amostra pequena, de cinquenta e dois tickets. Por isso um dos nossos próximos passos é medir tudo, ticket a ticket.

## 13 · A Apuração de Ponto abria em 1 minuto e 50. Agora abre em 14 segundos

Uma história rápida. [pausa]

A Apuração de Ponto demorava quase *dois minutos* para abrir. A IA leu a rotina com a gente, achou duas consultas desnecessárias, e a gente tirou só essas duas, conferindo que o resultado não mudava.

A tela passou a abrir em... [pausa] *catorze segundos*.

## 14 · Com a Base de Conhecimento, o N2 acha a resposta sozinho

E esse conhecimento chegou ao N2. [pausa] Junto com o nosso querido Suporte N2, a gente criou a Base de Conhecimento.

São *quinhentos e trinta e seis* artigos. Digitou boleto? [pausa] Trinta respostas na hora, inclusive a remessa do Santander.

Menos pergunta no chat, menos ticket subindo, e o cliente com resposta *no primeiro contato*.

## 15 · 21 tickets saíram com documento de teste

A documentação de testes também deu um salto. [pausa]

*Vinte e um* tickets saíram com documento completo, somando *cento e setenta e três* casos de teste, sempre no mesmo formato.

## 16 · O robô executa o teste e grava em vídeo

E agora temos um robô de testes! [pausa]

Ele abre o sistema numa base de teste, segue os passos, confere o resultado e grava um vídeo com legenda. Sem nunca encostar em produção.

Já são vinte e quatro vídeos. E esses testes podem rodar de novo a cada versão, para garantir que *nada volte a quebrar*.

## 17 · O que chegou aos postos

No fim do dia, o que importa é o cliente. [pausa]

Na Rede Liber, as sangrias voltaram a importar sem divergência. Na Mil Carvalho, o Pix da Stone entra no turno certo. A contabilidade parou de receber lançamentos em dobro. Quem usa Boa Vista ganhou as bandeiras novas conciliando. E os clientes da nuvem voltaram a mandar fatura por e-mail de qualquer navegador.

Caixas que fecham. Cartões que conciliam. [pausa] *Clientes mais tranquilos*.

## 18 · Quem fez

E nada disso aconteceu sozinho. [pausa]

O Felipe, com a conciliação de cartões, o Pix e o Sintegra. O Flaubert, com a nota fiscal, o perfil de acesso e a nuvem. O Wesley, com o ponto eletrônico, o CT-e e a reforma tributária. O Danilson, com as liberações de versão e o cadastro de clientes.

E um obrigado muito especial ao Suporte N2, que escreveu a maior parte da Base.

Gente, [pausa] *vocês fizeram isso acontecer*.

## 19 · Próximos passos, a partir de dezembro

E agora? [pausa]

Primeiro: preencher o responsável e o tipo de correção em todo ticket, para medir o tempo de resposta todo mês.

Segundo: junto com o N2, medir quantos tickets a Base de Conhecimento evitou.

Terceiro: levar o robô de testes para os tickets de caixa e fiscal.

O objetivo é melhorar ainda mais os processos do N3, deixar o retorno ao N2 mais rápido e claro e, com o tempo que sobra, *abrir espaço para novos projetos*. [pausa] Isso não é só do N3. *É de toda a LBC*.

## 20 · Encerramento

Se eu tivesse que resumir tudo em uma frase: [pausa]

*Cada chamado que a gente resolve hoje deixa o próximo mais fácil.* [pausa longa]

O N3 não ficou mais rápido porque digita mais rápido. [pausa] Ficou mais rápido porque *parou de esquecer*.

Muito obrigado, pessoal! [pausa] Agora eu quero ouvir vocês.
