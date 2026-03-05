---
subject: "It Depends #33: Flink, Start with why, Pace layer, Snowflake"
from: "Kislay Verma <kislay@kislayverma.com>"
to: ""
date: 2021-05-09 06:54:56
labels: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Kislay Verma"]
label_ids: ["CATEGORY_PERSONAL", "IMPORTANT", "INBOX", "Label_7563788208856972919"]
---
|
Hello everyone!
Welcome to the 33rd edition of It Depends. Hope you are all doing well and staying safe. If you haven’t got the vaccine yet, please do everything you can to get it. Best of luck to all of us!
No original writing on the blog this week, but here’s the handpicked best of what I found on the internet this week.
From the great interweb
- The Ververica team has a brief intro to
[how Apache Flink handles backpressure](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/1_KSBN85gV80m0vrj4IIm63zw3BcqPRsLGJJy2l_h2bR-f4H4pzkX-VnZbd1Ciu4VhRHoD3vP1o9Tw-6Pm1LUEmR28JRhUsU-BE-pVciMU-RIsOIaS-iXNfvbigDYzxyRbtRTBL3KRJENTMPYn2netaMXfC_AIyjnDs8RhC2HrjL3J_dRh-NmIfeUWPzz1y92j-6aLHp0TjwiIxF9Jn64AWNajSuT3TRgyD4EzRlZA0qbzdA7a950JGzRJNQUbY1vPgmcGiWGegVuTc_77DYKYrMcA3fPCx6nGfwYJzla6cNg5nP8CbiGLwPCBMT9Swn82ORAMO1KXdF8OoEmjfqAqpejWbmPycvIFKfZkoBujaeXToqdO5fcQ_Uwjw4Q9ioiHrmZJr8kqy7oo-1X59Viw). This makes for a nice follow-up to what I wrote about [visualizing distributed systems as computational pipelines](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/w9D4hcOYC-6D4OrGU2iU9J_rYRUrk5syWkqkOUFMTa1O7dnISWZV7EroBkZd_HqMv_FuK1RCpXxGFSdNUZVADRMwAgf21SNNwMOHl_CLBC1Dw7ZK9GpopgXvKhAbD7AHUotzRr4W9HGiuQHY-HiUHrrCFeSFRYi9BKhLlDtWJDi9dhX_2IsiX-6vWbqKCH7hg6fHw1yk0sIsu5phT8ccWreJguutl5C-m8GmIcMdx2P7NwjHfVGIQe1EJdKDzSI2VxA8CzNb4k_bp_biAcMWD1-cYD8RkbVsK_UC4O6FBSoOFjDEOAyvUJI-Jl4Du-gWQMSdFGEzCCDdLoiFAe6Xg1CkeMT-SNXryWrWrdkVONoElSgyX1mNK--r1La339pNXcLWlnno-4WQk9dPH33pc0E70Z3ZwLfsuQxsisn_YfBoPRure5r88srl2xcYbWtecU3Hsw6EHI6IyUadvI_qU9FCJyakCef8--tRpJpLFfXjfkDWaWzhY5qiXeR_Cgwv).
- Hat tip to Chris Patullo for sharing this
[short video](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/7qhFmIJKn1yhZUCYeq3kPoRf_9QqvDojtgPSIWbtZlmOn-egyqZMDHyl_9CFnya0_neBveF6zstVF9828oKTroHd8CzcjDDP4oqq3Ko84KV0jR5ZVlqemyx2GI8EvloCz3eDDKEEAYmQTqSmb1TAlT4LOmnfjy-D97ovZIsGllFVp4fS1zcoIEBrAWXxHxtD56Sobz25uyQb5UzDTFHLAvsO0nJMK-VWKTXBRoaeIQWSBdhgPq-ma5pVTbHaLoOUuqBYDJ-OC46CgxXpW3j4O3Ou6vmzuQ_U6D_zu3ZR4EDBuWL9ucby7BDfuWdYpaH1ySEt6MpSMvQy07i65eBSERNRoW1xUuDw5onCCdlsAk3lYT2VaeXzbQ) of Simon Sinek explaining why “starting with why” is a key element of success. There’s a whole rabbit hole behind those ~2 minutes, so happy exploring :)
- Architectures of buildings and software keep running into each other far too often for it to be a coincidence. Here’s Stewart Brand and Paul Saffo explaining how their “
[pace layer model](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/Yvs_LyrAj9sarCxf2we7iFaNKQA3hI3T0w4ajmt0Y9D7JYn_KMSRj27h68OrDRLDENKawEIj17ixjMmtYX127nre2CJhjTBsUuFBi8IFrvSPhOTAOYwZ7qgVVw3AxOP5rf-w98dyVTefxNJuo1P9h8-wryQ6atxjsCU1sL0rZ49XQ6qiBhdJUf7xmxLAS1N9PkiCdcuXlHbdgldiwawo1t-VP9e8jvpcFAHqYHZNvs0OmGW9DWVbyl5fyopkI8eqYMZwqnw2BUC_N5z8J5v27OFBbUbyGe6hLxvT0zJlYAIGFeg6F3SQ7tYE_ftzxV0j3-_6C0hUQuRrJZ1acoqqDPcwOt6ScHwLZZxevv1tI8YjOKVRKvfX9pJXFDhBuGLWJ4P_8uw3XPg)” for understanding the evolution of buildings has found widespread application in software engineering, complexity theory, and many other areas.
- For the more hardcore weekend reader, here’s a
[paper](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/A6p4xyfb4tlvyzdQ2lI69JhzObs__XfWEm1gONHF4G6TRyV2ItQOGwqYsxcSLgoHOMMo3KesZuXyv5GqECzq0c-Vtdz-Xv6N-iVJaNVlgY8r01S9Ew5BFYqg2hOhdDF7k2dk_VeCa_k0dfgCtXed9OSXTPFC30DZj9VIYDfBRqScn7904Ruz528Rsdv1JlfqCvjikBOHGNtCTzw69oEur3rguAi0dfNRjrayi50GwewaBGyXu97tHjPCSZp9YNJK-sJQbpDUIqgbB7zKG1AimtXa4Vz7_nuh34pYYYR33fMf_EOSLOENgj16lKyBBpy8vdj9R9lhO4cReAr-81KjI9h1j-JcUextnCzgAN7tyLgkgUONWsXatKNhYW0uSeDLed1Krhyc9GZKtG2MyZcgLs0ZdUQ) explaining the internal design of [Snowflake DB](https://daijdhg.r.bh.d.sendibt3.com/tr/cl/MJeK58OIzYNiGD_-xa-oJLRWhIeBXg5ieNvVZME4ku-8a2qSXvKHklizQhfvR7hEqWbN4R5t3kr22OJIh0i3mvLrwtg7MK9DW6HMDCWgtF5x5K5S78QUCNcKCavGeFad5DPT7vZd36uL3xyxoLYpV85wMPMNq3hqSp0mccN5C76cQ_u4kepBLVKIpUMR5d9gxQ9qge1ZkMM1snJP_xdTdi7cYwdEfFA9w9Y1Jbmw0pm9tLtE3tDyATTS72gO6fH7zuKf69VcZIWBNrKVRu_rhUGY7tL2qHf4VM3-9j_yggp-cXlu9uo2OwUcrTU5KgsfehZY643tUjs65OkY).
That's it for this week folks. Cheers!
-Kislay |