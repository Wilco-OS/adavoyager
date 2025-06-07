Questano is not just a playground for users; it’s also a powerful tool for **Cardano project partners** to drive engagement. The platform provides integration points for projects to set up their presence (guilds or factions), create quests, and distribute rewards in a seamless way. This section outlines how partners can integrate with Questano and manage their campaigns.

### **Setting Up a Guild (Partner or Community Guilds)**

While most guilds are player-created, occasionally a project team or community may want to establish an “official guild”. This could be useful if a project’s core community wants to band together under a project-themed guild name (though faction covers most of that need). If a partner wants a guild:

- **Guidelines:** They would create it like any user but likely get a verified status or special support from Questano team. For example, the SundaeSwap team might create the “Sundae Knights” guild for their community core members, separate from the faction concept.
- **Use Case:** However, generally, projects would focus on the Faction side for broad community, and leave guilds to organic player groups. So official guild creation is optional and case-by-case. If done, it follows the same creation rules (maybe fee-waived for partners as a courtesy).
- **Community Leaders:** Alternatively, a project might encourage their community to form guilds named after the project (e.g. multiple guilds all supporting the same faction). It’s up to players.


### **Faction Onboarding Guide**

For any Cardano project to become a Questano faction:

- **Contact and Approval:** The project would reach out to Questano’s team (or vice versa). They provide information like project name, description, logo, and agree on collaboration terms. The Questano team then creates a **Faction Page** for them in the platform.

- **Faction Dashboard:** Partners likely get access to a partner dashboard or **admin panel** specific to their faction. Here they can:
    
    - Create and manage quests for their faction.
        
    - View analytics on how many users are doing their quests, how their faction rank and fame distribution looks.
        
    - Manage rewards (deposit tokens/NFTs, configure distribution).
        
    
- **Quest Creation (Partner’s Role):** Questano provides a quest builder interface. Partners can define quests of various types (with some templates to choose from):
    
    - Off-chain tasks (like social media, content) where they specify the validation method (manual review, or using APIs for Twitter etc.).
        
    - On-chain tasks, where Questano can automatically verify certain actions (Questano likely has or uses an indexer to see if a user’s wallet did X).
        
    - They set the quest description, requirements, start/end date, and the rewards (points, fame, any tokens or NFTs).
        
    - They can mark quests as repeatable or one-time.
        
    - After defining, they submit for review. Questano team might review to avoid spam or security issues, then approve it to go live.
        
    
- **Reward Funding:** Partners typically should provide the **prizes** for their quests, especially if those are tokens or special NFTs:
    
    - **Token Rewards:** If Project Y wants to reward 100 of their tokens to each successful quest completer (or maybe a pool of tokens split among them), they will allocate those tokens. They might send a batch to a Questano-controlled wallet or use an automated method.
        
    - **DripDropz Integration:** One convenient method for token distribution is DripDropz. Questano can compile the list of wallet addresses eligible for a reward and use DripDropz to airdrop the tokens to them. DripDropz is a Cardano token distribution service that, for a small fee, lets users claim tokens if they meet criteria . In fact, DripDropz allows projects to configure distributions such that users can claim tokens by just entering their address . Questano leverages this by potentially adding the quest reward as a “droppable” token.
        
        - _For example:_ Clarity Protocol integrated DripDropz so that users could instantly claim earned tokens (“Diamonds”) once they completed tasks . Similarly, Questano could trigger an entry on DripDropz for each eligible user (or a bulk listing at quest end), enabling them to claim the partner’s tokens in a trustless way.
            
        
    - **NFT Rewards:** If the reward is an NFT (say the partner wants to give a special badge NFT to quest completers), the partner can either pre-mint them and hand to Questano to distribute, or Questano can handle minting via a provided policy. Often, Questano might offer a **minting service** for quest NFTs (possibly using a tool like NMKR under the hood, since Cardano gaming projects often use NMKR for NFT issuance ).

    - **Merch/Off-chain:** If rewards are off-chain (e.g., T-shirt), the partner handles fulfillment. Questano can provide a list of winners to the partner after the quest.


- **Analytics and ROI:** Partners will want to see results. Questano’s partner dashboard can show metrics like:
    
    - Number of participants in each quest.
    - Increase in followers or usage (for social or on-chain tasks, these can be roughly measured).
    - Wallet addresses of participants (useful for partner’s own follow-up campaigns).
    - Feedback collected (if quests include surveys).

