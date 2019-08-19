# Community
Building liquid communities for the ethereum blockchain

## Abstract
The internet has made the world technologically united. As a result, many new internet communities have emerged. Large (such as Facebook, Twitter, Github) and small (such as a fitness club or an association of local bird watchers). The large internet communities penetrate all geopolitical communities (such as nation states). These new internet communities have some serious shortcomings. They are not real communities. They are externally motivated by parties that are focused on an increase of consumption, economic or political power. The communities are not driven by the members themselves. These communities therefore usually have no democratic infrastructure (administration, elections, votes) and are a permanent plaything for geopolitical actors (China, Russia). The blockchain gives us the opportunity to create new communities that are democratic, run by members, and thus potentially play their own, independent role in changing geopolitical relationships in the world.

This project creates new communities and supports existing communities by making them fluid. Liquid communities have the following essential characteristics: People can join the community and leave the community. The communities can take positions or make decisions by a democratic voting process. The communities can elect members in organs through elections. Communities can be merged in a larger community. Communities can split into parts (horizontal differentiation). Parts of the communities can split off while maintaining a hierarchical relationship (vertical differentiation). The communities have a fluid democracy that supports direct democracy, representative democracy and a composition of both.

The Dapp (Decentralized application) to be built for liquid communities is a DAO, a decentralized autonomous organization, but the property of fluidity also implies that the DAO is able to 'simulate' existing (centrally controlled) organizations in a decentralized environment (the blockchain). This means, for example, that all liquid communities have a governing organ.

The design of the DApp consists of 8 types of solidity contracts that are stacked 'on top of each other'. They are called People, Identity, Community, Democracy, Trust, Ballot and Relations. Read the WHITE PAPER for the structure and functions of these contracts.

**Schedule**:
* 2018: first draft of blockchain contracts
* 2019: testing solidity contracts (remix, rinkeby)
* 2019: github publication
* 2020: search for cooperation partners, building community of developers of liquid commuinties
* 2020: website liquid communities.

** License **: read LICENSE file
**Background information on the idea of fluidity**: publication of PPeu, from geostat to neostat.
See also my new publication liquid communities (shortly after)

## Preface
How do we build new communities, supported digitally that can range from small thematic communities to a global community? Where do you start? With a page on Facebook? A Google hangout group? Twitter? One of the countless apps on internet that support "community-building"? Unfortunately, none of these options is suitable for building liquid, democratic communities. The problem with these apps is first and foremost that they are mostly commercial products from companies that want to earn money with them. Although these companies present very idealistic motives to us, facilitating a community is a revenue model for them. A company simply has to make money, sell products, attract consumers and promote trade. If companies sell their apps for "free", it's not for nothing. The use of the apps provides companies with data, which they then sell or use to serve advertisers. But a community is not just a marketplace. It is much more. A community is a social system with an internal structure, views, positions and interests that constitute a social identity of the community and specific processes that develop the identity by means of democratic decision-making. If you want to build a sustainable community, it must be made **by** and **for** the people of that community. A revenue model with advertisements is neither suitable nor correct.
Liquid communities, like other communities, small and large, will be build on a financial contribution of their members: you can call it a contribution, a subscription fee, a tax or other form of payment. This contribution can be understand as a barrier to gaining access to the community. But it is not. It is an act of commitment, a confirmation of wanting to be part of the community. When there are enough members the (virtual) community can perform its common tasks. By also becoming active within that community itself, a deep bond with that community will be created.

Every real community, including a liquid community, has a board that is elected by the members of the community. Large communities also have a parliament, i.e. a house of representatives of the people that control the administration. The board/administration (or individual members) can prepare proposals to be approved by the parliament. The representatives maintain a close relationship with the citizens they where elected by. Facebook is by no means a real community. There is no democracy. There is not even a autocracy. The management of Facebook is neither formally nor informally appointed by its customers. The management does not act in the name or in the interest of its customers. The management only acts in the interest of the company.

