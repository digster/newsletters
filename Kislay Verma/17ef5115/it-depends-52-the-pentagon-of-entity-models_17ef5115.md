---
subject: "It Depends #52: The Pentagon of Entity Models"
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2022-02-12 07:03:04
labels: ["CATEGORY_PERSONAL", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_7563788208856972919"]
---
|
Hello Everyone!
Welcome to the 52nd episode of It Depends. Hope you are all doing well. This week, I look at an interesting pattern of system evolution and then share the best of the internet as usual.
The pentagon of entity modelling
You can read [the original article](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/VHaUsekGL0smJMGVGfog0R4tY6T4gDv0nkHYw95pl1sqLMAqzFOcyFfZAd-225rbiBfEJOeoV3OzSwyeXDr2qNAeGUcF-BsocODLzWV58o_b79UVC8ihqE35kJNtAOuMbGFU2ZMSEKTcAwKFeyXUcJjzuF5ryp7qz5UQPMuaEXmXh7QHED8gnXVeGuVQyA-UV5AeaTKOz_K_0LMcxwNKLwepva0bQeknjW-e8IsW9bREMVHQKS1oQBWgDeQZ41CJ7rA8tOiHU3RzArCYIJaJDGmW6CxLXRwNyLG94muQxDOpOHNt54pUMvt-6Of7K1dsxeXt76WctIcfC2qc1dZOLC_DBwX_MWmIbljbSvIKgkdClN9sJPU4MSbXP7EtDbZi76ZIjNYsv4O_-5saMtsN3gU6DbvfiSSvqYqiwISANxEuuqeDm3x6uSa0oey5yyHeaIxrGXC7rYcFXiE8GQ) directly on the blog.
I recently read an article by Matt Ricard about the "[Heptagon of Configuration](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/HbExEmwfzL-mHFM1C9SBfnHM1M8NcqMgoLpMjpOo0e0taMOSxkjE2gUqnKIj01MxoV9zXCrLT2LJ3ukIdt74CSR-Xl2blckLa-7YYJWHl9VtdIYjH8jABLhpFAPW9xT4JT_JQ5oec_zS0WvXQDwsmEGU1xEnvjERA01tzcDa_3jM72tDUnoigPmEySKbwkDmHTW4tyQwpYS_9OBbtvjfQUbzjXrUjOTkStGP_5-08ntXDDREHB-SDFXrXtqVHyu26Te-8q9mvaDIu1D7pC4V5EqwdGZQcG9nAB-9Zko8F8_tPTIMZ4IP7x_10IEHnFUthy6g1UUj1V0elyisSpMuex3_BuqNgjRUERxySr6lyjWJg7OAZwMe2Z3kEixpEJsPfXQ6n2-fu-22TIn4ZWHQ4uw)" in which he discussed how configurations evolve in a cycle.
It struck me that there's another thing that follows a similar routine - entity attributes. Entity attributes often grow into entities in their own right.
The entity evolution cycle
This is the transition as I've seen it go in my experience.
-
Some new, urgently required properties of an entity are modelled as a hack in a configuration somewhere.
-
This configuration is then pulled into the entity's main data mode, typically as a boolean attribute.
-
Boolean attributes evolve into named/enumerated types, sometimes with more associated data.
-
Enumerated types become full-fledged entities linked to their previous host entity
-
Entities evolve into complete business domains with their systems, process, almost organizations.
Why?
This iterative process happens because as we explore more use-cases, a more and more complex domain model emerges. The pentagon of entity model evolution is just a sign of developers continuously trying to keep up with a deeper understanding of the business but not yet knowing enough to model its nuances fully.
[I interpret technical debt similarly](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/DJSzowpta98bHBJ5xbX1QIJhjbrKR-o5WnW55yPBNS3JfokSaRFbntQ3YGYG6ZBXRWU6JhloV2B_46FDUjB1e7oRjnVnoe4by9y4X6bobAmBJPv1Fn05S9cy0uJrFFO4-tIhglWmycMfAA2ABezvoafrCfcemZZBTaKG7rG4dVYWxTf2piFfOO-oAJLqIvoyyiQyiRBoiH3TvEALSFYlTaFw_VbCtB1-PG59PDNXZ85fcYWjZQKAORUwH9_iZkNdzW9D4vfUDfEWLhJXHLukTUuMo_x8PdXjFB3dvjhgXrrnVn5mJiPt3bqgVWTBAO7iSKjNhrliww9lhuanoWLJ-Trn8fQB8wluLl1d2apDArhP5hhUunLYwvzcSgJ8ioM9jLMDQIFxmMnejkAgBiDHdY3glfOw8diDPDRCaBUx1sS-CBRwe9M555BEWr6WVLq0yboEJGc) - as wisdom in hindsight. The system's implementation is essentially just catching up with the developer's understanding of the problem domain.
This is a perfectly safe, natural way for systems to evolve. But if you want to crank the wheel a little faster, the only way to move fast but stay on track is to [spend more time understanding the business domain](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/dk-mUVWpz2uUk6qL9UPKVefkHqZcV6_zkEDsn9loDzwfxhCu7rNIiWTv8HzmJaIij-4GMJplpha8yYjgiGQECOb3ti5onXBsH7OS9L0Sp3K74dA76xGNZryrH9Dd6fi8eCSlMvDT0B61xa1kumHeerK2kcVIPhkPD5xYDLug2BQadxLSLkIvupsoQ5HV_TEmzTLO5kzVsl5KhbLr-PM-739lYXLBzBvaOHFYG8utPWB6wFBnNTqPJ__996-qlpqYGzFZfq_AXvFq5Nwd3oPTFovj9uWE-IhE1Y8LFZ1raZQqenBz3dg7V_MoHRM0dizmBTEx6mJuSvyAyOdH1A9RJIZOatPwVyDXPt7aY28vOp-wEiOM79SiDUw7vRuyFvw-bFUmi2gT8NmNySy4FFq5hTamBCss8DwBi_FiickbEaQCf3Skp5kM6Z43m7IOF-BPt0AmMwC2SfYHrzrqRQpAxAmWARNl) upfront. Understanding the domain better can help us predict future needs and build the necessary extensibility, if not the actual capabilities in our designs right away.
From the internet
-
For me, [this article/talk by David Rosenthal](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/eHxpTUBL3UgHUmDb0qqHSnh4tSepoQd8Jt8233xNiCfXcFqNCvg4WonEjsayVxfh1agJKEq4pm3JvBu56rMwuYIjykZIGygkWK0yvLd9cSEdoF83Ad09A9lmWabKCjumXjw33-UQFaW3cFMiYW_zNaxznR-sYT52Wv5y3ythyvr3oHVViX_ILtFjzwjXL1YS51neKMIGECVVaRMP9Ow3oifSdZSAQVqEIdepSRjadsGjRItTPMv-HaJkHhHlF9-PB0vAt8K4_b5e3J08MXzd62ukZIpfQon3Ww2GrvzxfeXiyga8HmQulKWkEtEIGJu578cVyKa1hum-sPW-1lTkYkl_fI_NC7pnqaADv52Fjnbz8MwfMavzBb_9OhrHJjDkQ4JqdrYra0P8L3YWhOe6k4jRWeWpI-PRJ5Qxeto) is the last word in debunking the utter bullshit of the crypto-blockchain ecosystem. It is a technical, meticulous, and brutal takedown of the so-called decentralization of Blockchains.
-
Brian Footer and Joseph Yoder of the University of Illinois (UC) have written a paper on the [architectural pattern known as “big ball of mud”](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/ipFL7ixfUslDOwg0LHUp9C-resX1iTtFxMhWH1GXrvZLR8nNsDaWrSHI6w8fYWqkeFLAOFG654zreVv1EKl-5U6CjLfY9X2cXjwUwtei_us9jNPVlZSAndD4t70bUkaqqa21CnbVQrIAyfeVdCb2E2oYZkKRUpxFAz2n2zlv5iXH9T0ihFdL-yv6UAiFZuYTtBDMtqj9BdwuQeA2mqYIirtNED00Pht4m7YFFei572yN5CbECmed04T6J-o252ZkT3ICoTBg_vlCv8gmLiJEo37h-RqnFAHtXqNWXEirPZYlbXAj54xIKYVIMmhgHUtw0J_ASGo3wVe2KlL2tQ27uYVvO0Xmiu3Xx5cr5a_gyJid). Odd as it may seem, it proves that everything can have pros and cons if you look objectively enough.
-
[Efe Karakus](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/hlTuiJqTdIsYqIIupxfJHYZXyJp43LyBc-h88H0GohNYN2z5h9mEG88QmRclUsdri_A64bSSD7AHbLps6l0Sw9HSr17FqWS8SZDQ89MHtfuv-csU-RGx7zZ7dw4daxH05A0d9XEVJ4umr3aiM65fev0xvcadLDL8QSxe5F0ZvUmLn19auXUQOHt1jHNJXPB582WWO-_FXV4loQCncFQSyDBOZeeNOS69fX8gpYphwPsd7r1zaWel4A1EIojqEA-EQnfWSgHoBQOCzc87e9GyzmWf0WSTc_aizHtiHKo0_LV4sMKk9FX4_4Uqr-YhvUEwE7ha4Vrw7KMQLiXz9izBt03rL10brR7futx1VoVHJMxsPtA6fn3YdwmivCsIj9otxj3bBBnLGfi0tRrACwoqzReAbbZpd60I6w) wrote this fantastic Twitter thread on [building client-side platforms](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/JmwqGnOSGpIusPHkbFRp3KR2VUzKcGjLP1Y4U6AiIC8AgHAmPnVrghF5kxBDUT7F4diI6J0KFOima89EFDLs6l4WZUZe_7oIErMAD_AmWC2Ia5BEqTmoqcwjfAHfE1bkTYSeEeNlo9VG0v37g9YdiDMPIZiNnzirVyN6a7p_ScVz-Qaky0kMOslwkv7DMDUC4Zu-QZu3jVHXoi3-O-Eby6fP7IODcGfVe35VdLKC3-xQurpsMRtxyU00PJtWLqFib3-iXpUVkemmwQUb7mogweGBPtFOL8mTBl92ZFcNvuim0KsNYLyoUjK7qp5wYELc68X55domAE7oNXSJn-TufLFtFAslQw0KVTdWSxpdEbNMGIB6kgM76mSMv9ElqcreqA8_3M4kA4ylEapHkFBhqmD5Q-QIvUFqxw).
That’s all for this week folks. Have a great weekend.
-Kislay |