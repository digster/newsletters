---
id: "19fef9f87e872105"
subject: "How well does AI peer review work?"
from: "Marginal REVOLUTION <donotreply@wordpress.com>"
to: ""
date: 2026-08-11 07:00:36
labels: ["CATEGORY_PERSONAL", "INBOX", "Tyler Cowen", "UNREAD"]
label_ids: ["CATEGORY_PERSONAL", "INBOX", "Label_2466199532210586699", "UNREAD"]
---
Claude and I planted 100 known errors into 10 open-access psychology papers and then ran them through frontier models and two commercial AI review tools. In brief:
- The best single system caught 71 of 100 errors, while the worst caught 30.
- Pooling every system’s output caught 93 of 100. Models are only partly correlated in the errors they find, making ensembling a big lever for finding issues in papers. Check your papers against multiple models!
- Seven errors could not be caught by any system. All were omissions — information deleted from a paper rather than mistakes inserted into it.
- Refine.ink contributes more unique catches than any other single system, though it’s expensive.
- I didn’t measure false positives and I don’t know how this error distribution compares to the distribution of errors in real papers.
- I’ve made the papers, errors, model outputs, and the full experiment log
[public](https://marginalrevolution.com?action=user_content_redirect&uuid=56e4c9036cf178cc17ad06c55f4c8d753405214c3124afc74576979c8a3b4ab2&blog_id=42693868&post_id=93576&user_id=262258391&subs_id=225460721&signature=0db6fd3f85f6c58b98ae8dcd57cfd865&email_name=new-post&user_email=ishan.mail@gmail.com&encoded_url=aHR0cHM6Ly9naXRodWIuY29tL0Rhd2VzLUluc3RpdHV0ZS9haS1wZWVyLXJldmlldy1iZW5jaG1hcms&email_id=992b67be83f0486997c13e73070ea217). I hope people can build on this work to create a comprehensive eval benchmark across disciplines.
That is from Paul Litvak, here is [more](https://marginalrevolution.com?action=user_content_redirect&uuid=40efe3b823c2bb0c3f1affa8b2b39f9417a07cfefb93478f096a4db76737e556&blog_id=42693868&post_id=93576&user_id=262258391&subs_id=225460721&signature=8e56f2f94632af75cb2ce3a8ebab17ee&email_name=new-post&user_email=ishan.mail@gmail.com&encoded_url=aHR0cHM6Ly93d3cucGF1bGxpdHZhay5jb20vcC9ob3ctd2VsbC1kb2VzLWFpLXBlZXItcmV2aWV3LXdvcms/dXRtX3NvdXJjZT1jcm9zcy1wb3N0JnB1YmxpY2F0aW9uX2lkPTIyNDc4NjQmcG9zdF9pZD0yMDM2NDEyMzkmdXRtX2NhbXBhaWduPTEwMTA5MTUmaXNGcmVlbWFpbD10cnVlJnI9M285JnRyaWVkUmVkaXJlY3Q9dHJ1ZSZ1dG1fbWVkaXVtPWVtYWls&email_id=992b67be83f0486997c13e73070ea217). Note that is not even using the very latest generation of models.