Besides the similarity of financing a community there some important differences between liquid communities and permanent geopolitical communities. Liquid communities do not have 'mandatory membership' based on birth or place of birth. Every person freely decides whether he or she wants to become a member of the community or leave the community. Liquid communities therefore do not make exclusive claim to territory. But they can penetrate all existing geo-communities. A large liquid community that develops into a close-knit community can eventually lead to a confrontation with the old geo-communities (read more about this in form geostates to neostates).
The power of fixed communities, like  nation states, large corporations, platforms, or religious movements, is based on the idea and the practice of centralism. There is a center, that center gathers power and with that one is able to steer and control the community. The blockchain is a new technology that "decentralizes" this centralism, which bypasses traditional power, which makes it possible to develop a community without a central power center. The blockchain is ideal for building new liquid communities.

The blockchain is a decentralized accounting system. We will record the entire 'accounting' of a liquid community (members, bodies, memberships, proposals, nominations, votes, elections and delegation of trust) into 8 blockchain contracts. While fixed communities store this data centrally, behind a firewall, often inaccessible to members, in a liquid community based on the blockchain, this data is accessible and at the same time protected against malicious actions (of manipulation of data) through cryptographic calculations in combination with decentralized storage.

The blockchain is transparent. That is an essential condition for building a close-knit community. All transactions can be viewed and requested (but never changed). So there are no shadowy algorithms that inimitably determine who will be at the top of a Google search query result. There are no central "secret" considerations. The blockchain, precisely because a central authority is missing, has no secrets. This has major advantages: there are no fraudulent transactions, there are no hidden accounts, no false addresses, in short, no corruption is possible. And if a rogue method is nevertheless devised, it is registered in the blockchain for eternity. With the given transparency of the blockchain, this also means that everyone, even years later, can find and disclose the fraud.

Because of the cryptographic requirements ("Mining") saving a transaction in the blockchain will be very slow compared to, for example, a bank transaction that takes place in a central environment. To put it better: a transaction from the Dapp costs thousands of times more computer time (and therefore energy) than a normal transaction from an App. Another difference is that the performance of functions, or the modification of data, is not free but must be paid immediately (to the miners who do the work for us). This means that the costs of maintaining a fluid community can quickly become very high as a community grows. That is why it is crucial that liquid communities have instruments that make large communities work more effectively and efficiently: those instruments are: organization and trust. Large communities cannot do without an extensive organization and in particular a body of representatives. In addition, a liquid democracy has a trust contract: community members can - at any time - put their trust in or withdraw their trust from another member of the community with regard to voting. If these two instruments are used properly, the number of transactions in large communities will be dramatically reduced, costs will decrease, the community will become more effective and flexible and a strong sense of community will arise.

## The blockchain contracts of a liquid community
The Dapp designed here supports different types of communities, the Dapp uses little energy (which is important if we want to be able to support very large communities) and the Dapp is flexible enough to adapt to new wishes and demands of a community. The Dapp design consists of 7/8 interrelated contracts, which together form a new social contract between community and members. They blockchain contracts have the following names: People, Identity, Community, Democracy, Trust, Ballot, Relations (and Economy). Each contract has its own functions that determine the rules and laws of this specific part of the social contract. Together they form a kind of "constitution," but there is territorial part in this constitution. This community is virtual. Because the rules of this constitution are automated into blockchain contracts, they are, although virtual, stronger than an ordinary constitution: they are carved in stone and cannot be changed.  

The **People** contract is a basic registration. The People contract registers people. Every person must be identified as a unique person. People can build one or more communities. No person may appear twice in this basic registration, because this would in principle give the person the opportunity to vote twice on the same matter. That's not allowed.

Anyone registered and identified in the People contract can start a new community. This creation process consists of two parts: A (social) **Identity** of the new community is defined: for example, the residents of flat X in city Z. The bird lovers of the region R. Jehovah's Witnesses, the followers of the theory Z, the baseball club 'sets it up', the fans of Madonna, the IT specialists of multinational Y. The fan club of footballer H, the members of political party P, the citizens of street S, the citizens of city A, the citizens of the world state, etc etc.
Simultaneously with the creation of the new Identity, a new (still empty) **Community** contract is created. The person who has appointed the Identity contract is the first member of the Community linked to the Identity, and at the same time also the first (temporary) member of the board of the Community. Thereafter, others (other persons of the same People contract as the founder) can now join the Community by becoming a member. In the Identity contract the membership and the status of the members is registered.
Note: the Identity contract reflects the identity of the community. Of course this also contributes to the individual identity of the people/members of that community. But the concept of identity here is explicitly linked to the **social** unity of the community and not to the individual. The People contract only has the role of identifying the person. In principle, a unique number is sufficient here (passport number, social tax number, membership number). Read more about the background and meaning of identity and identification in the WHITE PAPER.

