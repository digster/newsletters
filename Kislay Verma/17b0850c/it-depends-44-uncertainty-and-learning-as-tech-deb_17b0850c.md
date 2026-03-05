---
subject: "It Depends #44: Uncertainty and learning as tech debt"
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2021-08-01 05:34:15
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_7563788208856972919"]
---
|
Hello everyone!
Welcome to the 44th edition of It Depends. Hope you are all doing well.
First up, a HUUGE shoutout to Ms. Nimmi Bandaru who is now supporting this newsletter on [Patreon](https://daijdhg.r.af.d.sendibt2.com/tr/cl/boobeCHxiS-pT7C9q7sx6OQDZpNpbzJH1Vp7hO8GCOs1Qt-0u8R1byM8CrPFrX_RDtBZfBZvv59un63rXwLqQ96QtmOfhKqqO_w-D-yJjM6h4uDnM-Fpsa_h9Cc8q0QJUWvlxcqIqwD1L9nr23fuE_rZh-1Die08V3J_Q26lHFxL7WQQWd2LJEFGjQ1RQknvEYjUgG61Pb8M7EQg6US89-rYdWlPorS9M1Wdyovdt53mxEYIahmRY8OwiYeLiLYt8lzTHqIAW7XagsfGD7wgQd2TaHY_PoUBIyMnCM1tFHH7Pk0G73uX9rmie6iUzVwrtntDETuWIGQy1uFByWz4x_o_UDrnP3E0PYj6fcgKmRscu8VQAAhcTvCCWvI) (only my second patron). Thank you Nimmi, this means a lot for a newbie like me - hope I can continue writing what you like to read.
Today, we are discussing tech debt, and then the usual best of the internet for your learning pleasure.
Uncertainty and Learning as Tech Debt
Tech debt represents an accumulation of conscious or subconscious decisions which can now be identified as bad decisions. Basically, a shoddy job that makes taking the next steps harder. The more tech debt you have, [the harder you have to work to make new changes](https://daijdhg.r.af.d.sendibt2.com/tr/cl/8_mhJzM-8NdrhgjccZ6vmdKXYILMkXMjrm6chudUdfUGnBBzNmckrRjRDhISf1JXeibLjS-enVbtxFhBxU4HXGWEKQ8rNKGQrPblOBkI5XB3OgtYMEXlI9Z3ptINocvS1mQINbasrcXVBon-HrLYAT2tvE7wvULsC1ye8TvboKJL1VlRRC39YI1kTq9sTWU33Lia_V-Wp4t5nC-o3qa4xZqrQxKG0kneJgiZMTIekf1CnF8vhfYbwsm8vWR8gOhw9ujCicV6cw2KGo3yfcFJMByVLbzVAc5UZ9UblkrgxgQjoJgzNtyiUcBK01XehOvJfXMm69hewKjflk_JWvJKcd2SmiGOX7PqPMDBvJi63iddL8qNK2kp14a1gSNG1ydcdVVU6xef09KV2NBikMe0WGripzU).
My approach to system architecture and evolution is via continuous learning and improvement. I believe that all things change all the time. So all parts of a system will carry tech debt some time or the other. The developer team’s job is to continuously identify these parts, prioritize the critical deficiencies which are blocking the way forward, and consciously deepen their understanding of the system by taking on controlled tech debt if required.
This article is just a few observations about this phenomenon, mostly focussed on change and uncertainty.
Every decision is tech debt in the making
-
The reason we see so much tech debt, even in good teams and organizations, is usually not because of bad decisions. Decisions were probably good when they were made, but the world keeps changing. Parts of even good decisions will end up being tech debt at some point in the future.
-
No one designs bad systems deliberately. If a decision looks bad today, it does not matter why it was taken. Maybe the team didn’t know any better, or the world changed on them. The outcome is the same either way – we need to do something about the situation.
-
The ideal architecture is only ideal at a point in time. Perhaps not even then because there are almost always things we do not know that might lead us to design our systems differently (Conway’s Law).
Tech debt is great when taken deliberately
-
A lot of discussion around technical debt is only about technology quality. It does not talk about learning.
-
Deliberately taking on tech debt allows us to learn faster by shipping faster.
-
The problem is that we forget that we made the feature as a learning step. The context of that deliberate decision is lost. So when the next iteration comes around, the decision looks like a bad decision rather than a feature in process of growing. Too often, engineers think on the lines of “we built it badly and need to fix it” and not like “which part of this system should be evolved next”.
-
The more we remember as a team, the more we can think of tech debt in terms of WIP features rather than an already finished piece that was designed badly.
The location of tech debt matters
Tech debt is a balance
-
The trade-off isn’t between speed and quality. The tradeoff is learning and executing on that learning in the long run.
-
I wrote earlier about [ditching the urgency](https://daijdhg.r.af.d.sendibt2.com/tr/cl/VDru0CcQUlkTh4fjtrhMCHgE-74fIYMSYB45trQWWqYuZxkMlL0Cy696L0nYQV-Xlt7G3VGiVIOrIBwOgIb-Cz1AxOpYVr0_Ul47TQAiUN6vpKGJzXVg0OAgMhfzHIqKfP-UsSbsu1UyF3nPC1dOGOgozGgAzCUNM3IAoQ_nzBnfnsLZj5_tfamU7eSUt2ylhIGsgKtQ5gc9zA5z_9L-UrHUMdsfWZ5FeLRm0jGjIohp6Ws-jZ5KhmtP2V9Ltt_5zw31RdPKVhYe7st_zj8LeOoQOXjxsENJCEvv9Z2yRMSyS01BKjjke1IPqSa5I0yTmZjAcbgjIeE9JujGeXRep_DhVA7qELlTaZG32e0Wn0BZ9HEQ) to execute in the learning phase. This is where it is okay to take on tech debt. Build something small and fast to see what the users do with it.
-
Now while the user feedback is coming in and we are trying to understand it, [clean up the most undesirable of the bad decisions](https://daijdhg.r.af.d.sendibt2.com/tr/cl/Mq-l6cicp_Ci4z0NOywpfX8vBI-cSFN1nf79RDrmkmdnJ1KPLKJnI12G4IKdvEtnOqYRfbS1SyQcO0tQjE4quNEhst2iszJkZUqdqkt5HTJCkUH7RImuF0gHrMAnaa01wN_HegQVLb1Izt7ecKIoGgUd0QTZeI0sV90u90EJXLESNxQwiRUZlk0WvJVcMDgBbWG7qhGU1mqxud6IpgCy2Q5ICxC4-MSSds9LDhn-9GqPMbUhreepn1Fe-vkZ9yPJudu2YK-63bM7zK8iodJOAQKgjoFdz86xA1QgpmSBoHD4h3Bo11R-7nruOx28o-I2O42891Y0LoJDp4uNeucg1RT8dsKYXTa8qbvHgAVTmV7KwffumkXYMQm9xW02puCCUpgjxP5vRzVrwp_beQ9qR3umD0wYx2DtffYjlDg023yspjYguPgDQg) you have in the system.
-
BOTH THE ABOVE STEPS ARE CRITICAL. It is inevitable that we will go back and forth to some extent.
The origins of tech debt are important
-
I mentioned earlier in this article that why we have a bad decision right now doesn’t matter. What matters is to fix it. This is true from an operational perspective but not from a growth perspective.
-
For the engineering team, identifying the origin of the tech debt is a critical part of the learning process.
-
Looking back on their decisions, can they identify the bad decisions that they then thought were good? What led to those decisions? This will typically reveal some sort of information gap – not having enough technical skill, not having enough knowledge about the product or the customer, not understanding the direction of the organization etc.
-
These gaps can then be filled actively.
-
This is hard because teams are biased against their former selves due to the new knowledge they have gained since a decision was made.
From the internet
-
This article from Cloudflare describes [what edge computing is and isn't](https://daijdhg.r.af.d.sendibt2.com/tr/cl/RfEJK6bJJUvad7jp0YT2dsAde5uouqv5rRdIglGPxcWMoXivRW7GvnhICqJSQgdk5lsLd3deqc9bTXUKLjpewhg2d8_2sUVUoBJo6Q0reTt_jqkyzkNMwcUiiASauYY0Fd0GeJyjABPbrz3ZueRcJl21z5KvWTLMc5eyQuQMe5_U35r42LYmdqDLshOArthj04hvEY8rj0AavLRrOW5L9yZgy-fz3exq0Rh60-et_9Hc4Qm-tQgFrNWv9MxFTRfhcGR8pWh13jF9GKy2YFCeMAzMsB1Rsl1MFORJtn96HbAgS0XgPfMgN9IwLrD6aW25jAh6JIrRx70Jyw9bTljQdB-Ur_8unzTTWSM6ttfM3e3ISBa9LkI2cmECObmsQv4fK5UnciBFmrM). Cloudflare is doing some superb work in this field and yours truly is trying to make a blog on the technology happen soon. Stay tuned!
-
Larry Sanger explains [what decentralization requires](https://daijdhg.r.af.d.sendibt2.com/tr/cl/rYAUtq7h_GpOcVqFjnP2vgSh_K36PA7bMQiS-tMh7w08RA-C7NEvEsDabk-mIlWRpXw70TEVQix0OqjI862GnbZ5bedHelzzrbMH5RcdmeyvXpvmmgcpuSpuTmm2hnQJ2yDOq4mNr-wRCAH4qSQC4_lzAbHpibIlr2Arte1_9jBbyqiVun0cavKSuDgt2jGRPMha1PvygJphvrafstOin6s9do6hPbv3c_AigUlPjOLwu4azd-bngnZEaIbfSzn6I7MgzicThnEwrToLQKe3iwc4e5EydRHUMPx-mohO9G2KMMs4TZHjTV-gOTLG_-lJyBya1DDascA6eoSjXuNQB0WOi0XDjBnUiuHKeEmeuoAPzTeF7ZdvBsRhCQODPwlORgpwxqfRXXU) to work out in the wild.
-
James Urquhart discusses some [critical elements of Flow architecture](https://daijdhg.r.af.d.sendibt2.com/tr/cl/0mIKwcgrITKhThUc8WevxdGn4TUVofqOvc3VXo_BkeYAivzepqtK17d4QBAS3Y5zTwRCk5G6ewojlxpAx-2-P-4VR7y6gA0brX_F7Bby9ajImUFIG_qyOjGF9N2EqHG-aYDo_fZNhOB21HwXHrDC1pDDZQN6ptm9F2d28qHXnZC-DCZNqsHTSuPqXFoXzUb3IWsDD_iPoCc92-CkBFLpgDRDTe-lp25_nzljdsFbpDi4IVpk99BF1BmAMq0zf-HcuqACj4VR8mbS5AyZgC1dFFjtUuvmRHx0heKHbL21fi98XvmEE0I774zfJyawXk3Qu2bRbjKPe4iuYOrAzsiKJXSYUJeualIxHJvmk8nAzsUNU2XdQlmxTGjYSuAQCXH6Z4qG7TXxtYYmELUcS2arHI7hwx_y8QeE9AFiurpJSB9QAzNf).
-
I know this [Dan North article on testing](https://daijdhg.r.af.d.sendibt2.com/tr/cl/qw0cX8W_XUJ5EWKuFU3t-qIDnZI2X4q3zSb5O6ElpCucePsOOpRbrmNHJ1hIzXVpui-0Ji7SLZN001g4_crCQOtcwyaBuOgD2xDgxbW-RbGCa6pWlXvzctgJOLa_rQe6NHo6jF33Gv_0nB_5LQKBSWXxQMduSo9SOGY06eTPK2b4Bc6YlKa0YFdGm24WVMM7gittUQZTXLsm1245tmHjzeuPoDRgob5ISJ6HPo6ngCu23xWbf15aH_WQzj_QwijXUkH0vKO3sF_v-3c7h3XimGvGYVwd75ZHxlJ-yIpQyBrDgyTclTCKUvydlyZ20ufVHiQLxMfW2Z9VudQZH6b1KDVNJg3Or9LGD_F6zSW5DXi6VizuLi6x3BxPsmOIhwldijMCokNw1Qvm6ZOr) is on every curated tech newsletter right now, but I had to include it because it is just that good.
That’s all for this week folks. Have a great weekend!
-Kislay |