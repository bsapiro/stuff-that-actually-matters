#The case for making data protection a foundational requirement

_(working title)_

_note: intentionally focused on why and what - not how_

##a software based society
* we are increasingly a software based society (software eats the world argument)
* we rely on software (software on hardware or software in hardware) to run our society
* software runs critical parts of our society from financial systems to electrical grids to manufacturing. Software keeps planes in the sky and keeps us connected (even your old bakelite phone relies on a smart network core to route your call)
* even software that isn't mission critical was become important to its users
* if software fails to work the way we expect, whether by accident or by malicious design, it has impact on its users ranging from mild inconvenience to business disruption to life altering events (cite impact of Russian intelligence activities)
* we aren't just build software, we're building fundamental parts of society
* consider software that has crossed the 1 million user mark, those that have crossed 1 billion. How many users does software need before it is part of society? It could be as little as one user in one important company. 

##user expectations
* users give us their data and expect us to keep it safe, they trust our software and by extension they trust us
* use of data is not a neutral act, sharing of data, even if public, is not a neutral act. Whether that data is shared involuntarily, whether stolen or shared because of a monetization strategy (even if consented too) users feel a betrayal of trust
* if we share data in a way the user does not expect they lose confidence in us
* if that data matters to them in some way then
* the user expectation:

> I will give you data and expect that you will keep it safe. Protected from unauthorized access; free from corruption and available when I need it. I will give you no reprieve in this matter

* 

##as we became connected we relied more on everything around us
* your software relies on third party components, a data centre, other service providers
* to make our software we work we may actually share some or all of the data we collect with someone who transforms it in some useful way
* what if your software is the third party component or service that other depend on? If you don't make sure you build your systems with security and privacy as a primary requirement you could cause harm to others

##getting hacked
* getting hacked - having your data stolen, your systems intruded open by unauthorized access, service disrupted - whatever the actual harm, the act is what we will focus on. The motivation behind a hackers actions is rarely informative until after the fact.
* the old adage about getting hacked is that it's not if but when
* "who would want to hack us" is not a useful line of reasoning
* asymmetry of security - you have to be right the entire time, hacker only has to be right once
* automation - hackers embraced automation long before the software profession discovered devops. Hackers can trivially search the entire internet for a specific class of defect and then abuse it on mass
* in a highly automated criminal world, the cost to compromise a single system is approaching zero. You are just a target of opportunity, you may be hacked first and put to use later.
* hackers exploits flaws in software/systems to gain unauthorized access

##why are hacks possible?
* we won't discuss all the means in fact we'll concencrate on concepts alone
* bugs in software - pure implementation flaws, logic errors, design mistakes or intentional ommissions based on ignorance or invalid assumptions
* implementation flaw lack of input validation
* assuming you were operating inside an environment you have exclusive control of
* relying on third parties/components to behave in a consistent manner
* the top of objective for a hacker is

##the smallest unit of data
* pretend for a second that none of the data your software processed mattered
* let's pretend that the only thing which matters is a short string you store called a password
* Why does this string matter? It's the keys to access your software
* Even if your software doesn't have a user authentication function, somewhere in the environment that your software operates there is something that handles authentication and with that password, someone can get to your software. So, for the sake of argument let's assume that functionality is a part of your software one way or another
* The password only works if it is a secret. If even one more person than it's user knows the password then it's utility is immediately destroyed. Even if the other person that learns the password is the most trust worthy person on the planet, we are no longer certain as to who made use of that password and we can no longer guarentee the password's owner that nobody can access their account
* What if that user used the password elsewhere? Users shouldn't do that but in practice they often do and while they are complicit in the problem expanding, it was us that allowed it's disclosure to first happen and now other parts of the user's life are exposed. Perhaps that password being stolen from your software led to greater harm than you could have anticipated.
* What if we didn't know the password were stolen? Then we would not know to monitor for unauthorized access, we would not know to tell the user to change their password. Not only does this leave the user with a sense of uncertainty as to who harm came into their life likely causing them to scramble to regain control. What if the user is unaware of the theft and therefore unable to respond till the harm expands to an ever widening pool of victims as their access is used to steal data about others?
* If we are entrusted with passwords we have a duty to protect them. We need to protect them from not only those that are malicious but also from those that are good, which includes ourselves. The techniques are well understood.
* However, we're not just entrusted with passwords, we store and process so much more and those passwords are there to protect the data from unauthorized access. If we need to protect the passwords to the best of our ability then by extension the same requirement extends to the data itself. It's pointless to protect passwords alone.

##privacy and security

##informed consent

##understanding (regulatory) harm
* arguably getting hacked is bad but there are different types of impact
* ...

##the cost of a breach
* investigation
* downtime
* reputation harm
* loss of sales / loss of velocity / loss of users
* cleanup
* fixing broken software
* lawyers (suing you)
* lawyers (keeping you from being sued)
* product recall (if your software is in a tangible thing)
* dealing with regulators (like lawyers but less willing to compromise)
* increased insurance costs (both directly and indirectly to other insureds)

##the lawyers are coming (actually they're already here)
* contracts commit parties to protect data
* lawyers have enlisted the help of technology professionals and security advisors in crafting legal contracts that speak to data protection
* failure to meet contractual obligations result in contract breach which opens the door for litigation
* lawyers may not understand the nuances of software development but they understand law, harm and failure to fulfill contract obligations
* lawyers are also backed by a growing suite of data protection regulation (software distributed globally can run afoul of many laws)

##the citizens are coming
* security breaches have resulted in class action lawsuits against Sony, Home Depot, TJX and others
* legislation in the EU will give individual the ability to pursue companies directly that fail to protect data properly (this includes suppliers to other companies)

##the internet's alpha predator
* Snowden's revelations about the NSA and Five Eyes confirmed our wildest fears
* ...

##an impossible promise (but one we must make anyways)

##security and privacy at the beginning

##well understood problems 

##well understood solution patterns

##it's a business problem

##responsible disclosure

##design defensively - do not put yourself in a position of trust
* as we see legislation being passed in the United Kingdom, China and other jurisdictions that either require that "technical assistance" of some sort be provided to law enforcement on request. At first that seems entirely reasonable, but what if that technical assistance means weakening encryption or putting a backdoor in your software?
* Apple security... the HSMs... engineers were willing to quit

##a call for help
* built software that follows security and privacy patterns
* test your assumptions that underpin your security
* have a practice of closing security defects rapidly
* make eveyone in your team responsible for delivering software that is secure and respects a user's privacy by design

##a note on the internet of shitty things
* We're connecting more of our lifes by instrumenting our movements, automating our homes
* The software inside IoT devices has poor quality (Mirai botnet) and remains unpatched, outdated with little incentive to manufacturers to update
* Not only do these poorly designed software devices expose their owners to harm but we've seen them (massive Botnets)
* IoT devices are long term devices; we've seen with SCADA/PLC that they remain in use far past their "best before date" meaning risk lives for a long time
