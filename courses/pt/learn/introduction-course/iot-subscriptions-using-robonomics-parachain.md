---
title: "Lição #5, Assinaturas IoT usando a Parachain Robonomics"
lastUpdate: Thu May 04 2023 12:57:02 GMT+0400 (Samara Standard Time)
description: Você aprenderá como comprar uma assinatura IoT na Parachain Robonomics usando tokens reais da nossa rede.
lessonNumber: 5
metaOptions: [Cursos on-line, Curso introdutório]
defaultName: Introduction to the ideas of Robonomics
---


A última lição de nosso curso introdutório é provavelmente a mais desafiadora porque exigirá de você alguma destreza e paciência. Você aprenderá como comprar uma assinatura IoT na Parachain Robonomics usando tokens reais da nossa rede.


## Intro

Uma assinatura IoT é uma chave de acesso a todas as funções relacionadas à mudança do estado do gêmeo digital de um sistema ciberfísico e ao armazenamento de informações sobre ele usando o ecossistema Polkadot / Kusama. Possuir uma assinatura evita o usuário da necessidade de pagar uma taxa pela transação. Em vez disso, o usuário pode enviar uma transação gratuita uma vez em um período de tempo determinado .

A principal maneira de comprar uma assinatura é participar do leilão de assinatura e, portanto, nesta lição, você deve obter tokens XRT para fazer ofertas e submeter transações. Mais informações sobre este processo também estão disponíveis em [nosso wiki](https://wiki.robonomics.network/docs/get-subscription).


## Instruções

<List type="numbers">

<li>

You need around 2 XRT Robonomics Parachain tokens ([sobre tokens](https://robonomics.network/xrt/)). Se você não tiver, você tem várias opções para obtê-los:

a) If you pass both tests after Lesson 2 and Lesson 4 with 90% correct answers, you can request free tokens for the lesson. Check your scores on [the special checking dapp](https://lk.robonomics.academy/). Specifically, you need to score 15 out of 17 for Lesson 2 and 10 out of 11 for Lesson 4, and you have two attempts to do this. To get tokens, contact the Academy Administrator on our [Discord](https://discord.gg/xqDgG3EGm9) (IBerman#5862).

b) Buy XRT tokens on one of the exchanges (check out the [list of exchanges](https://www.coingecko.com/en/coins/robonomics-network#markets/)). Tenha cuidado se você não estiver familiarizado com corretoras de criptomoedas, lembre-se de que todas as compras em corretoras de criptomoedas podem ter riscos potenciais, compre apenas a quantidade necessária de tokens para passar nesta lição. Also, keep in mind that Robonomics exists on two networks, Ethereum and Kusama, so each network has its own XRT token. You need a token that used by parachain in Kusama network.

c) If you have XRT token in Ethereum network (ERC-20 format), use [Exodus](https://old.dapp.robonomics.network/#/exodus) process to transfer tokens from the Ethereum network to Kusama. Keep in mind that the transfer of tokens is carried out once a week.

</li>

<li>

As assinaturas IoT são compradas através de um processo de leilão regular com o maior lance obtendo uma assinatura. 

Antes de tentar participar do leilão, você deve verificar se há algum disponível. Abra o portal Robonomics [Polkadot/Substrate](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Fkusama.rpc.robonomics.network%2F#/chainstate) no menu Chain state. Selecione <code>rws</code> consulta com <code>auctionQueue()</code> e pressione o botão ´+´. Você deve ver os IDs dos leilões disponíveis; lembre-se do Id de um deles. Se nenhum leilão for exibido ou estiver disponível, por favor, entre em contato conosco em nosso Discord in "[🎓robonomics-academy](https://discord.com/channels/803947358492557312/803947358492557315)" channel.

Agora, no mesmo menu Chain state, selecione <code>rws</code> com <code>auction(u32): Option&lt;PalletRobonomicsRwsAuctionLedger&gt;</code> e no campo <code>u32</code> digite o ID do leilão lembrado. Após pressionar o botão '+', você verá informações sobre o leilão de interesse. Se o campo <code>winner</code> tem valor <code>null</code> então ninguém tem esta assinatura e você pode tentar consegui-la.

</li>

<li>

Faça uma oferta com seus tokens XRT.

Vá para o menu Developer -> Extrinsic e para a mesma conta polkadot.js que você usou na lição anterior, escolha extrinsic <code>rws</code> com <code>bid(index, amount)</code>. No campo <code>index</code> entrar com o ID do leilão de interesse. No campo <code>amount</code> você deve inserir o seu número de tokens para o lance, convertido para os “wieners” (1 XRT = 1 000 000 000 Wn). Check the current minimum subscription price in our [dapp](https://dapp.robonomics.network/#/subscription). 

Envie a transação e, se você tiver sorte, receberá a assinatura IoT. Você pode verificar se seu endereço Polkadot é dono da assinatura através do menu Chain state.

</li>

<li>

O último passo é adicionar dispositivos para sua assinatura IoT. 

Isto significa que você atribui à sua assinatura endereços Polkadot adicionais que você ou seus dispositivos podem usar para executar extrínsecos (por exemplo, para lançar dispositivos ou enviar dados do dispositivo para a blockchain). 

Antes de começar, crie uma nova conta na Parachain Robonomics (guia em [nosso wiki](https://wiki.robonomics.network/docs/create-account-in-dapp/)), e chame-a de 'dispositivo inteligente' por conveniência.

Depois, vá para o menu Developer -> Extrinsic, e selecione <code>rws</code> com <code>setDevices()</code>. Na lista de dispositivos use o botão `Add item` para adicionar dispositivos e selecione a conta recentemente criada para dispositivos inteligentes. Depois disso, envie a transação.

O endereço do dispositivo deve ser adicionado à assinatura. Você pode verificá-lo no menu Chain state consultando <code>rws</code> com <code>devices()</code> para sua conta polkadot.js que possui a assinatura..

</li>

</List>

<Result>

A lição será considerada concluída após uma transação bem sucedida de compra de uma assinatura IoT e a adição de um dispositivo nela.

You can check your results on [the special checking dapp](https://lk.robonomics.academy/). For authorization on the checking dapp use the same account in Polkadot.js that was used during the course.

</Result>