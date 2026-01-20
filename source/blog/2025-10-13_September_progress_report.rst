.. post:: 2025-10-13
   :author: Julian Groß
   :exclude:

   September has been a very busy month for me as the accountant. Our organization fell victim to a group of "AI Cryptocurrency Investment" scammers.

September progress report
-------------------------

Organizational
^^^^^^^^^^^^^^

"AI Cryptocurrency Investment" scammers
"""""""""""""""""""""""""""""""""""""""

**Too long; didn't read**: We fell victim to scammers and lost >190 €.

September has been a very busy month for me as the accountant. Our organization fell victim to a group of "AI Cryptocurrency Investment" scammers, who try to use our identity to build trust with their targets.

On the 12th of September, we started receiving multiple payments of around 250€ each on our bank account, which were seemed not intended for us.
I (Julian Groß) didn't notice these payments initially, as I had already done the monthly accounting and didn't check our bank account.
On the 15th of September, we started receiving payments on Stripe, which is our credit card payment provider, as well. Since I got an email notification about those, I knew of them pretty much immediately.
Nothing seemed weird there at first; The transactions were using our donation form, so they were clearly labelled as donations. What was odd was that we would suddenly get such large amount of donations in the first place. And, looking closer at them, multiple people were supposedly sharing email addresses.
At this point, I started reading through Stripe's documentation and contacted Stripe. Unfortunately, they were very unhelpful. Their documentation suggested this being a card testing scam, and that we should immediately refund everything. Their support was extremely slow, AI translated, and never had anything helpful to say.
This is where the first mistake happens as well: I follow Stripe's advice and press the refund button on all the transactions.
What I didn't notice at the time, was that Stripe keeps their fees. Meaning that on every refund I make, the Overte e.V. pays a hefty credit card fee. Multiple Euros per transaction.
In total, we lost 163,50 € in Stripe fees.
Once I noticed this the next day, I started returning only what was left after Stripe's fee.
While that saved us from another losing another >100 € in Stripe fees, it ended up incurring a chargeback from one person who really wanted their 1,86 € back.
As it turns out, Stripe (and credit card companies) charge 20 € per chargeback. Not to mention the bank responsible for the chargeback graciously rounded up the sum to 1,95 €.
Contesting chargebacks incurs another 20 € fee. So I decided to just pay up.

In the meantime, I noticed transactions also going straight to our bank account.
This felt way less problematic, since the fees are *way* lower than for credit card stuff, and we have rule of law there, rather than credit card companies and payment providers just offloading everything onto us.
At this point, I got in contact with the Police, since the victims suddenly had names and identities, and as opposed to our Stripe account, I wasn't willing to just close it off.
The local Policeman knew immediately what was going on and asked me to inform the victims by sending them messages via SEPA bank transfers. Turns out, instant bank transfers are faster than the police. At least as long as the victims check their bank accounts regularly.

Apparently, this is a very common scam:
- The scammers rope their victims in with promises of high-return investment opportunities.
- They then have their victims pay a smaller sum to a place that feels trustworthy; In this case, a German bank account. Since it is a German bank account, at least the German victims have little to worry about. If it is a scam, they have someone they can hold accountable. None of this money actually makes it to the scammers.
- The scammers then show their victims how much money their investments are allegedly making, and are offering them to invest larger sums. At this point, they have their victims pay money to a channel they have control over. `In this latest case published by Eurojust <https://www.eurojust.europa.eu/news/eurojust-coordinates-action-halt-cryptocurrency-fraud-over-100-million-euros-across-europe>`__ it was mainly Lithuanian bank accounts.

While our bank was slow to respond, they were *extremely* helpful. They immediately knew what was going on, and offered to screen the transactions for us,
meaning I didn't have to return the money manually anymore and didn't have to account for them in our books either, since they never actually make it onto our bank account.


The scam is still going on, but has slowed down considerably. Only one of the scammers appears to remain, and I now know what to do with any fraudulent transactions we receive.

So what did we learn from this?
- The saying "Never look a gifted horse in the mouth" doesn't always apply.
- We are legally required to pay back any money that wasn't intended for us. (See `BGB § 812 <https://www.gesetze-im-internet.de/bgb/__812.html>`_)
- Credit card is an awful way of receiving donations, because it leaves you vulnerable to chargeback and contesting fees, and generally costs *way* more than even international and inter-currency transfers.

What are the next steps?
I am still considering to completely stop accepting donations via Stripe. While the 163,50 € of fees was my fault to some degree, the chargeback fees are something we cannot do anything about with our current setup.
Some donators already switched over to donating via bank transfer instead. Meaning that we receive so little money via Stripe now, that just two chargebacks per month are enough to completely negate the money received from there.
At that point, I would need to shut that channel down. We could still decide to accept credit card payments via email then; Or maybe we can find some other payment provider who takes over such fees.


If you have any suggestions, questions, or input on this, feel free to reach out via our usual channels.


Infrastructure
^^^^^^^^^^^^^^

Our `Weblate translation instance <https://weblate.overte.org/>`_ has been slow or inaccessible for most of September due to crappy Chinese AI scraping bots.
While this is probably not a deliberate attack, it manifests the same as a distributed denial-of-service attack on our infrastructure.

`Anubis <https://anubis.techaro.lol/>`_ has been deployed to our Weblate instance, but unfortunately the low percentage of scrapers that do get through are still occasionally enough to overwhelm the server and flood us with error messages.
Due to this, I had to shut down the server for multiple days. While it has been running without issues again for a couple of days now, it might get overwhelmed again until a solution is found.

Weblate added the option to back up individual projects, instead of the entire server, so we are currently looking into moving to a public Weblate instance.
So far, this has been a slow process though:
- hosted.weblate.org allows creating said backups, but it currently doesn't allow actually restoring them.
- translate.codeberg.org doesn't currently support pushing to GitHub and still hasn't made a formal decision if they want to. We also haven't been able to reach their admin yet.

We are not aware of any other public Weblate instances.

There are some other open-source organizations hosting their own Weblate instances, so we might try to join with one of them.

Alternatively, we will just have to upgrade our server and/or pay for something that lets fewer bots through, like Anubis' "`Thoth <https://anubis.techaro.lol/docs/admin/thoth>`_" service.


Progress
^^^^^^^^

74hc595 spent most of their time working on upgrading to Qt6. Apparently, the Qt6 branch already works, even if it is still very unstable.
Of course, they also did their usual general contributions like reviewing and testing a *lot* of Pull Requests.

Ada has been helping with the Qt6 upgrade, focusing on QML related fixes. They also committed some smaller fixes like fixing OpenXR trigger click reliability,
in addition to reviewing, testing and reporting bugs, and prototyping their upcoming UI theming support.

HifiExperiments helped with a lot of triage, advice, and code review.

RTUnreal worked up upgrading dependencies and has generally been helping with build system maintenance.

I was mostly busy with handling the recent scam and the flood of broken Chinese AI scrapers. In addition, I worked on refactoring our GitHub Actions workflow files (shoutout to RTUnreal for the code review),
fixed some smaller build system bugs and troubleshot regressions. I also started initial work on an itch.io release: Finding regressions introduced multiple releases ago isn't fun and showcases that there just isn't enough testing happening.
This suggests that it is about time to try to get more users in. When this release will happen isn't entirely clear yet; We have an upcoming protocol changing release which will undoubtedly introduce more not-yet-known regressions, as well as require all servers and clients to be updated.

We also received bug reports and help from Alezia, Dale, and Krzeszny.
Big shoutout also to KawaneRio for organizing Sunday's "Overte warmup" event.

Release!
^^^^^^^^

We made our first release since switching from VCPKG to Conan. Version 2025.09.1 and its changelog are available `here 🔗 <https://github.com/overte-org/overte/releases/tag/2025.09.1>`__ and come with a *huge* list of bug fixes, improvements, additions, and changes.
It does come with a regression that causes it to crash on many on some Linux distributions when opening a web view, like the Places app. A fix will be included in the next release. For now, affected users can get the CI testing build from `GitHub <https://github.com/overte-org/overte/pull/1840>`__ or keep using version 2025.05.1.