The organizational structure is laid down in the Community contract. A community has two bodies when it is set up: an administrative body and a representative body. In small communities, the seats of the representative body does not have to be occupied with members. But there must always be a board with at least one member. Members can add new organs to the community, which usually perform specific tasks within the community. Organs also play an important role in the functioning of democracy. Only temporary organs with a minimum number of members can submit proposals, which can be voted on in democracy.
Note on translation (Dutch to English): I will use the term 'Organ' within the blockchain contract Community for a part of a community, in analogy of biological terminology. The community is considered to be an (complete) body. Organs are body parts. Stictly speaking, in my terminology, the board is not a body but a body part. I will omit the text 'part' or when things can be confusing, i will use the biological term 'Organ' in a social context.   

Identity and community are to seperate contracts, but they are created simultaneously. In many situations, identity and community can be used interchangeably, because only one community belongs to one identity. However, it is possible, especially in large communities, that new additional communities arise under the same Identity. A permanent organ of a community can transform itself into a separate (sub) community within the same identity. This sub-community can create new organs within itself and those organs can again become sub-communities. Etc etc. A vertical hierarchy of communities within an identity will be created.
In addition, neighboring communities can also be defined within an identity. In fact, it is even possible to set up several separate, unrelated communities within one identity. The Relationships between the communities of an Identity are maintained in the **Relations** contract, comparable to the international relationships between national, geopolitical communities. The Relations contract regulates communication between the communities: the method of representation, the financial relationships and the way in which proposals are transported from one Community to another. If an identity has only one community, a relationship contract is superfluous.

Each Community has one or more **Democracy** contracts in which community proposals can be drafted and meetings can be convened to put those proposals to the vote. Democracy is used to grow and develop the Community, both in organizational structure and in identity, shaped by a series of views of the community. The debate on proposals takes place outside the blockchain (in all kinds of websites and social media). If the proposal is 'mature' enough, the board can put the proposal on a meeting and offer it to the Community for a vote. The course of a community is determined by the result of the votes. Proposals can only be put to the vote in meetings. Meetings are essential for communities. Of course, proposals in a blockchain could also be put to the vote at any given moment seperately, but then an important community aspect will be lost: the social gathering, where people meet each other physically and virtually.
The virtual meetings will often be accompanied by real physical meetings where people meet. They are the focal points of the democratic process of a community, which will be full of debate, lectures, discussions, explanations or just festivities, whereby every proposal is concluded by a virtual vote in the blockchain.

The sixth contract is **Trust**. No (large) community can do without Trust. Not everyone can do everything. Sometimes you have to put faith in others. In elections for members of a representative body, members of a community entrust their vote to others, delegate their vote (voting weight) to representatives that they trust. It means you do not have a vote any longer, but the representative gets an extra voting weight. Your vote is cast through his vote. The election of people into seats of organs are also conducted by proposals in a democracy. In this case a proposal will fill vacancies in a body for which people can apply. In the Trust Contract every member of the community can store his rules for delegation. This rule establishes who you trust in certain matters and for how long. A rule of delegation can contain four types of trust. The representative democracy of a fluid community will become much more complex, more flexible and more powerful. The bond between voter and elected person will become many times stronger than it is now.

Finally, the seventh contract, the **Ballot** contract. If a proposal is voted on at a meeting, a new special Ballot (contract) will be created. In this contract the voting of the members of the community takes place. Voting in the block chain takes a time period that can last from hours to weeks. Voting is always anonymous unless you have received the trust of others. People who carry a vote weight greater than 1 must show that they have voted and what they have voted for. Representatives can never vote anonymously.
Voting is precious. In large communities with many delegation rules, a vote can take a relatively large amount of computer time. That is why a board should be able to settle a vote that is only a formality by acclamation.

There is an eighth contract (the **Economy**-contract) that converts the adopted proposals into economic and financial transactions. This contract falls  outside this project that focuses on community building and strengthening social cohesion.

These 7 contracts are further explained in the WHITE PAPER. But before you start reading, two basic (philosophic) principles of the Dapp must first be presented here: the principles of fluidity and the need for servants for a community.

