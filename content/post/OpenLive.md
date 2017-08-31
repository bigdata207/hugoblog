---
title: "Openlive： Blockchain + Live"
date: 2017-08-30
categories:
- Storage
author: "Chet Zhang and Tao Zhong"
tags:
- hexo theme
- responsive
- gravatar
- disqus
- google analytics
keywords:
- disqus
- google
- gravatar
autoThumbnailImage: false
thumbnailImagePosition: "top"
thumbnailImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city-750.jpg
coverImage: //d1u9biwaxjngwg.cloudfront.net/welcome-to-tranquilpeak/city.jpg
metaAlignment: center
---


直播行业最近火的一塌糊涂，也渐渐进入平稳期，我们采用最新的区块链技术，渴求直播行业的进一步突破。
<!--more-->

背景：

据相关数据显示，2016年中国在线直播市场用户规模达到3.1亿人，增长率为60.6%。

![1](https://gateway.ipfs.io/ipfs/QmeBUexKn6x5GaJkHJVSa9HX13sqGEK7ActMuR5ZL4ESnu/1.jpg)

数据来源：艾媒咨询、中商产业研究院整理

直播市场用户巨大。

随着在线直播行业的逐渐成熟，网络直播法规收紧，监管力度加强，在线直播行业的门槛也相对有所提高。直播内容受限制太过严重，没有互联网自由精神的体现。其次，直播平台与主播的利益分配极度不均匀，大部分平台的主播只能拿到礼物的50%的收入，甚至更低，不符合观众打赏主播的初衷。
为了解决这些问题，一个全新的可替代的方式就是去中心化，利用P2P的思想来革新整个直播行业，让直播内容更自由，利益分配更均衡。OpenLive通过实现以下功能，使得上述内容更现实：

1.	使用加密货币BTC鼓励各方的参与

2.	使用BTC进行打赏

3.	允许使用昵称进行与主播的互动

4.	鼓励用户成为直播环境的维护者，以手续费的提成为奖励

项目概述：
整个直播平台的使用者分为两种，第一种为主播，第二种为观众。每一位用户都是一个节点，可以进行节点之间的信息传递。观众可以为喜欢的主播送出礼物，礼物的支付方式是BTC，主播收到礼物时，钱包会自动增加余额，观众的钱包余额数据也会更新。
受信任的群组Trusted Group（参考了MaidSafe的原理）

在Live网络内，可以假定邻近的节点群组是可以信任的。虽然围绕特定目标在一个邻近群组内建立占多数的恶意节点群并非不可能，但这一点应该被视为在计算上是不可行的。

在Live网络内，通过以下规则来确定群组是受信任的：

1.	获取某一节点的特定地址是很困难的。（新节点的地址是网络使用节点证书哈希运算后定义的）除此之外，节点每一次离线后再次加入网络时，都会被分配到一个新地址上。此外，在验证期结束之前，该节点不会成为一个全功能节点。

2.	当一个群组发出一个指令时，所有群组成员都必须签名。而接收到指令的节点，在路由层上将执行寻找最接近节点的验证过程，用于验证发送指令者确实是离目标（数据）最近的。还有，网络将提供节点的公钥下载，以便验证签名。

3.	邻近群组并非一成不变(即仅依Kademlia协议定义的XOR距离）。只有当目标数据进入网络时，才会形成邻近群组。除非预先知晓目标数据，否则无法确定哪两个节点是相邻的。

举报机制：

由于法律上的一些固定，在自由直播同时，我们也反对黄赌毒等违法直播行为，所以有专门的举报机制进行处理。当某个节点发现了非法直播的行为之后，可以立刻进行举报，将信息发送给附近的受信任的群组，受信任的群组负责审核，达到半数以上的同意即认为该节点坏掉了，把该节点从网络中去除，其节点内部的余额也将损失掉（最好可以将该节点的余额奖励给举报者和受信任的群组）。
暂时定每一组节点为13个，当半数以上的节点（至少7个）认为某节点有不良行为的时候，该节点就会被认为是坏掉的节点，该行为被成为举报成功。

一旦举报成功，则被举报节点的收益会被管理者没收，其中诚实的节点平分这些收益，不诚实的节点被剔除，重新找出新的管理节点。

交易延迟确认问题（未解决）

由于BTC的属性问题，每一笔订单的确认都需要1个小时的时间，但直播环境这个以用户心情好坏决定收益的平台，不可能等待1个小时的充值时间。

所以双方的交易仍然是实时的，只是打赏的礼物的显示仍要在一个小时之后才会显示。

简而言之，主播可以实时的知道有谁送给了她礼物，然而其他的观众则需要在一个小时之后才知道谁送给了她礼物。如果主播对送给了她礼物的观众已经很熟悉，确定他并不会进行双重交易，也可以直接通过沟通的方式来让其他的观众知道，“感谢XXX的礼物”，仍然在一个小时候之后产生特效。

第二种解决方案
---

我们可以设计一种新的币种，该币种的确认时间非常快，甚至可以直接选用其他更为优秀的币种。在这里以太坊也是被考虑在其中的

竞争优势
---

参与度高

    由于采用的是区块链的模式，所以人人都可以参与到网络中来

匿名性强

    在这个网络平台上，你可以直播任何不违反法律的内容，而不用担心自己被暴露出来

角色多样性

    在这里，你不仅可以选择成为一名观众，你还可以去当主播，甚至成为一名管理员，用以获取收益

收益高

    以为没有第三方机构的监管，所以所有的交易只需要支付部分手续费即可，收益模式完全是多劳多得的形式，没有娱乐圈里面乱七八糟的事情

待解决的问题
--

弹幕的文明程度问题

    因为缺少第三方机构的监管与进入网络的门槛之低，弹幕的文明程度与质量必定参差不齐，网络熟语更易流传，弹幕戾气可能会过重，但是一般的直播平台也存在这个问题，并不是由于区块链+直播而单纯产生的这个问题

违法内容直播

    即时我们有了很完善的举报机制，但仍然可能存在漏网之鱼，没有被举报与发现，但我们相信这类现象在市场机制的作用下，可能性并不高，只要给了足够的激励机制就可以让这个举报机制很好的运行下去。

总的来说，此种营业模式更多的是主播与观众之间的互动，切合我们当今市场上的直播行业，主要目的也是为了去中心化，直接建立直播者与观众之间的交易关系，避免巨大的礼物抽成问题。

第二种营业模式
==
OpenLive Coin
--

我们也打算开发一种新的币——OLC，该币是参考Livepeer的模式，主要采用的是流量与货币之间转换的关系。在整个网络中所有的节点也分为3种，观众、主播、传递者，传递者的主要作用是接受主播传播到网络中的视频流，然后负责解码，将视频流转换成各种格式，在这其中允许任何节点发出需要视频流的信息，也允许任何节点贡献自己的流量和宽带，从而获得奖励。

下面是关于Livepeer的一份简单的摘要

Livepeer
==
Abstract:
--

The Livepeer project aims to deliver a live video streaming network protocol that can server as the media layer in the decentralized development stack. In the document, we focus on how to construct a secure network for Livepeer. In addition, we describe a protocol for the network which relates the roles and the consensus in the roles. What is more, the bandwidth from the broadcaster and consumer cost much and we can combine any user’s bandwidth and make it cheap.

Introduction and Background
--

With the development of the bitcoin, blockchain and decentralized network begin to generate a discussion and we would like to apply the technical to media layer. Therefore, Livepeer as a P2P media service appear and it will enable users to participate in the following flow:

1.	Capture a video on your camera, phone and so on.

2.	Nodes running within the network will encode it into all the necessary formats to reach every supported device.

3.	Any user on the network can request to view the stream, and it will automatically be distributed to them in the near realtime.

Livepeer Protocol
--

1.	Allow any node to send a live video into the network, and optionally pay to have it transcoded into various formats and bitrates.

2.	Allow any node to request the video from the network.

3.	Allow participants to contribute their processing power and bandwidth in service of transcoding and distribution of video, and to be compensated accordingly.

Video Segments
--

A segment is the core unit of media within Livepeer, which is a time sliced chunk of multiplexed audio and video of time length t. Every stream is made up of many consecutive segments, each containing a sequence number identifying their proper ordering. A segment contains the following fields:

![2](https://gateway.ipfs.io/ipfs/QmeBUexKn6x5GaJkHJVSa9HX13sqGEK7ActMuR5ZL4ESnu/2.png)

Livepeer Token (LPT)
----------------

LPT is the protocol currency in the Livepeer.

•	It serves as the fuel for broadcasting live video through the Livepeer network.

•	It serves as a bonding mechanism in a delegated proof of stake system, in which stake is delegated towards transcoders (or validators) who participate in the protocol to transcode video and validate work. The token, and potential slashing that occurs due to protocol violation, is necessary in order to secure the network against a number of attacks. More below.

•	It is a unit of account that is specific to the Livepeer ecosystem, which forms the basis of a SectorCoin concept, applicable to additional functionality to be introduced in the future. Services such as DVR, closed captioning, ad insertion/monetization, and analytics can all plug into the Livepeer ecosystem using the Livepeer Token as a transfer of value.

Protocol Roles
---------------

![3](https://gateway.ipfs.io/ipfs/QmeBUexKn6x5GaJkHJVSa9HX13sqGEK7ActMuR5ZL4ESnu/3.png)

In addition to the above roles played by users running Livepeer nodes, the protocol also will refer to the following systems. While we use certain specific systems to make reference to a possible implementation, alternative systems can also be swapped in if they provide similar functionality and cryptoeconomic guarantees:

![4](https://gateway.ipfs.io/ipfs/QmeBUexKn6x5GaJkHJVSa9HX13sqGEK7ActMuR5ZL4ESnu/4.png)

![5](https://gateway.ipfs.io/ipfs/QmeBUexKn6x5GaJkHJVSa9HX13sqGEK7ActMuR5ZL4ESnu/5.png)

Consensus
-------------------

Livepeer has a two layer consensus system.

1.	The LPT ledger and transactions are secured by the underlying blockchain, such as Ethereum.

2.	The second layer dictates the distribution of newly minted LPT by smart contract.

Bonding + Delegation

In Livepeer, in order to indicate stake in the network, nodes must bond some amout of their LPT. The bonded amount is used to delegate stake towards a transcoder. Any node can indicate that it wishes to be a transcoder. Newly minted token in Livepeer is distributed towards transcoding nodes that behave according to the protocol. Nodes who have bonded and delegated towards a transcoder also receive a portion of the fees that the transcoder generates through transcoding jobs on the network.

In summary, participants choose to bond their stake for the following reasons:

Participate in delegating towards effective transcoders who will provide great service to the

1.  network, ensuring its value to broadcasters.

2.	Earn token rewards in proportion to stake.

3.	Earn fees generated from transcoders.

4.	They may wish to be a Transcoder.

Total process
---------------

1.	Broadcaster -> Livepeer Smart Contract: submits a deposit on chain to cover the cost of the full transcoding job. This can be refilled later at any point, but the Transcoder may stop work if the deposit runs out as they gradually cash in for work done.

2.	Broadcaster -> Livepeer Smart Contract: Job(streamID, options, price/segment)

3.	Creates the job request on chain and places some token in escrow to pay for the work.

4.	The protocol can use the next block hash to deterministically select the correct Transcoder for this job.

5.	Transcoder -> Broadcaster: send output streamID and receipt that the job is accepted.

6.	Broadcaster -> Transcoder: send stream segments, which contain signatures verifying the input data.

7.	Broadcaster -> Swarm: Write input data payloads, using SWEAR params to ensure the data will be there long enough for verification (PersistenceLength time).

8.	Transcoder performs transcoding and makes new output stream available on network

9.	Transcoder checks Swarm periodically to ensure that the original stream data is there. If not, end the job at your discretion and claim your work.

10.	Transcoder: Store a transcode claim for each segment of transcoding work. A transcode claim has the following fields.

11.	Transcoder -> Livepeer Smart Contract: Call EndJob(StreamID, StartSegmentSeq#, EndSegmentSeq#, MerkleRoot). Transcoder is claiming on chain they have performed work on the claimed segment range, with a merkle root of all of the transcode claim data to commit to the content of these encoded segments.

12.	Wait for this transaction to be mined, and observe the next blockhash. The protocol can then determine which segments will be verified based upon the VerificationRate.

13.	Transcoder -> Livepeer Smart Contract: Provide transcode claims on chain for each segment that needs to be verified, along with merkle proofs for each segment in the transcode claims. The smart contract can verify the signatures from Broadcaster and Transcoder to ensure all data necessary is available to conduct verification, and can verify the merkle proofs against the committed merkle root from EndJob().

14.	Transcoder -> Truebit: Verify(). This is an onchain call to the Truebit smart contract, where the Transcoder provides the Swarm input hash for the challenged segment. (More on verification in the following section)

15.	Truebit -> Livepeer Smart Contract: The result of the job is written on chain. This is compared to the transcoding claim result that the Transcoder provided.

16.	Livepeer Smart Contract: at this point the Livepeer smart contract has all the information it needs to determine if the Transcoder’s work is verified.

Summary
--

In the end, the Livepeer protocol incentivizes nodes to contribute their processing and bandwidth to the network in service of transcoding and distributing live video. The verification of work is solved by a scalable extension on top of the Truebit protocol which incentivizes nodes to perform transcoding operations correctly in order to earn their fees and block rewards and preserve their value earning role as a transcoder.  The gamification of the network and false work problem is solved via the economics of the delegated proof of stake block reward distribution. It becomes more economically rational to simply stake one's tokens towards a value adding node than to pay fees into the network to be distributed to other delegators when performing work that there wasn't actually real demand for.
