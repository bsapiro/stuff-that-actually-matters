#The case for making data protection a foundational requirement

_(working title)_

_note: intentionally focused on why and what - not how (there are plenty of publications on how to build software that protects data_

##a software based society
* we are increasingly a software based society (software eats the world argument)
* we rely on software (software on hardware or software in hardware) to run our society
* software runs critical parts of our society from financial systems to electrical grids to manufacturing. Software keeps planes in the sky and keeps us connected (even your old bakelite phone relies on a smart network core to route your call)
* even software that isn't mission critical was become important to its users
* if software fails to work the way we expect, whether by accident or by malicious design, it has impact on its users ranging from mild inconvenience to business disruption to life altering events (cite impact of Russian intelligence activities)
* we aren't just building software, we're building fundamental parts of society
* consider software that has crossed the 1 million user mark, those that have crossed 1 billion. How many users does software need before it is part of society? It could be as little as one user in one important company. 
* if our software is relied upon by civil society, do we have a moral responsibility to them?

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
* we know governments are acting against their citizens, sometimes with deadly consequences, by abusing flaws in software
* governments have don't demonstrate the same economic rationale as other hackers. Specifically, a moderately protected system may be enough to dissaude the "common" criminal but a government may be willing to spend well in excess (either in effort or actual cost) to compromise specific targets for reasons of national security. While there may be some legitimate national interests at stake, an anti-government activist or a journalist are hardly that.
* If civil society depends on certain assumed security properties of your software, their absence may actually result in actual harm including the possibility of inprisonment or death

##an impossible promise (but one we must make anyways)

##security and privacy at the beginning
note: _might move this closer to the business problem point_
* putting the cat back in the bag, or undoing the damage caused by a breach is difficult or perhaps impossible
* refactoring code and design to achieve data protection outcomes is an expensive form of maintenance on youtube
* building in security and privacy through good coding style is barely more expensive

##well understood problems 
* there are hundreds of security conferences, thousands of publications and tens of thousands of talks on how security in software fails
* a video how to hack a web app or circumvent common security can easily be found on youtube
* while we deal with new manifestations of a given security problem as our technology evolves, the underlying principles in security failures (such as trusting input from an untrusted source) have not evolved in decades
* other than time there is nothing stopping a software engineer from gaining a basic knowledge of how software security fails
* the solutions to these problems (input and output validation, enforcing of trust boundaries, controlling access to resources) are well documented and easily accessible

##it's a business problem
* While this manifests as a technology problem, it is at its heart a decision around where to spend resources. Shall we ship more features or ship safer features? 
* The business wants to make an informed decision around what the likelihood and impact of a security breach is versus the likelihood and impact of having fewer features than the market demands. In the lack of good data, they're most likely to see the failure to stay competitive as the far more urgent risk
* We know that security breaches happen, we know they have varying degrees of severity and while actuarial tables don't exist for this class of risk, it is possible to build informed models that actually describe the likelihood of a breach and it's actual impact (Monte Carlo sim, "How to Measure Anything" by Douglas W. Hubbard - no... not that Hubbard)
* Good coding style is barely more expensive in the short term and cheaper in the long term. Good design practices are likely more expensive for the duration (security at a design may require more abstractions and overall functionality)
* be cautious of the "do just enough" or "what's the rest of the market doing" rationale. While it may be a rational business decision, consider the following:
  * being industry average is literal solace when you get hacked and your competitors don't
  * if the rest of the industry does a poor job, does that excuse you from your moral responsibility to do the right thing?
  * some classes of bugs are trivial to fix quickly but for those that are not, you could find your software in a vulnerable state for months as you refactor code or possibly even rearchitect your software
  * you do not control the rate of progress the criminal element (or even security researchers) make in abusing vulnerabilities in your software. More importantly you are blind to their efforts (and possibly even their success)
* Best case you're playing a case of catchup to fix a security defect, worse case you're cleaning up after its too late

##responsible disclosure
* sometimes our software has security defects in it and its important to tell your users about it so that they can make an informed decision about fixing it.
* Ideally the software updates itself automatically without impact to or involvement of the user(which, if you look at web browsers, is now a universally adopted pattern)
* However, if your software doesn't then you owe it to your users to tell them that a security is weaker than they though it to be so they can choose what to do

##design defensively - do not put yourself in a position of trust
* as we see legislation being passed in the United Kingdom, China and other jurisdictions that either require that "technical assistance" of some sort be provided to law enforcement on request. At first that seems entirely reasonable, but what if that technical assistance means weakening encryption or putting a backdoor in your software?
* Apple engineers were willing to quit if forced to undermine the security of their product (http://www.nytimes.com/2016/03/18/technology/apple-encryption-engineers-if-ordered-to-unlock-iphone-might-resist.html?_r=0). How many of us are willing to put principle over pay check? What about our own freedom?
* Don't make your security depend on you behaving in a moral/ethical fashion. Make your security work even if you fail to do so. If you have privileged access that can be abused, then you are a weakness in the security of system and you undermine the security you provide whether you do act maliciously or are forced to do so by others

##a call for help
* built software that follows security and privacy patterns
* test your assumptions that underpin your security
* have a practice of closing security defects rapidly
* make eveyone in your team responsible for delivering software that is secure and respects a user's privacy by design

##a note on the internet of shitty things
* We're connecting more of our lifes by instrumenting our movements, automating our homes
* The software inside IoT devices has poor quality (Mirai botnet) and remains unpatched, outdated with little incentive to manufacturers to update
* Not only do these poorly designed software devices expose their owners to harm but we've seen them cause harm to others (massive Botnets)
* IoT devices are long term devices; we've seen with SCADA/PLC that they remain in use far past their "best before date" meaning risk lives for a long time
* If you are building software that powers IoT devices then building defensively from day is essential and having a plan to keep security updated. IoT software builders find themself in potential position of having to maintain software forever, possibly long after such maintenance is no longer profitable. A difficult position to be in but one that only underscores the need for building security in at the very beginning or face the possibility of expensive maintenance work later. In the enterprise world where devices are covered by support contracts and End Of Life notices are often ignored, what will happen in a world where IoT device manufacturers are selling devices to consumers who are still running Windows XP well after it's end-of-life date?