## The function of liquidity in communities
Liquid communities are open democratic communities that do not make an exclusive claim to a territory. The identity of the members are not determined by the birth ground but only by the material bond between member and community (a central task of the board). This bond will therefore be made stronger (by the administration) than ordinary, ground-bound communities (by proposing, taking positions as a community and by improving the functioning of democracy). But the strong bond also gets a counterbalance: fluidity and mobility. Members can "cancel" a community or change their community. New scalable and parallel communities can arise within an identity. In the Identity Contract, scalability is built in by the possibility of transforming an organ into a community that remains connected to the source body community. Parallel communities are neighboring communities that are not hierarchically related under an identity.

In present fixed geopolitical states there is a great tension between identity, homogeneity and diversity, between inclusiveness and exclusivity that regularly leads to conflicts. In liquid communities we try to "discharge" this field of tension in a natural, virtual way. If the differences in a community increase, this does not have to lead to unfruitful polarization and opposition, but new communities can arise, in which members can further develop their own identity. New relationships can be established between the communities based on this 'individuality'. I therefore try to resolve issues concerning the inclusiveness and exclusivity of communities through the social reorganization of communities. Through scale differentiation, a hierarchy of communities each with its own governance and organization, we simultaneously create new identification options for the members of the identity.

In our Dapp we provide another form of mobility and reorganization. A community with its own identity can "move" to another Identity and become a sub-community of the new Identity. The source identity loses its role. The other Identity changes into a double community.
The (new) Relations Contract regulates communications between the communities. Proposals that are accepted in an organ community can be "automatically" submitted in the body contract they are part of. And vice-versa. Financial relationship and relationships of representation strengthen the bond between communities, and thereby strengthen Identity as a whole. The reverse can of course also happen. Organ communities can become autonomous or split off into a new identity of their own.

Neighboring communities can stimulate a horizontal mobility: members can switch between two neighboring communities. Neighboring communities can have the same body community. But that is not necessary. This horizontal 'migration' is a well-known problem of geopolitical states. It can also play a role in virtual communities. The solution in liquid communities is not to "build a wall," or to deny access, but to work with different citizen statuses. Rights (to vote or to propose or become organ-member) can be assigned to different statuses. Persons who move to another liquid community can start off with a 'lower' status which will be upgraded in time gradually.
For example, if you move from city A to city B, you cancel the membership of the liquid community of the volleyball club in city A and you become a member of a volleyball club of city B. The new member will not immediately have access to policy bodies of his new community. He must first "prove" himself as a good loyal member of the new association before the member gains access to organs. This process can be arranged using the status field of the membership.

Internal mobility and social cohesion of a community are reinforced with a new type of democracy: a fluid democracy in which direct and representative representation are closely integrated. People can vote for themselves or through another member they trust in by creating a rule of delegation. As a consequence the voting process in a liquid community is very dynamic and flexible process. It creates and supports all kinds of new (political) participation.

The voting right is connected to social Identity and not to the community. If an identity has only a single community (which will occur relatively frequently), this innovation is invisible. It has no impact. But if an identity has many communities you can only be a member of one and precisely one community. A member is therefore obliged to choose. Of course a person can be a member of many different identities. The issue hier concerns the communities of a single identity.
This is an important rule in the Dapp. The choice of the community determines where you have the right to vote and therefore in which community your vote counts. That choice gives weight / mass to the community. The choice indicates what you find the most important community within an identity. This choice implicitly determines the balance of power between the scales of community within an identity.
A similar rule exists in fixed geopolitical communities: national citizenship. A citizen is a member of one and precisely a nation state. Obtaining a new nationality usually means losing the old nationality. In our present time of migration the latter will be less and less the case. Today many citizens have acquired multiple passports / nationalities. Other citizens have become stateless due to war or persecution and formally do not belong to any community at all. In liquid communities we 'restore' this loyalty choice within a single identity.

Finally, De Dapp offers people the opportunity to join many different identities. The members of Identity A cannot communicate in any way with the members of Identity B. They are separate worlds. They don't see each other. That does not seem to be a problem when the communities are 'a fishing club in Harlingen' and 'the rugby club in Brazil'. They have nothing in common so the do not need any communication. But one of my principles in the design of the fluid communities is that we all live on ONE Earth and that ultimately we all are members of that ONE global community. Liquid communities are not designed with the intend to create gated liquid communities (but I do not exclude the possibility this Dapp will be abused for that purpose), but rather to connect all communities of the world, to let them flow together because they share the Earth and yet meet the wishes of people to create new social identities.