- **Use of Data:** Partners can analyze which quests were most popular to refine their engagement strategy. For example, they might find tutorial quests are completed by 500 users but advanced ones by only 50, indicating drop-off points.

- **Integration into Partner’s App/Website:** Some projects might want to embed Questano quests on their own site (to show “Questano quests for our project”). Questano could provide widgets or APIs for projects to list their quests on their site, driving their users to participate.

- **Verification & Security:** From a dev standpoint, partner integration should ensure that verifying on-chain actions doesn’t require unsafe access – Questano likely uses **read-only APIs or smart contracts** to verify quest completion, preserving user security. For example, verifying a swap on a DEX can be done via chain history, no need for user to give private info.
  

### **Example Scenario for a Partner**

Suppose **Project Catalyst** (Cardano’s community fund project) integrates as a faction:

- They set up quests like “Vote in Fund10 Catalyst proposals” – which Questano verifies by perhaps requiring a screenshot or using a Catalyst API if available. They allocate 1000 of their community tokens to reward participants.
- Questano collects the list of wallets of users who completed the quest and uses DripDropz to drop the tokens: each eligible user can claim, say, 50 Catalyst tokens via drip after voting. This approach has precedent: AdaQuest, another Cardano game, distributed its community QuestToken to supporters via DripDropz every epoch , showing how tokens can be regularly dispensed to engaged users.
- After the fund’s voting period, Catalyst team sees that 300 users completed the quest, meaning 300 voters engaged via Questano. They see maybe 50 of those were new voters who mention they discovered Catalyst through Questano – a win for them.
- They might repeat or adjust quests next fund or invite those users to deeper involvement.  

### **DripDropz Integration Details** 

Because this is specifically mentioned, let’s detail how **DripDropz** helps:

- DripDropz normally distributes tokens to stake delegators or based on criteria, where users claim by paying a small ADA fee . It’s very useful when you have to send tokens to thousands of addresses (doing that manually would be expensive and slow; DripDropz streamlines it).

- Questano can use DripDropz in two ways:

    1. **Quest Completion Airdrops:** After a quest, Questano provides DripDropz with a CSV of addresses and token amounts to distribute. Users then go to DripDropz (maybe via a link in Questano) to claim their tokens. _Pro:_ offloads distribution and uses a proven system. _Con:_ user has to take an extra step to claim (but many Cardano users are used to DripDropz)
    2. **Ongoing Rewards (Epoch-based):** For long-running contributions, a partner could set up a continuous Drip for Questano users. For example, if a user holds a Questano NFT or is part of something, they might get X tokens per epoch via DripDropz. This is more speculative

- The integration likely involves Questano partnering with DripDropz or using their API. Clarity’s example shows you can integrate it such that rewards are available immediately for claiming .

- The benefit: **Secure, fair distribution** of partner tokens without Questano having to custody or individually send tokens to each user. This is both convenient and adds trust (since DripDropz is known as a neutral distributor ).

  

### **Developer API & Integration**

For developers, Questano might offer:

- **API Access:** If a project wants to programmatically create quests or pull quest data (maybe for their own app), Questano could provide REST or GraphQL APIs. For instance, a dApp could trigger a quest completion event via API when a user finishes something on their platform.
- **SDK or Libraries:** In the future, there might be a Questano SDK for Cardano dApps, making it easy to connect on-chain actions to Questano’s quest completion logic.
- **Webhooks/Callbacks:** Questano could notify partner systems when a user completes a quest, so the partner’s app can also celebrate or record that.
- **Single Sign-On:** Possibly an integration where if a user is logged in to Questano, partner sites can detect that (though likely not needed, as the wallet connection is central).

### **Content Management (CMS)**

Questano likely has an internal CMS for managing static content (like the wiki itself, news updates, help sections) and possibly quest content. For partners:

- They might get limited CMS features to create rich descriptions for their faction page or quest lore, etc.
- The Questano team will use a CMS to publish announcements (like season story, patch notes, etc.) which show up in the app.

### **Partner Support and Collaboration**  

Questano will have a team to support partners:

- Helping them brainstorm quest ideas that suit their project and users.
- Ensuring quests are balanced and not prone to exploitation.
- Possibly co-marketing: announcing new factions or special partner events via Questano’s channels.  

By providing these integration capabilities, Questano positions itself as a **growth platform for Cardano projects**. It’s not just a game, but a marketing and user acquisition tool that projects can plug into, with much of the heavy lifting (verification, distribution, gamification design) handled by Questano. Partners can focus on what quests to offer and what rewards to give, and then enjoy the influx of engaged users.