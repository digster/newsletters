---
id: "web-dc166de01a9b2351"
subject: "WhatsApp owns India!"
from: "Ba from The India Notes <theindianotes@substack.com>"
to: ""
date: 2025-10-29 02:00:19
labels: ["Dharmesh Ba"]
label_ids: ["Label_6503034974112952532"]
source_url: "https://newsletter.theindianotes.com/p/whatsapp-owns-india"
origin: "backfill"
---
India’s most used business software isn’t chosen - it’s tolerated.
Over the past 18 months, I poured lakhs of rupees and time into building automation tools on top of WhatsApp - and failed. That failure opened up something bigger: a look into the tangled web that holds up India’s messaging infrastructure.
This is everything good, bad, and quietly dangerous about WhatsApp - and our growing dependence on it. It’s quite a long read.
If you’re a VC, founder, or policymaker exploring how deeply WhatsApp runs through India’s digital economy - or how we might build beyond it - I’d love to talk. DM me.
In 2023, I met a cosmetic store owner in Nagpur who had accidentally invented demand forecasting.
He sells beauty products - Korean serums, Indian sunscreens, foreign moisturizers. His challenge wasn’t competition or pricing. It was more existential: his shelf space could hold maybe 200 SKUs, but his customers now wanted access to 2,000.
Ten years ago, this wasn’t a problem. A woman would walk into his store, and he’d guide her. “Try this Lakmé sunscreen. Let me show you how to apply it.” He hired young women specifically for this - people who could explain products, who could teach.
But Instagram changed the game. Women no longer came to his store to discover products. They came with screenshots, asking for specific Korean brands they’d seen on reels. If he didn’t have it, they left. And he couldn’t stock everything.
So he invented a system.
He joined a vendor WhatsApp group - wholesalers who posted about new products arriving in the market. When something looked promising, he’d post the image to his WhatsApp status. Or he’d share it in a customer group he’d built over years.
Then he’d wait. If even two or three people asked for the price, he knew there was demand. He’d place an order before the product even touched his shelf.
He wasn’t using WhatsApp for communication and marketing alone but turned it into a just-in-time inventory system.
This was India’s answer to the Shopify + Stripe stack. Discovery happened on Instagram. Demand validation happened on WhatsApp Status. Payment happened on UPI. Small businesses had discovered that consumer apps could be hacked into business tools. In this WhatsApp owns India’s communications layer. And unlike every other tech platform, there’s no competitor even close. Instagram competes with Twitter and YouTube. WhatsApp has... nothing.
This creates both opportunity and danger.
WhatsApp isn’t a product Indians use. It’s infrastructure Indians depend on.
Infrastructure is different from products. Products are things you choose. Infrastructure is what you assume exists. You don’t think about electricity until the power goes out. You don’t think about roads until they’re blocked.
India stopped thinking about WhatsApp years ago. It’s just... there. Assumed. Essential.
This matters because of a simple truth: when something becomes infrastructure, its problems stop being individual frustrations and start being citizen problems.
A business owner spending two hours a day manually managing WhatsApp groups isn’t just inefficient - it’s a productivity tax on the entire economy.
WhatsApp work messages and personal messages in groups - it’s a design failure that affects work-life balance for millions.
The question isn’t whether India needs better WhatsApp tools. The question is whether WhatsApp, as designed by Meta for Meta’s goals, can ever serve as the infrastructure India needs.
To answer that, we need to understand what WhatsApp actually is - and what it isn’t.
Most people think WhatsApp is a single app. It isn’t. Meta offers three distinct products with different users:
WhatsApp: The everyday consumer app
WhatsApp Business: A mobile app for small businesses, with profiles, catalogs, chat labels, and auto-replies to manage customer chats.
WhatsApp Business API: Not an app but infrastructure - an API (via Meta Cloud or Business Solution Partners [1]) that connects WhatsApp to CRMs or back-end systems for large-scale messaging.
Bottom line: one phone number can be linked to only one WhatsApp product at a time. If it’s registered on the WhatsApp Business API, it can’t also be used on the standard app - and vice versa. Though WhatsApp has rolled out a recent workaround.
Here’s the critical part: these three “WhatsApps” behave very differently
The consumer app and the WhatsApp Business mobile app expose full phone UIs (groups, stories, calls, broadcast lists, catalogs) that people and small shops use directly on an app.
But the WhatsApp Business API historically only supported a subset of the app features and couldn’t do many of the interactive, UI-driven fetures that make WhatsApp feel like WhatsApp. For example, you cannot create or manage groups, post WhatsApp Status, or manage channels via APIs yet.
Update: Meta has added Groups endpoints and a Calling API to the WhatsApp Business Platform. You can now automate some group actions and initiate voice calls via the API - within tight limits and platform rules. As of Oct 28, 2025 there’s still no official API to post Status Updates like the mobile app.
In short: when small businesses say “we run everything on WhatsApp,” they usually mean the consumer or Business mobile apps - with manual groups, broadcasts, and catalogs. True automation and scale require the Business Platform/API, which is powerful but not really designed for typical SME needs.
WhatsApp’s business model is simple.
Meta charges per message on the WhatsApp Business API, with rates varying by country and message type (Marketing, Utility, Authentication, Service).
Businesses can reply free of charge within 24 hours of a user’s message; after that, only approved templates can be sent - and those cost money.
In India, rates are about ₹0.78 for marketing and ₹0.11 for utility/authentication messages. Example: 10,000 marketing messages = ₹7,800; 1,000,000 = ₹7.8 lakh monthly.
Businesses can use the platform directly via Meta’s Cloud API or through Business Solutions Providers like Gupshup, WATI, Interakt, or Twilio. BSPs add their own fees on top of Meta’s, so prices include markups and platform charges.
Most WhatsApp SaaS vendors sell both software and message credits - earning largely from those markups. When Meta changes rates, profits shrink or costs rise for customers, creating instability.
The pricing volatility makes WhatsApp a shaky base for predictable business models.
Here’s a paradox: The businesses that most need WhatsApp automation are the ones least able to use it.
For instance, one of the most common patterns we’ve seen is business owners consistently updating their WhatsApp status each morning with details about the day’s fresh vegetables, sharing posts about new stock in their groups, and responding to customer inquiries within minutes. These actions have become almost daily rituals for entrepreneurs running their businesses on WhatsApp. Such simple automations today are not possible on the main WhatsApp mobile apps but only possible in their API version.
Most small businesses in India use one phone number for everything - personal and work. But the WhatsApp Business API needs a separate, dedicated number that can’t run on the regular or Business app.
Porting the existing number would mean losing existing chats and giving up the mobile app and certain crucial features like groups management and WhatsApp status posting.
Without the WhatsApp Business API even simple automations stay out of reach for SMEs
Even with an additional number, setup is a pain. You need to link it to Meta Business Manager, create and submit message templates - all buried in Meta’s dashboards.
Many small businesses turn to unofficial modified versions (mods) of WhatsApp or to access automation and additional features. [GBWhatsApp](https://gbwaplus.net/) is the most famous unofficial app that can help you run two accounts, auto-reply, tag chats, and send follow-ups, see deleted messages - without using the official API. These tools work but violate WhatsApp’s rules, risk malware or data leaks, and can lead to account bans.
Here are some top features of the WhatsApp ‘mods’ that are helpful for SMEs
Auto Reply: Configure automatic replies per message or contact.
Message Scheduler: Schedule messages to send at set times.
Broadcast to Multiple Groups: Send one message across several groups at once.
Multi Account Support: Use two or more WhatsApp accounts on one device.
Bypass Forward Limit: Forward messages to unlimited chats.
Always Online Mode: Keep your status showing online continuously.
It’s a messy market trading serious security and compliance risks for convenience.
The irony is almost poetic: WhatsApp became essential infrastructure because it was simple and open to everyone. Yet, the moment businesses try to do anything advanced with it, it turns into a maze.
And there’s another catch: most WhatsApp automation tools live on the web, not as mobile apps.
Why? Because if you try to launch a mobile app called “WhatsApp for Business” or “WhatsApp Automation,” Meta will hit you with a trademark notice, and Google Play will take it down. So every SaaS company ends up building a web dashboard instead. But the small business owners live on their mobile devices.
If the problem were just technical limits, businesses could adapt- learn the rules, find workarounds, move on.
But the real instability comes from something deeper: WhatsApp optimizes for Meta’s goals, not yours - and those goals change without warning.
That creates systemic unpredictability that businesses quietly pay for.
Delivery drops: In 2022–23, marketing messages reached 90–95% of users. By mid-2025, that fell below 75%. Meta added hidden user-level caps to fight spam - no announcement, no numbers. Businesses only found out after delivery cratered. [2]
Sudden suspensions: Accounts get blocked - sometimes permanently - for vague policy violations. The appeal process is slow, and while it runs, operations stop cold. [3]
Shifting rules: In Oct 2025, WhatsApp quietly banned all “general-purpose AI chatbots.” The term isn’t defined, leaving even compliant tools exposed. [4]
Even if you master the tech, pricing, and compliance, you’re still building on shifting ground - where Meta’s priorities decide your uptime.
Here’s the uncomfortable truth: these aren’t problems Meta is trying to solve. They’re features of the system working as intended.
Meta is an advertising company; ads pay the bills.
Every product in their portfolio - Facebook, Instagram, Messenger, even Oculus - exists to collect data and sell ads. WhatsApp is the outlier. It’s a messaging tool that, in a different world, might have evolved like Telegram, Slack or Microsoft Teams: an open platform where developers build productivity tools, businesses customize workflows, and ecosystems flourish.
But that’s not Meta’s DNA.
If WhatsApp opened up like Slack, businesses would build their own solutions. They’d customize the experience. They’d create value that Meta couldn’t capture. From Meta’s perspective, that’s money left on the table.
So instead, WhatsApp is being slowly transformed into an ads platform. You’re starting to see it:
Ads in WhatsApp Status (already rolling out)
Paid WhatsApp channels (in beta)
Business messaging in groups
Click to WhatsApp ads
From a pure business perspective, this makes sense. Why would Meta invest engineering resources to solve a hundred-million-dollar problem (Indian MSME productivity) when they could deploy those same resources toward a billion-dollar opportunity (WhatsApp ads)?
To put it bluntly: Meta doesn’t care about your kirana store’s inventory management problem. Not because they’re evil, but because they’re a trillion-dollar company optimizing for trillion-dollar opportunities.
WhatsApp will never be the open platform India needs, because Meta’s business model requires it to stay closed.
Which raises an obvious question: If WhatsApp can’t serve as the infrastructure India needs, what can?
India’s WhatsApp problem isn’t unique. China faced something similar a decade ago - and solved it deliberately.
WeChat handles everything WhatsApp does, plus native payments, mini-apps, ride-hailing, food delivery, and government services. The architectural choices Tencent made are precisely what WhatsApp lacks.
In WeChat, businesses can send users only 4 marketing messages directly per month through service account. Beyond that, marketing messages get quarantined into a separate subscription feed/folder - visible but segregated from personal conversations.
This forces discipline. Every message must justify its existence. The result: businesses target better, users feel less harassed, and the platform maintains trust.
WhatsApp has no such limits. Businesses face tiered messaging caps (starting at 1,000 recipients daily for new accounts) but these scale automatically based on quality scores. The only real constraint is cost - and when marketing messages work, companies pay willingly. The incentive structure rewards volume, not restraint.
When an employee leaves a Chinese company, their WeChat relationships vanish with them- customer conversations, sales context, years of institutional knowledge, gone.
Tencent solved this with WeCom (WeChat Work), a parallel app for professional communication. In WeCom, workplace conversations belong to the company, not the employee. When someone leaves, their account transfers. Customer relationships survive.
Search for a person on WeChat in China, you see two options: their personal WeChat, professional WeCom. Same ecosystem, separate contexts. You message friends on WeChat, coordinate work on WeCom. Both feel familiar, both interoperate, neither bleeds into the other.
In 2022, WeCom has about 180 Million active users and are used by over 10 million businesses in China. [5]
The boutique store owner shouldn’t manage customer orders where his daughter sends memes. The sales team shouldn’t lose client relationships when someone quits. The contractor shouldn’t coordinate labor in the same group planning his wife’s birthday.
The solution exists. WeCom proves separating contexts without fragmenting networks is possible. But WhatsApp won’t implement it - not because of encryption, but because of infrastructure.
WhatsApp’s value to Meta isn’t in reading your messages - they’re encrypted. It’s in the metadata around them: who you talk to, when, from where, and which businesses you engage with.
Meta has added ads to WhatsApp’s Status tab, but the real value lies in metadata and business messaging, not large-scale ad placements. Linking WhatsApp, Facebook, and Instagram through Accounts Center lets Meta build a unified behavioral profile - without touching message content. [6]
Splitting personal and professional WhatsApp use would shatter that identity layer. Meta wouldn’t lose access to messages - it never had them - but it would lose the metadata correlation powering cross-platform personalization.
Keeping all communication in one place creates richer data, tighter business tracking, and a more valuable ecosystem.
Which leaves the real question: if Meta won’t separate it, who will?
WhatsApp isn’t going anywhere.
Half a billion Indians won’t switch apps. Businesses won’t rebuild customer relationships. The network effects are too strong, the switching costs too high. Our goal should be to build optionality in the form of building ONDC-like infra for messaging. A protocol could make the platform used irrelevant.
Instead of building one mega-app to rule all of e-commerce, ONDC built the rails underneath. A seller listing on one ONDC app can be discovered by buyers on completely different apps. Orders, payments, fulfillment - all work across platforms. No gatekeepers. Just open infrastructure.
The same architecture can break WhatsApp’s monopoly.
A messaging protocol doesn’t need 500 million users on day one. It needs 500,000 users who will pay because the protocol solves a problem WhatsApp won’t.
For example we could start with construction contractors. They need labor coordination, site photos, payment tracking, and material orders - all over messaging. WhatsApp works, but barely. A purpose-built tool would save them hours daily.
That’s the wedge. Once one vertical proves interoperability works, others follow - logistics, healthcare, education, government services. The network grows without forcing anyone to switch.
The protocol layer should provide the essential stuff:
End-to-end encryption standards
Message delivery guarantees
Identity verification
Cross-app routing APIs
Different apps build specialized experiences on top: One for Gen Z, one for the elderly, one for MSMEs and they should all be able to talk to each other. Same network. Different interfaces.
Just like you can email someone on Gmail from Outlook. The protocol doesn’t care. It just routes messages. Email, the web, and Bluetooth already work on open protocols.
WhatsApp solved India’s communication problem. Now India needs to solve WhatsApp’s incentive problem.
That doesn’t mean banning WhatsApp or building a clone. It means creating optionality - a messaging layer where WhatsApp is one choice among many, not the only one that works.
This isn’t about nationalism or rejecting foreign technology. It’s about infrastructure resilience. No nation should have its business communication layer entirely controlled by a single foreign corporation with different incentives.
The question isn’t whether to replace WhatsApp.
The question is: What does India need to build so that WhatsApp’s limitations stop being India’s limitations?
That’s the conversation worth having.
If you liked this essay, consider sharing with a friend or a colleague that may enjoy it too. (If you share on socials, tag me. I’m on [Twitter (X)](https://x.com/dharmeshba) and [LinkedIn](https://www.linkedin.com/in/dharmeshba/))
Shoutout to [Gowri N Kishore](https://www.linkedin.com/in/gowrink/) and [Krishna Hegde](https://www.linkedin.com/in/krishnahegde/) for reading the preview and helping sharpen the edits.
[WhatsApp’s New Marketing Message Limits Policy Change: Detailed Guide](https://support.exotel.com/support/solutions/articles/3000125954-whatsapp-s-new-marketing-message-limits-policy-change-detailed-guide)[WhatsApp Business API Account Disabled? Here’s How to Unban it!](https://wanotifier.com/unban-disabled-whatsapp-account/)[WhatsApp changes its terms to bar general-purpose chatbots from its platform](https://techcrunch.com/2025/10/18/whatssapp-changes-its-terms-to-bar-general-purpose-chatbots-from-its-platform/)[WeChat’s corporate communication tool reached 180 Million active users](https://pandaily.com/wechats-corporate-communication-tool-reached-180-million-active-users)
You can download the People’s Voice report on AI opportunities for Indian SMEs, created by [People+AI](https://peopleplus.ai/) in collaboration with [1990 Research Labs](https://www.1990labs.com/), below.