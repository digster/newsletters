---
subject: "It Depends #43: Book review and Highlights from \"Accelerate\""
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2021-07-24 06:51:11
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_7563788208856972919"]
---
|
Hello Everyone!
Welcome to the 43rd edition of It Depends. Hope you are all doing well. Today I will try to save some time for you folks by sharing the highlight of my reading of “Accelerate” by Nicole Forsgren, Jez Humble, and Gene Kim. And then on to the best of the internet!
Highlights from “Accelerate”
Accelerate has consistently been described as one of the best books when it comes to DevOps and building technical agility in organizations. I finally got around to reading it and it was every bit as good as I had expected it to be.
The book essentially presents the conclusions of a multi-year research program and contains a whole section on why certain research methods were chosen over others. I have been reading and writing a fair bit about [agility](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/WIl6fZZ_NwHr7Jkb01YisGUvwuynD3ZSk9itXR3PvAORy-PKn1uEE-JT-As5Ha8NPY8HmbxJeKmf5Cu57Zr7ACFA_GW8krlRn5l_7WyJPUcsrUUuTp4ydAwf7SSvz8W-Y2fZ09QQbde2tSYUWdkI30ImInDK52NnszwRSgn9BWKlqIbAz9C1TeRCsYL8nh4BfxQGer8jBjAv_GdeArrQuLJ4s2v0cEJhybjMO2e7L5xl282MbU0UzDOYYx69HIHkk67zszB1Skg8VlmH64iiD8NYtLrdzrCEDzf6qOiKNMmSFiUYFVxruoByVtholPnAnSSa68gbIHeqb0z8tlcoWhPs5g0) and [moving fast](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/E-9wpOqr6T6nro3wvUoO-r8I-V4_xer_0XQX-08VA2fMqhLFLdj-BMr4ovf-DWI8oaziTZfz8rlhmIo-oMkrSul2YPm_aLoNcp7W6zWeX18yvch5gScZxs8hcjUIU9Icar415_PrnK1mrFuzy0vctLTPMUKWNlFn-7GOv5p3Cw4vIb669_JzIVLtJQml_QCShIPLF2c8ZFywo4naQmhD9uTipFmo5GN2F5xGvG4QaeK_yohrnACy9g3ZJQOslF7kwKs0PMa0wCYn_glM9rRQA_Z5D6Xaq5zRFHIBG6DDeaDo1gfFRJ9XPMR4NzuBlWHiw1tnQyD_klDIKSHzFo7BLl84oTJEpPumtdE6PP56zl_vkC-xCUjxy2AI3XWhXwV3ow_30iYUqNDkOrqVWoDD9sLFdadiRDObTBWP5003pU8pTogW5opeSUn2e7hqML9Iu9kA4toRdPk), so most of the things in the book were not new, but the solid research backing it means that “CI/CD is a must-have” is not just an opinion anymore. The authors have shown it to be a demonstrable trait of successful teams in the wider industry.
Accelerate is a short-ish read, but it is dense with information. I am sharing my highlights from it below so that you can get a taste of what the book is like. If you like these semi-organized snippets, you should definitely read the book.
Preface
improvements in software delivery are possible for every team and in every company, as long as leadership provides consistent support — including time, actions, and resources — demonstrating a true commitment to improvement, and as long as team members commit themselves to the work.
Chapter 1 – Accelerate
-
Small teams that work in short cycles and measure feedback from users to build products and services that delight their customers and rapidly deliver value to their organizations.
-
[DevOps](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/sO58bv_hUCUo878Dh2MXeHxZy8J4kWT1DyioEFRe9MgMLUMSNoEgCTbfbIllpt-XWlv1Pdxwo9RbUSFHx5TPciPBm9g0b5Kpk1mBNtyk9I18DmZUoWle2zKkXi8M7CHpLNWEKFiKSaFFO39bAmzfBGwwA2beHkX-hNNX17mS1bahP0J2dqg4GE9YrcviV7iTzq1_cDdNrtKpsQEQk-x7bUcTiYarcFtvm_sSqI6ah6WIpc9HxlocYA3-v75zMj_Li8IdkWXD1FE4d1wZaMfHznGuF22WJhW8lV6CIWTQdfwvgeiX-K6X3wHwZs1rdQ4LH6MDTqBHvTFIwzVlXTZXaSkgu99h3yuf) emerged from a small number of organizations facing a wicked problem: how to build secure, resilient, rapidly evolving distributed systems at scale.
-
The Forrester report states that DevOps is accelerating technology, but that organizations often overestimate their progress (Klavens et al. 2017). Furthermore, the report points out that executives are especially prone to overestimating their progress when compared to those who are actually doing the work.
-
The key to successful change is measuring and understanding the right things with a focus on capabilities — not on maturity.
-
Maturity models are not the appropriate tool to use or mindset to have. Instead, shifting to a capabilities model of measurement is essential for organizations wanting to accelerate software delivery.
-
Three reasons capability models are better than maturity models:
-
Maturity models focus on helping an organization “ arrive ” at a mature state and then declare themselves done. Capability models focus on helping an organization continually improve and progress, realizing that the technological and business landscape is ever-changing.
-
Maturity models are quite often a “lock-step” or linear formula, prescribing a similar set of technologies, tooling, or capabilities for every set of teams and organizations to progress through. Capability models are multidimensional and dynamic, allowing different parts of the organization to take a customized approach to improvement, and focus on capabilities that will give them the most benefit based on their current context.
-
Capability models focus on key outcomes and how the capabilities, or levers, drive improvement in those outcomes — that is, they are outcome-based. Most maturity models simply measure the technical proficiency or tooling install base in an organization without tying it to outcomes.
-
Maturity models define a static level of technological, process, and organizational abilities to achieve. In contrast, capability models allow for dynamically changing environments and allow teams and organizations to focus on developing the skills and capabilities needed to remain competitive.
Chapter 2 – Measuring Performance
-
Velocity, lines of code, and other typical technical measures focus on outputs rather than outcomes. Second, they focus on individual or local measures rather than [team or global ones](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/KXj3_ny1EMwsOABpaudf0XJYi8Tujp7hTe_gLIFm3xybenlwwbMjyZZGItL96c9pJ02G0ZW5j2NlCbYDG2z9UmHZkg5856I05zrQB7Qet-U_iZcy-ZoWLrhzPtyEKHDoFf60N4OIpEUQ9WuT5vmIZEfFjO_cz5YoGCr_qPg3PIg4N3cegoMB73L_8lN5aJsJ88ip1kXmCxvoPfQoxjj-p4znNQnS8zrf7jdSokApIONlUGGaGxy_prqJW0ACMjlvqEbkBkyEZG-7OnxZ2OAyFJqxRcllDijilo5hbiFmINuSDVv2b9K7tmYxQDO-dafKZQcRWTlgQnvp1JZxmdnfwQC7VZWb_uvsUOK-VnMn3cawCCG8YjVNAcFdJJNEx1DwcdxzNvXg55QM_PSAu-Ur-bwyb3WD1PaH2aAA8kpGTVtVjmtxXXAMcXDeOy_j0K4XDDASGw).
-
Ideally, we should reward developers for solving business problems with the minimum amount of code — and it’s even better if we can solve a problem without writing code at all or by deleting code (perhaps by a business process change).
-
A successful measure of performance should have two key characteristics. First, it should focus on a global outcome to ensure teams aren’t pitted against each other.
-
Second, our measure should focus on outcomes not output: it shouldn’t reward people for putting in large amounts of busywork that doesn’t actually help achieve organizational goals.
-
In our search for measures of delivery performance that meet these criteria, we settled on four:
-
Delivery lead time
-
Deployment frequency
-
Time to restore service
-
Change fail rate.
-
Lead time
-
This is the time it takes to go from a customer making a request to the request being satisfied.
-
There are two parts to lead time: the time it takes to design and validate a product or feature, and the time to deliver the feature to customers.
-
In the design part of the lead time, it’s often unclear when to start the clock, and often there is high variability.
-
However, the delivery part of the lead time — the time it takes for work to be implemented, tested, and delivered — is easier to measure and has a lower variability.
-
Deployment Frequency
-
Reducing batch size is another central element of the Lean paradigm.
-
We settled on deployment frequency as a proxy for batch size since it is easy to measure and typically has low variability. By “ deployment ” we mean a software deployment to production or to an app store.
-
Delivery lead times and deployment frequency are both measures of software delivery performance tempo. The key question becomes: How quickly can service be restored (if something goes wrong)?
-
A key metric when making changes to systems is what percentage of changes to production ( including, for example, software releases and infrastructure configuration changes ) fail. In the context of Lean, this is the same as percent complete and accurate for the product delivery process, and is a key quality metric.
-
The ability to take an experimental approach to product development is highly correlated with the technical practices that contribute to continuous delivery.
Chapter 3 – Measuring and Changing Culture
-
Organizational culture can exist at three levels in organizations: basic assumptions, values, and artifacts (Schein 1985).
-
Basic assumptions are formed over time as members of a group or organization make sense of relationships, events, and activities.
-
The second level of organizational culture are values, which are more “visible” to group members as these collective values and norms can be discussed and even debated by those who are aware of them.
-
The third level of organizational culture is the most visible and can be observed in artifacts. These artifacts can include written mission statements or creeds, technology, formal procedures, or even heroes and rituals.
-
Type of organization as defined by Ron Westrum- https://cloud.google.com/architecture/devops/devops-culture-westrum-organizational-culture
-
Culture enables information processing through three mechanisms.
-
First, in organizations with a generative culture, people collaborate more effectively and there is a higher level of trust both across the organization and up and down the hierarchy.
-
Culture emphasizes the mission, an emphasis that allows people involved to put aside their personal issues and also the departmental issues that are so evident in bureaucratic organizations. The mission is primary.
-
And third, generativity encourages a ‘level playing field’, in which hierarchy plays less of a role”.
-
We should emphasize that bureaucracy is not necessarily bad.
-
Westrum’s theory posits that organizations with better information flow function more effectively.
-
A good culture requires trust and cooperation between people across the organization, so it reflects the level of collaboration and trust inside the organization.
-
Better organizational culture can indicate higher-quality decision-making. In a team with this type of culture, not only is better information available for making decisions, but those decisions are more easily reversed.
-
Finally, teams with these cultural norms are likely to do a better job with their people, since problems are more rapidly discovered and addressed.
-
Failure in complex systems is, like other types of behavior in such systems, emergent (Perrow 2011).
-
Following the theory developed by the Lean and Agile movements, implementing the practices of these movements can have an effect on culture. You can act your way to a better culture by implementing these practices in technology organizations, just as you can in manufacturing.
Chapter 4 – Technical Practices
-
[Continuous delivery](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/nS1J5ePm1AaVNne9XCvqTUoN34ys0wOpbZ5CHHLkd1zo5ZekBETgB1UvrqQfUAf3oHxKH3Q2qGOfqeeMpY1Ekr7lFrM0PzsBqJGk9gDGW5gI8oy3ca8NH9xvoMhLDcXz8mP5lxx-WNb5HrHKu9kJ3HwYcXThWB33YqBbp10PSC_0wq9VBuLjoND5WRJVbSYyGJRVwT5e3W4pv5cSXz3bZljK-VLiT10fh7OG3VkbmE_zcAVavLStMeVD-5tN0a7PGwS8x-wB05JN-c61XleegpDa3vqAWLk-Gb6v5Da9u69jS_rFP2KMvBSjp5_CvyKvq9NpD_vqRaIZDBRJ_HOCYYgf5z4_Ns7S06Sj1SZVcJ3dw1sNTK7ahpzDGN0CKyKVYi-a6w6n8llRsKq8Lg24kLb6JtA) is a set of capabilities that enable us to get changes of all kinds into production or into the hands of users safely, quickly, and sustainably.
-
There are five key principles at the heart of continuous delivery:
-
Build quality in: “Cease dependence on inspection to achieve quality. Eliminate the need for inspection on a mass basis by building quality into the product in the first place ” (Deming 2000).
-
Work in small batches: By splitting work up into much smaller chunks that deliver measurable business outcomes quickly for a small part of our target market, we get essential feedback on the work we are doing so that we can course correct.
-
Computers perform repetitive tasks; people solve problems. One important strategy to reduce the cost of pushing out changes is to take repetitive work that takes a long time, such as regression testing and software deployments, and invest in simplifying and automating this work.
-
Relentlessly pursue continuous improvement.
-
Everyone is responsible
-
In order to implement continuous delivery, we must create the following foundations:
-
Comprehensive configuration management. It should be possible to provision our environments and build, test, and deploy our software in a fully automated fashion purely from information stored in version control.
-
Continuous integration (CI): high – performing teams keep branches short-lived ( less than one day’s work ) and integrate them into trunk/master frequently.
-
Continuous testing: Because testing is so essential, we should be doing it all the time as an integral part of the development process. Automated unit and acceptance tests should be run against every commit. No one should be saying they are “ done ” with any work until all relevant automated tests have been written and are passing.
-
By giving developers the tools to detect problems when they occur, the time and resources to invest in their development, and the authority to fix problems straight away, we create an environment where developers accept responsibility for global outcomes such as quality and stability.
-
We discovered nine key capabilities that drive continuous delivery.
-
The comprehensive use of version control is relatively uncontroversial.
-
Configuration is normally considered a secondary concern to application code in configuration management, but our research shows that this is a misconception.
-
[Test automation](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/1R-9mLdeqII9E4QWXo_9foGd8XANRHhmnjr0E4HT_-Hkml_NwYCLvZF9FVjrfS8kfvG-OlqhaFA1Vq5PIHNhi_lz9i483ohAVfoI0OMf2mEjf57vj7O5TNYjeqR8X9UnRmULoTLxA7PK9b_hjrnysyimzYzEmi8PRYwtKjWGyOb7fstXPbWnIwTwcjQaxO2YTQ55otbAMmyK8kZgZXSoRsSJxdS-xnb_hMKGaIZ3lWZuKhKiBUtikoLd4n9HgyO2b1EbUzItgr2Gtm1JTvMvICu77yJNKSpHIA6krj1eY478pFXYK67ebyMXVj0G8q-XzKHYTVusBWbdzsQUDjabg9aoYspUEDeov3KLThRV-xe_N3K3ErhsbU0Be4VQVUjyEV-tpcZzSmv6vHj8VvbcWw) is a key part of continuous delivery. Having automated tests that are reliable: when the automated tests pass, teams are confident that their software is releasable.
-
Developers primarily create and maintain acceptance tests, and they can easily reproduce and fix them on their development workstations. It’s interesting to note that having automated tests primarily created and maintained either by QA or an outsourced party is not correlated with IT performance.
-
Successful teams had adequate test data to run their fully automated test suites and could acquire test data for running automated tests on demand.
-
Our research also found that developing off trunk/master rather than on long-lived feature branches was correlated with higher delivery performance.
-
High-performing teams were more likely to incorporate information security into the delivery process. Their infosec personnel provided feedback at every step of the software delivery lifecycle, from design through demos to helping with test automation.
-
A critical obstacle to implementing continuous delivery is enterprise and application architecture.
Chapter 5 – Architecture
-
The architecture of your software and the services it depends on can be a significant barrier to increasing both the tempo and stability of the release process and the systems delivered.
-
We found that high performance is possible with all kinds of systems, provided that systems — and the teams that build and maintain them — are loosely coupled.
-
This reinforces the importance of focusing on the architectural characteristics, discussed below, rather than the implementation details of your architecture.
-
In teams that scored highly on architectural capabilities, little communication is required between delivery teams to get their work done, and the architecture of the system is designed to enable teams to test, deploy, and change their systems without dependencies on other teams.
-
Organizations should evolve their team and organizational structure to achieve the desired architecture.
-
The goal of a loosely coupled architecture is to ensure that the available communication bandwidth isn’t overwhelmed by fine-grained decision-making at the implementation level, so we can instead use that bandwidth for discussing higher-level shared goals and how to achieve them.
-
If we achieve a loosely coupled, well-encapsulated architecture with an organizational structure to match, two important things happen. First, we can achieve better delivery performance, increasing both tempo and stability while reducing the burnout and the pain of deployment. Second, we can substantially grow the size of our engineering organization and increase productivity linearly — or better than linearly — as we do so.
-
Architects should focus on engineers and outcomes, not tools or technologies.
Chapter 6 – Integrating Infosec into the Delivery Lifecycle
-
Infosec is a vitally important function in an era where threats are ubiquitous and ongoing. However, infosec teams are often poorly staffed and they are usually only involved at the end of the software delivery lifecycle when it is often painful and expensive to make changes necessary to improve security.
-
We found that when teams “shift left” on information security — that is, when they build it into the software delivery process instead of making it a separate phase that happens downstream of the development process — this positively impacts their ability to practice continuous delivery.
-
First, security reviews are conducted for all major features, and this review process is performed in such a way that it doesn’t slow down the development process.
Chapter 7 – Management Practices for Software
-
Limit work in progress (WIP), and use these limits to drive process improvement and increase throughput.
-
Create and maintain visual displays showing key quality and productivity metrics and the current status of work.
-
Use data from application performance and infrastructure monitoring tools to make business decisions on a daily basis.
-
WIP limits on their own do not strongly predict delivery performance. It’s only when they’re combined with the use of visual displays and have a feedback loop from production monitoring tools back to delivery teams or the business that we see a strong effect.
-
WIP limits are no good if they don’t lead to improvements that increase flow.
-
Implement a lightweight change management process.
-
We found that approval only for high-risk changes was not correlated with software delivery performance.
-
Approval by an external body ( such as a manager or CAB ) simply doesn’t work to increase the stability of production systems, measured by the time to restore service and change fail rate.
Chapter 8 – Product Development
-
The key to working in small batches is to have work decomposed into features that allow for rapid development, instead of complex features developed on branches and released infrequently.
-
The ability of teams to try out new ideas and create and update specifications during the development process, without requiring the approval of people outside the team, is an important factor in predicting organizational performance as measured in terms of profitability, productivity, and market share.
Chapter 9 – Making Work Sustainable
-
The technical practices that improve our ability to deliver software with both speed and stability also reduce the stress and anxiety associated with pushing code to production.
-
In order to reduce [deployment pain](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/1B_z1RogiswgXiYl1jvbf6_Gy3XlDsdYXr6CPOlKRve3-wRmt4jeeqF8Aug5WaMEGJvFvLqqqQBQzHpjhqZ8y-jeAJCa14mdfeTyYLK7IwfBkRZxYmPGHLbnzSZNGS4Nj2-nPhGScphYU6k4B9a6Cf1E-hZNUjKJFJGIebJbQMed-m7CwjgJj8Ewgf1RUywHN1CKSLOxkUTQUNmxTqQrUEF6ahPy56bhahTbDVpOmwdmQVUuOXUA0DOS_SRf-IMLK6n7cT9tsB_xUSW_-NgtXI-FOu56pxCKHBVMnxKDe79NwVKzTLbT1zWbXfetY__qb67DacftXXe37hv_sl5za7duDLHj0SeujU2dOwTp6ANmLYThx5d_5hrEPvUJhuQwkL06wN8gXKtCBnDrpRzsX6DGu9e8T0_Q), we should:
-
Build systems that are designed to be deployed easily into multiple environments, can detect and tolerate failures in their environments, and can have various components of the system updated independently.
-
Ensure that the state of production systems can be reproduced (with the exception of production data) in an automated fashion from information in version control.
-
Build intelligence into the application and the platform so that the deployment process can be as simple as possible.
-
Christina Maslach, a professor of psychology at the University of California at Berkeley and a pioneering researcher on job burnout, found six organizational risk factors that predict burnout (Leiter and Maslach 2008):
-
Work overload
-
Lack of control
-
Insufficient rewards
-
Breakdown of community
-
Absence of fairness
-
Value conflicts
Chapter 10 – Employee Satisfaction, Identity, and Engagement
-
Employees in high-performing teams were 2.2 times more likely to recommend their organization to a friend as a great place to work, and 1.8 times more likely to recommend their team to a friend.
-
We found that the employee Net Promoter Score was significantly correlated with the following constructs:
-
The extent to which the organization collects customer feedback and uses it to inform the design of products and features
-
The ability of teams to visualize and understand the flow of products or features through development all the way to the customer
-
The extent to which employees identify with their organization’s values
-
investments in continuous delivery and Lean management practices, which contribute to a stronger sense of identity, may very well help reduce burnout.
-
Being able to apply one’s judgment and experience to challenging problems is a big part of what makes people satisfied with their work.
Chapter 11 – Leaders and Managers
-
Being a leader doesn’t mean you have people reporting to you on an organizational chart — leadership is about inspiring and motivating those around you.
-
According to this model (Rafferty and Griffin 2004), the five characteristics of a transformational leader are:
-
Vision
-
Inspirational communication
-
Intellectual stimulation
-
Supportive leadership
-
Personal recognition
-
Transformational leadership means leaders inspiring and motivating followers to achieve higher performance by appealing to their values and sense of purpose, facilitating wide-scale organizational change.
-
A transformational leader’s influence is seen through their support of their teams ’ work, be that in technical practices or product management capabilities.
-
…leaders cannot achieve goals on their own.
-
As the real value of a leader or manager is manifest in how they amplify the work of their teams, perhaps the most valuable work they can do is growing and supporting a strong organizational culture among those they serve – their teams.
-
Enable cross-functional collaboration by:
-
Building trust with your counterparts on other teams.
-
Encouraging practitioners to move between departments.
-
Actively seeking, encouraging, and rewarding work that facilitates collaboration.
From the internet
- No stinkin’ webhooks for
[Anthony Accomazzo](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/6QUErlDtGYizbhxM87RnXpldbcbmFIPYwPu1yjRzB72cIpfl4hHixUW8XFCcZovF9e6ZYgfFebnJE7KVGXwGvF0_yf6K9szoDr3EpYbzwZ7mslkyHnAEljgNosFuF6OYXegz4_vh4zqo9fuv_0mBv8BJ1MWfAMEMw19ySUCXuwlbznlgT4jKcY4vwPEpadNRRN_v4ABXUguC1_fy95JrJJSEdx8mHcFKAANwaPWbqiGV3LqXOaIRrODOIjx6Jk2IGKGFiTwXs6kpicm93_xlLrLX81GQNeCOcJaScyfimC8r-Bw-CUITPhNAUSt14TT7q_ltfCzs7qCYXcDv3esWWw), [he wants them events](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/Ji-Q-JoszGfierFqjA0GOaOt1BhCo6aYwayYGkQ0B9NEJep7ScRAs79QUydLAPHy-yBgqmF1ibgwjwNeNoU3KVSA3i5EXOpgPI7kNITQLF-cgSlPKkxRU19RHn9KjWHbChs28NRZQOjwx4c5O_53016I2bOfUsclNyZZkbXSu6l05R2vqyDNZ3Tcgj5iH8D6sX5ZKlE_RBZsdQq8KlByxRmm-66Ywl_5ed4wu10glgR9nLjNOIbnZxIEaOdGqFS4iW9e0sk-j6EMrEJs4PsTDtj8yGxlBBtjvah7OBy8G0Ezgq2to1LHJNS7cuxiRLqMUKjPFge1Ujh-qy-TGctOdFH8w_1UgPTYfZlzyTSk17nIWBPeKyO-EQ)!
- Paul Graham explains
[how to write usefully](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/Lhpk48G0eFKBILd3S2YQEFo5qCqn-F90cfM48Eu_3XX4loKwiytKgQnhCmdHhI9vcCmmaZdmN6mMMvLKuTeWMmt1s_iiZrkVn26X5oFUxjTaWJlCFbtnjMOmKebirDcIexizQtTqON7fVik-jREtADjalYdRbWUBqG9NKpXaI6z4ypCT-4JeZXNIUEfJk8cXvjG7Hx1uwPX5NV-V8jfjdaL57H130oXHCaXEYjcESj_HzECBYZ02gsrsaVGo3weKVOugIWwBvu8mJw4H--zTZju7BHlfGaefnYkeKXe_2ffQeEDbKxmGaNVKmgBTTKmStqNoWaTOB1v6q8VsDNQ0WA).
- This Twitter thread gives a good introduction to how
[Ethereum can be used for implementing decentralized single sign-on](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/IuEp8hKejmXHMDHdwrsLizAgyzdwVxpZCsd6Cre3cKttO3W2lr82Z5x9UVI5108YqBG6s4AwXPGVo74HwVXNMDGE4u5bixwQxsM69a5wTw6LqZURXwpX5QvBnx7hrKt418CsRE4vEyqNyOc_umSY-rII-TFBVnkciv68mEXD0xeDZrBs8APArABaF070GYd40al5p2lYdFmaf_fqd-O2X9BtC3NuBbkmYDlg1ijLwplrlUBJHSOm7F96nyKRK4tNqMwIkccYtfE-a-xxkpYw4bcgcSTiSVaL55hniLv0aOTpfKhPGuPGUnCTKh83E5jsp_7TJGPozZ2JMzjQT18vm1egHuDMAGzIzgmElbgq9F0I0W1GCOZn5iJ-BLC3xbQbpu2YrwxL_NXOPouB).
[Thierry Du Paw](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/PsEWhL9I8bYQe-E67zUd6B_YHajbXP__hoWB1D5wp95yAgT_LbQCLVGZcrzS14VoL2Tudwjw6L78xWtn57GasF4aQiL3q6ZzRAT1g5jm76epHZhB5cy4GWKVB-V94W2e8nqsZGXFc_FbV6ivCBEW1gHuaAlaaolD1NvHb-HlVXukvMkoowSkrZYV0Dg0GRsTP4jSjZ8QBWZEAuFAp6Zo4eqEzn-Eb_6z0JRKr1Ugv7yUc3MC8BKEFCBftcmyjZLxiJi6rnAElJUGb6N2hCuVgoMYiP1CI1VY3GbwJtqXdfZuNSmYC5bO0vxSLJXumy_DjfGqHYN34XI6UDWZ) has collected [various interpretations of Conway’s Law](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/3GIEuKmw4U46z5_qcPQnFpnDTZf_4-qKnufeilLUxG8CtUF8dDUrPo4zj6InSQ_zt-7nFDtT-Mqr0D9r3qOgcTAvY-hl2GUTgsbUVl9Vq-e2X4xU4XA8u0mlrvhVTAkqUeh4_cllzNizuBNb8uHKsYfnTyB1_0CPJ0ZQ6DclRssjdULbdFLAKepP9jAdLo-eTbFPZRMVcnwCfGa4wIPwiy3MQbWDHi7dAhraWCX62M_6gB6MiPb2mjRB0wGpssu5Q0r66d2yePV2rG9yJ9nk6qkBQs499mabOxOF_0jdEo9ckOEbyRV9OhXZifo_m8pZsuhRcLUuTScCKatJnc4Qw61TVlIs-BnVfTMo_XZpR8qwmADT-P119X4e-vdMmMZ-TgUbjXPqe5_PNDmRlxux4yF7A9d_zjTSXzBXzA). All of these are fun to read, and neatly rabbit-hole into different aspects of socio-technical architecture.
That’s all for this week folks. Happy Weekend!
-Kislay |