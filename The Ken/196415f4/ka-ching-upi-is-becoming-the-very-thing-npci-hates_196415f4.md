---
subject: "Ka-Ching!: UPI is becoming the very thing NPCI hates"
from: "The Ken <info@the-ken.com>"
to: ""
date: 2025-04-17 01:31:22
labels: ["CATEGORY_PERSONAL", "INBOX", "The Ken"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_8244464457792971031"]
---
|
|
Ka-Ching!
Thu, 17 Apr 25
A weekly newsletter about how finance is getting supercharged by tech in India, and how you can make money work for you..
Good Morning Ishan,
It feels great to finally be back in your inboxes after a six-month maternity break.
I’m a newly-minted mom to a spirited baby girl, and I’ve spent the last half-year only passively absorbing fintech news. But on 12 April, my daughter and I became unwitting participants in a UPI disruption.
I was getting my daughter’s passport photos done, and for once, even the photo gods were smiling. Within two attempts, we had a picture that her future 15-year-old self would no doubt approve of.
But it seems the UPI gods (read the National Payments Corporation of India) had other plans.
When I whipped out my phone with all the seasoned muscle memory of a veteran UPI user and scanned the QR code, the payment failed.
Huh. Okay.
Maybe my bank was down. It had happened before. So I tried another payment app, but that was also down.
My fintech training reminded me to try my bank’s own UPI app. But—you guessed it—it was down too.
Maybe the problem was with the studio’s QR code? I asked for the shopkeeper’s personal number and tried to send a payment, but… no luck. By now, my infant was well and truly annoyed with my persistence. And to no one’s surprise, she won. I left the studio without the photos, cursing myself all the way back home for not bringing my wallet.
People becoming entirely comfortable with not carrying a wallet has to be the biggest win for UPI—a reflection of the faith users like me have in the system. But the recent outage also reminded me of another, less comforting, fact.
I had been putting all my faith in a near-monopoly.
Join The Ken’s live careers event ft. Razorpay’s Harshil Mathur, Inmobi’s Vasuta Agarwal, and IIMB’s Prof Sourav MukherjiThe career ladder is gradually disappearing as roles get eliminated, hierarchies get flattened, and work gets automated with AI. So how should we rethink careers in an age of rapid change and uncertainty? Join us in Bengaluru on Monday, 21 April, for an interactive, insightful, and stimulating discussion. |
My daughter and I are hardly the only ones to be affected by an unexpected UPI outage in recent times. In fact, this was the fourth disruption for UPI in just three weeks. On 12 April, its payment success rate was just 50–80% for a span of about five hours.
UPI’s mothership NPCI told banks and payment apps that the root cause of the outage was a flooding of its systems with “check transaction” calls.
Essentially, every time a user attempts a transaction, irrespective of whether it succeeds or fails, a “check transaction” call is triggered. This is to help the sender’s and receiver’s banks communicate and check and resolve any payment issues.
And the behaviour I was exhibiting along with hundreds of others—repeatedly trying to make payments—was only making things worse.
As a payment executive I spoke to explained, every time a user enters their pin, a transaction is submitted to NPCI by the payment app, which then keeps checking on the status of the transaction every 3–5 seconds. Due to the very nature of the system’s design, for every UPI transaction attempted right now, there are at least 3X more “check transaction” requests. If one billion transactions are attempted in a day, whether successful or not, it results in 3–5 billion check transaction requests on average.
This may have ended up exacerbating an already stressed system.
This way, even a small initial outage can cause a pileup of check transaction requests, which only amplifies the problem.
But here is the thing. NPCI has bigger problems if its system failed because it could not handle the inflow of check transaction calls. As another payments executive said: “Check transaction calls are designed to be in massive volumes because they are read-only messages. It should not cause any strain in the systems.”
The solution that NPCI proposes in the root-cause analysis it shared with banks and payment apps is the imposition of “rate limits”.
Going forward, the organisation plans to enforce stricter rate-limiters and reiterate API usage guidelines to all PSP banks. Rate limiters are technical controls that cap how frequently banks can make API requests to the UPI system to prevent overload.
NPCI attributes UPI outage to excessive API calls; plans preventive measures, [Economic Times](https://economictimes.indiatimes.com/tech/technology/npci-attributes-upi-outage-to-excessive-api-calls-plans-preventive-measures/articleshow/120316821.cms?from=mdr)
Rate limits, as the name suggests, will cap the number of requests NPCI receives from each payment app as a way to manage the volumes. But that also means that transaction status checks will fail, according to the first payments expert. Which, to the end user, feels pretty much the same as an outage.
So NPCI has its work cut out.
But regardless of whether it manages to overcome its current difficulties (infrastructure is just one of them, as [we wrote earlier](https://the-ken.com/story/upi-can-be-forever-or-free-not-both/) this month), these recent outages only remind us about what happens when monopolies take over. Which is particularly ironic, because the NPCI has reminded us time and time again about how it does not want monopolies in the UPI ecosystem.
Since 2022, NPCI has [said](https://economictimes.indiatimes.com/tech/technology/npci-extends-upi-volume-cap-timeline-by-2-more-years/articleshow/116829131.cms?from=mdr) it will impose a 30% market share cap on Phonepe—the UPI market leader—but has never been able to do it. All we’ve seen is extension after extension.
At least when it comes to payments apps, UPI users have a variety of other options, including new entrants such as Super.money and Kiwi.
But what about UPI itself?
Who is worried about its 80%-plus market share of digital payments in India? What happens when NPCI’s system itself faces trouble, like we’ve seen happen recently?
To be fair, NPCI may say such instances are a one off. Its track record of 100% uptime for all of last year is strong evidence for its claims. But in payments, the service levels expected are 99.999999%. And as the payment executive noted, any system runs smoothly only up to a certain capacity.
When it reaches full capacity and you don’t have other systems to take the load, things will break.
Has UPI reached that point with the 600 million transactions it does in a day?
That’s a wrap for this week. Please write to [kaching@the-ken.com](mailto:kaching@the-ken.com) with your thoughts and suggestions.
Regards,
Arundhati Ramanathan