## Servants of the community
With the 7 blockchain contracts, all community processes can be fully automated in a decentralized administration. However, I do not think that is desirable. Additional "degrees of freedom" must be built into a community. That is somewhat paradoxical: the decentralized administration of the blockchain offers the possibility to eliminate fraud, corruption and other forms of manipulation that are implicitly attached to a central administration, but here I propose to re-enter the human factor, which is evidently reducing the powerful properties of the blockchain. Why introduce a human factor in decentralized registration, an introducing the the risk that certain people will play a central role, who, after all, can introduce corruption or fraud to that registration? Why should we not legally "regulate" all the tasks of the community - management, policy, administration, preparation and implementation - in the new blockchain social contract?

There are three reasons: First of all, a community is not an automation system that has to be controlled like a production process of a factory. A community consists of many different people with their own views and ideas. The human social capacity is in fact a big 'unknown'. We do not know what communities can produce. We do not know which communities can arise. We do not know whether some communities do not want to function differently from the rules that I am proposing. That is why I think that community processes should always include moments of human consideration, so that the system can work differently than the built-in rules of the blockchain contracts predict.

The second reason concerns the significance of technology in a broad sense. Every technology can be used right and wrong. Technology, including the blockchain, can one moment be cheered at being the solution to a problem, and the next moment be a major "oppressor" of human development. For the same reason, I would not accept being taken care of by a future care robot (no matter how intelligent!) Without an on / off button. The problem with technology is, even if it is designed with the best of intentions, there will always be situations where the built-in rules of technology should NOT apply. So I don't want blindly to rely on technology.

And the third reason is the role of power. A healthy community recognizes the existence of power and ensures that there is a good balance of power in which as many people as possible can exert maximum influence over the course of a community. This is the premise of democracy. The human factor is a degree of freedom to make corrections and is needed to fine-tune the balance of power within a community (later on).

How is the human factor built into the blockchain contracts? The most important balance of power is regulated by defining two organs to each liquid community(body): a board and parliament. They are countervailing powers. They are the executive and the legislative power of the trias politica. If the parliament body is not used (the seats remain empty), the legislative power will be transferred to the members of the community. Every proposal will have to be voted for community-wide.
The third power, the judiciary, which in our current societies speak "justice" in conflicts between members or between members and the community, is missing in our liquid community because software does not impose differences of interpretation or conflict. This does not alter the fact that the software itself can be changed. If we encounter program errors, they must be corrected. And of course we can adjust the operation of the contracts by changing its functions. For the development of liquid communities, it is extremely important that the blockchain contracts themselves can develop further (new versions). But that is an external factor. We have therefore not yet realized a human factor in the operation of the system itself.

In my design of liquid communities I chose to implement the fourth power - the power of the civil servant - that is not part of the trias politica, into the blockchain contracts. I designed a separate category of members that, on the one hand, has extra 'powers' and, on the other, has extra limitations. I call them the servants of the community. The role of the servants is to prepare, monitor, manage and implement. Servants may never submit proposals themselves or become candidates for a position of board or representative. Conversely, administrators and representatives do not have the additional powers of servants to manipulate certain processes. The extra powers of the servants consist of 'implementing status changes'. The 5 basic entities (structures) of the Dapp, i.e. a person (of the People contract), member (of an identity contract), an organ (of a community contract), a proposal or a meeting (of a democracy) contract) have a status-property that reflects the current state of that entity, which can be changed by the rules of the contract AND by servants, enabling servants to make modifications that do not follow from the rules of the system itself.

The role of community servants is to actively promote, guide and guard the organizational and democratic processes of the community, without introducing a new bureaucracy. The servants are technical experts in the operation of the system and are therefore a source of information for all members. They are also concerned with the functioning of the community itself. They are an independent neutral power, and can act at their own discretion and on behalf of the board or community. Their primary task: service to the community. A servant cannot be a director or representative and may not make proposals, but may of course vote. He or she is a normal member of a community. In the WHITE PAPER I will discuss the special servant functions per contract.
Servants of an identity (just like for example Wikipedia moderators) form a "own community" within the identity in which they judge each other's actions. They judge their own actions on neutrality and accuracy. Servants who abuse their role can be ejected by the community.

Read the WHITE-PAPER about the details of this Dapp.
