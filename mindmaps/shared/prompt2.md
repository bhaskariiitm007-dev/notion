usability - Transcription

Time:  13 May 2026 13:10:02
Topic:  usability

00:23
Three to two, try to move on.

00:30
There was this one called the upcoming center.

00:35
Something was decided that we will I mean, we will try to go ahead with the strategic approach and we will see if intellemas doesn't have capacity, then only we can go for tactical things. Okay? That's what I think was this capacity. I did not. But and actually I joined.

00:58
I mean, I did not get the invite. No, we we were on call on a call. Now that was the final call.

01:13
I.

01:21
Okay, so, um, so basically,

01:27
Anyways, whatever was discussion? So I was listing down all the tasks from etl perspective and usability perspective. So as you mentioned that to onboard any of the asset classes, there there is already ah agents sub level,

01:43
 ah we can use that. And that requires two laps. Day, you mean two, two last day? You mean four days, right? Yeah, four days.

01:53
Okay, yeah, four days.

01:55
And one was one another was like some kind of investment on usability side.

02:06
I'm not sure you mentioned that you will check in richmond.

02:11
Yes. So we already have like similar thing have happening for other things. We just need to figure out like what we will join keys and everything.

02:22
So there is an investment.

02:24
Yes. Yes, there is an enrichment which we can extend to sftr. The data is already there for sftr because we are using it for pairing and matching.

02:31
So that enrichment should happen in new gen control. Yes. So usability pipeline?

02:36
Yes. In your safety pipeline. Cp.

02:38
Um okay. See, see. Ah so ah what do you think? How much efforts?

02:44
Not much Pro.

02:48
There is a nuclear fish here that's with.

02:53
You you know this recipe. Yeah pairing and matching now stuff. Now you see that request. Yeah,

02:59
I heard that. That is moving to usability.

03:02
It is sounds really interesting taking maybe one, one, one that piece actually.

03:09
So if you see sftr here, you see an option padding matching. Okay. So so this is we are see purely, okay. So here, like we already have the data populating in the same tr enrichment table. Like but so stable.

03:22
 So we just need to figure out like what will be the joint keys for that particular say from intellectual or you to use a uti mandate, then material join keys for missing gtx breaks and field plates and we should join. That's it.

03:36
 Not a big task.

03:38
Missing in fields. A missing in fields.

03:41
Why missing in fields? We have trade ref, right? Okay. But missing in gtrs is not present in gts system. So joining with trader will not be useful. Will not have trade ref missing in gtrs.

03:51
Do you receive such breaks as well?

03:53
If there is a C two D reconciliation will receive like a that will be seat. If it is C two d, you'll have like um ccd. Thirty percent of these area there could be population break. Yeah population breaks in the other side. So if it is missing in the gta system,

04:07
Then usually whatever file we send except the D side file,

04:14
We ah send the same number of rows on both all the files. Like if you send AAC files, then the number of records will be same on both a and c. Yeah, our dt AD side file is like dtc. We don't do any kind of removal or enrichment

04:35
Or any series.

04:35
So there could be chances of population break on when while comparing with reconciling with the dtcc or D files, but it should not happen for other files like a to c. Why upstream? Because what um ah what is the

04:54
A to Z break growth if there is any I

04:57
Am saying in perspective of not for sft. Yeah.

05:00
I'm saying it it for in general,

05:02
For India and the jfsa, a two C files are built in such a way that both will have same number of records.

05:12
Then you will not get into population breaks, right?

05:14
We will never see any population break for A

05:17
To c. But we do have.

05:19
We do have.

05:24
Ah so there is an apps difference in the upstream and there is a difference in the unique identifiers of gtr system. So we but we get like missing in upstream and missing in gts. Okay.

05:42
Because whenever we send files for a and c, we do internal join and then we create two separate files, one for a and one one for she.

05:55
I don't know. God like how you you can sell it. But we get a file which has like, but like yeah how you compare. Now here to see like a file and see so how we are comparing, like engagement, how they compare, and what is there in the files? We don't have accessibility, but the file we are getting now, it is having population, okay?

06:15
So yeah, yeah, the missing in primary, this will not have to address in it. Right?

06:18
And this is for sftr.

06:20
Yeah sftr ST three sftr. it is the population as many as the same. We have it. So here this one the known unknown function, this will be.

06:33
Like this is they have written rules. So if the field is this value,

06:40
Is this is it the tag? Okay. That that feature is there in India?

06:50
But like how are we going to do that in new jersey? We may have to write for go for rules

06:56
With track system

06:57
Id. So that's an inbuilt feature we have in cpp, but rtp has to adapt to it.

07:02
Okay. So you mean whatever ah known issue tag feature is there in old end reconciliation framework that similar feature is in usability news? And like,

07:12
Yeah, we can create rules. Okay? So you know this if this particular field is this this particular value is this, then tag it to this particular media review.

07:21
Who who creates those rules? Ah okay. Ah rtb,

07:25
Ah rtb. Ah rtb creates those rules. Ah rtb creates those tracking system id. They enter it in one space. Like we have one dashboard just for that. Um so you need to educate them. So if you see here, no.

07:36
 So their rule is if asset classes in this, if a asset class is any one of this and a counterparty one reporting, what about this? Is is this one? Then tag it to this particular attack instrument. Okay. God, they do it.

07:48
 They see it here. So,

07:49
And that is one time configuration.

07:52
One time configuration, every day it will get reflected.

07:54
And that will reflect for all the users or only so

07:57
Users of this when the reorganization, and so so it picks up. So whatever you see in the UI, right? it will be tagged on,

08:03
And that's nice. Because known issue tag is something which is implemented on our side. Yes, that needs to be implemented in code. Then only it will flag. Yeah those known issutags. Yeah. But this is something from UI, then it's easy.

08:17
Yeah, they can. I can conquer. And like if they feel that like this is no more issue, they can just delete the rule.

08:23
This is for no need to tag any other ah things.

08:25
I think that we have a special check actually, but I don't. Yeah, sorry. The tableau. And I said, no aggregation. I'm still checking. I didn't get a reply. Like where they are using it.

08:35
Ah so the aggregation is happening in the old yeah pipeline. The old usability pipeline? Yes. Is it in code or is it that is also something detail.

08:47
We have a separate etl in our.

08:50
Okay.

08:50
You shouldn't be safe.

08:55
So we insert this data into the yearly MA. Yeah this one active break, aggregate euri. Okay. What it does is like that particular we will have like break closure and everything on a day to day basis now.

09:06
 So with this particular reconciliation type, how many breaks are there at the end of that particular day? it will just list that breaks in numbers like this many breaks, this many known issues, this many unknown issues.

09:18
 it just list that and we show it to the dashboard tab, dashboard. But now that'sAnother condition because we do not have breakClosure.

09:26
Number one and number two, the etl function, sorry, the aggregate function which we use is different. The table is different. So they may have to like create new dashboards or like integrate that into the nugen dashboard actually, as a tier one into the nugent dashboard.

09:42
Why are we not losing those ah rates now?

09:45
I don't.

09:47
And new pipeline.

09:48
We don't have that functional data. Okay. Like if we are receiving some breaks today, we are going to receive that breaks tomorrow. Also, if it is an open break, it is a live trade. So we just increase the age of the.

10:00
Like like if the age was yesterday, one, we exhausted two. Okay.

10:03
So you mean this aggregation is happening in older gen. Pipeline. Yeah, but that won't happen in new gen pipeline.

10:13
It just has a different flow. it happens. Aggregation is happening, but different flow of different table, different columns.

10:20
 So there that tablet dashboard which is built on this particular table now will not work for a subtr anymore. So then you have to like onboard assertia to nugen tricks, like where we have like a sigmas and everything now.

10:33
 So they have to onboard it to them. So that stuff, the tablet stuff they need to do because we will not be close to that. Right? A tableau developer should beAware of that iridium team. I have checked with one of the BA.

10:47
Bit. I haven't got a reply. I'll check if and anything else.

10:53
So this is related to investment that that aggregation.

11:01
And okay, in return, you will have a look and we have the data.

11:06
So you can just configure like whenever you are doing CV generation, you know you will have the opportunity to.

11:16
So I just add this similar to what we have for SFT usage.

11:36
Similar report. Like for scc, you created one, right? Ah yeah, ah C two D two. Okay. So based on the reconstruction type, you will be creating one JSON config file that is going to be the base of your code. Okay. Okay.

11:49
So that is something will be displayed on ui. Exactly.

11:53
So what you see as this is the reconciliation type. So what you see here at type, now that is this.

12:04
Otherwise. Yeah, I get confused because I am not.

12:07
What is the name going to be? I asked this question. So the name is gonna change. Like change. We have not decided if changing we are good. If not, then you have to like pour little bits of pieces actually. Okay,

12:21
Then we'll change it.

12:29
Ah so this

12:30
Is the current I am idle match format. This is how they give us the file name, IRCC. Okay. And and here you see that.

12:39
And that agent ah creates autosis jobs. That is for onboarding the.

12:50
A new agent creates this json. If we have three agents, one for creating this JSON, one for creating the autosis jobs with using this JSON, and one for the year, your ua configurations. Okay.

13:04
So three agents. First ah is jason. First of all, one will create json. Then second one will create. Um what was this based on this? Yeah. And then third one,

13:20
Third one will be the ua changes, UI changes. So these two things are in control visibility repo first and second control usability. And third one is in usability gateway.

13:36
So that the angular budget.

13:40
So these three events, then the second chance you mention the name.

13:47
So you have this name,

13:48
See this name,

13:49
Underscore the copy, this dot that this is the file format. So you should be also giving us in this particular format. I think everything is all okay.

14:01
 And the column names also should be matching this from here to this one right master key to and also from here to unique for a parent to play this till this match id. This should be this is a mandatory actually.

14:20
Master key and match key.

14:23
Match id. Match id.

14:25
Yeah this should match where starting

14:28
To master key and match id to item state. Yeah, this is mandatory. And apart from that, you will have like unique transaction identifier, unique step identifier, unique product identifier, right? Like whatever it is, but that is configurable. That can be anything remaining. Everything is your. So

14:43
This is mandatory to define where

14:46
This should be part of the output file, right?

14:49
But you give to yourself, okay? From intellemas,

14:51
From intellect side, okay? If they are doing the reconciliation they fall for sure will provide. If you're doing the integrity, you you should make sure that you give us this.

15:01
Taken. Ah so this is this is again output file.

15:06
Yeah anything else that in the jason file if you want like industry enrichment, right? So for example, if this is a CC two one, now what we have like exception enrichment, tier enrichment, dtcc enrichment all happening. Okay. If we wanted to extend that to sftr, we are good to go. If we don't want that,

15:29
We just keep all these

15:30
Things as empty if you don't pass this one. Okay? Okay, so whatever JSON you create here, right? This one, agent. So this will create with the default index resources, you just need to manually delete if you want. Don't want it.

15:45
Ah so we would like to manually delete those stuffs, which we do

15:52
Not want to do not want in the

15:53
Enrichment sources. Correct.

15:54
If you don't want enrichment at all, this is not just configuration, right? So there is this multiple stages. Three four, five, four is the enrichment stage, you can just skip that.

16:11
Okay? Yeah. So you you see one,

16:14
Two, three, four, this is the stages, okay? And what the stages means now.

16:22
Here you see. So number one is control metrics. Number three is im load, four is enrichment, five is auto tagging, which I mean like tag system arena. So if you don't want engagement happening, you can just remove this in the author's job.

16:36
Now you can pass one two three five,

16:39
Six seven eight instead of four.

16:41
It will work

16:43
Only

16:44
For investment

16:45
If

16:46
You

16:46
Don't want anything, or like keeping it empty, also perfectly fine.

16:54
And this in the this these stages are defined in visual. Yes,

16:58
I know. This is in your autosis profile profile which was created from here.

17:08
Yes. Otherwise we can keep it in empty,

17:13
Also in jason directly.

17:20
And that that take again like from BS. We need they want any new things on when we are going like if they want any enrichment, right? That should be decided with like

17:32
Ah rtb and bs should

17:34
Be discussing with them like whether they want anything new or like just they want like

17:37
What we have now. And the thing you mentioned is if they want to have a auto closure, then,

17:50
B is need to define.

17:52
Yeah we don't have provision for that now.

17:57
What rtb right now? Does it now with other rtb? Secondly, so they have like contracting system id defend and there's just if it is a known issue and it's no more issue, they just tag it to that particular tag system id. Okay. They don't do any investigation on that type of system id. They just investigate the remaining.

18:18
A very high level key. What is the responsibility of usability? What are all the things you guys cover?

18:28
One. And we have that.

18:30
What is under ah the wood's team. I mean,

18:33
Okay,

18:33
The books also utility matches. Okay? But we take care of the reconciliation. Or like you, I javasite. Okay. Angular java site. Anything on tableau and etl that goes to them, right?

18:47
Um tableau.

18:49
When does it comes in picture.

18:51
Ah higher management. They just look at the table dashboards for everything, right?

18:55
They don't want like detail data.

18:57
Yeah,

18:57
My that's a my management information.

19:03
High level, high level enforcement, just numbers. Okay.

19:05
High level. And what do you say?

19:10
ETS. If there is anything like etl, etl, like SQL, everything. Basically, they are a SQL sql. So you have your dtcc report, like how that we picked in usability, right?

19:23
Like all these things take care of. Okay.

19:25
And this UI and java side. Ah what are all the features there in usability? Which.

19:38
Which is for any of the reconciliation and which bas use, for example.

19:48
In the UI, you obviously saw all the results. So that is one kind of feature that you show. The the users can aggregate or all those stuff is.

20:00
Okay. But award from that, let's say you there is a feature to or auto close ibs can tag that. So that is one. But so like that. Is there any other feature which is specific to reconciliation and

20:15
Which user? Yes. Okay.

20:17
Like new journey. We have like commenting feature. They can just write, click the breaks. There is an option to comment. They can just comment it or like they can assign it to somebody. Investigation status,

20:29
Again, that is for if they don't close it, they can comment it.

20:33
And yeah there is that coming into reflecting there and it can be grouped by comment.

20:37
And that is only a specific when you do not close your group.

20:41
Now that depends to you. So like they they can do like whatever they want. Okay.

20:45
So that is independent of in demand. Yeah. Okay.

20:49
Investigation status. Commanding to like how? What is the investigation status of these breaks? Who is it assigned to those things we have. Okay.

21:03
And yeah pretty much that no other actions are there. Yes.

21:11
And commenting is there in origin as well. Ah but not like this. Something different process is different. So here the commanding carry forward as well. If your record key right, like the take your id for people in order.

21:23
 So if it is the same, we will propagate the comment to the next day, the next day, next day, if everything is, say, like, if the break is going on, carry forward it. The government is also going on going forward.

21:37
So auto closure coming feature investigation status, auto closure,

21:42
We're not doing that.

21:43
We need to have discussion. No, no. That we is doing, but that feature is from usability side. Now we once we will close, no,

21:50
Ah we don't have the auto closure feature for new gen.

21:55
So then how can be is like,

21:58
Okay,

22:03
Sorry,

22:04
I got confused. That is tagging.

22:16
So there is a auto tagging feature, comment feature and investigation. So yeah,

22:22
Okay. Like whenever you receive it, like whenever the record is received,

22:27
It automatically runs based on particular rules.

22:30
Yeah preconfigured rules. Yes, preconfigured rules. Yeah they need not do anything manually for this one for commanding. And this investigation status they have like manually do it after you see the brakes on your way, there is something before you see the brakes on UI.

23:07
The breaks. But there are so many features,

23:09
So many things. Like our team is doing these things here, like four teams actually five. So five different teams, different works on five different things, but we we just focus on drag on.

23:20
But the other teams are ah related to

23:22
Core or everything on dashboards. Everybody is working on dashboard. We have like exception manager one. We have like this. Like

23:30
That is not something related to our space and um but like controls the space it

23:34
Is. So like whenever there's a trade flowing, whenever there's a hack on that, where do you see that? I connect? Okay, so we listen. Dashboards for that. So if they wanted to override reprocess, all these capabilities,

23:46
 they built it. Ah for us, it's like user interaction is less. We just show the data, but they interact with the data. So they do reprocess, overrides everything except force. Like lot of things happening in the back. Okay.

23:58
 Core and controls are building the code and we are integrating theCode to I will toUsers,

24:03
That's it.

24:08
How did you find? Have have you started? Although new things using copilot AI, how did you Find X6seful? Is it useful personally? You are not a big fan. Why?

24:30
We had a joy of developing life. Now the joy is gone. No, it's easy. More easy. We didn't we don't have any difficulties, challenges, nothing, I feel personally I think, but it's really useful. Whoever does he know the code base? From the day one of his work, he can do starting commitments and nothing goes majorly wrong.

24:50
So what are all those features do you use mostly? I mean, which model do you use?

24:58
May mostly.

25:00
Personally, I mean copilot,

25:05
Copilot. Okay.

25:06
And yeah,

25:08
I think that's it. And sometimes I use this gpt as well.

25:15
Um so you never use opus models. Okay.

25:21
I haven't tried gpt one. I tried plots on for this one price park. And it's just not I mean, it was able to do deliver, but not to the standard. Actually, the best practices. I prefer click gpd for that. Others I have you know what I have found,

25:40
Man. Ah cloud and codex both are in different space. Like cloud can do a very complex

25:51
Task and

25:54
It won't do easier task very well. And codex will do the easier task. Very. That's what I have my experiences so far.

26:11
And will start implementing it. I have developed something.

26:16
Yes. You know.

26:22
It's there or not.

26:23
Ah like I have developed some games. This is using all cloudshire and this is on hosted on my personal.

26:31
This one we have. it's not it's not here.

26:35
So like if you want to play, so these are all memory games. Like select all this and submit. So if it's strong, then you won't get any points like that. Puzzle games or like this is to train your brain.

26:54
Like, so III mean, I am not EY guy, so I and I'm.

27:04
I never found. For me, it's little difficult for managing the wife. And yeah,

27:11
I mean, learning new technology is really good. Like that is. I mean, if if you are not a UI developer, then having to.

27:25
So these are all things done by this one. I did not do anything.

27:33
Yeah. So that's what that's why I was surprised he, even if I don't know, I can build so so many things.

27:40
You can build things. But the difference is how we are building. So is it the best code that you don't know without that without you knowing the code? Right? Even in java, like you'll have like just for loop or streams or anything.

27:54
 You decide like which one you want. But if if agent suggest you go go with for loop, we should be knowing like why is such into but.

28:17
Now what they are planning to do, one model will write code, another model will review the code. So we we won't be reviewing and the codes as well. And some company has already built their tools on these things and they are advertising that, no, no, things are moving very fast.

28:49
I mean, you remember now, like when we had this it's Mongolia. We were like pouring like you know but that you're not doing anymore.

28:59
So that's interesting.

29:00
This new gen framework. We built it from a scratch. We started from zero. And we built everything, all the framework, and using controls framework. Now it's easier to develop anything on board anything. Now we have built so many things. Now within two days you can onboard any again,

29:23
Same with you previously. Just use take like four or five minutes in the whole like in days. You can do.

29:27
Also when we started everything, like, every details, like how will we store the data? In which data structure we will use? Why not this one? Why that one? Why not this one like that? Everything we discussed in details and review

29:47
This one and things

29:48
From scratch. But now,

29:59
So if you are a good.

30:19
Um this one I am planning to.

30:23
Ah right now I have ah developed six games, so I have planned to develop around two hundred games.

30:30
Two hundred. Ah and

30:33
We'll plan to do it in within a month. Once that is complete,

30:37
Then maybe I'll post it in production for everyone.

30:43
Everyone can use it. But the link is like my personal github.

31:05
Their capacity, I will list out all the tasks first. Then we will analyze the how much effort is required from their side. We will discuss with them and if they are confident, then this will go ahead with strategic purpose, otherwise will go ahead with tactical solution.

31:25
So major reason for the slowness, I'm just setting that ACD stuff. That's my especially we are planning to do that. Like the monday we are gonna start in our project seventy one.

31:47
So now

31:49
People have started using ACC as well. So ah in opensbake, I think we will need to configure the tools. Like we need to connect ah all the tools, but in acc, I think we don't need to do that as well. it will automatically.

32:08
So.

32:12
And john is committing quotes like any twenty one, he will commit thousand lines of code and ping pr to me that.

32:27
And I need to review everything.

32:34
I think he has

32:35
Already put open his fake all the skills, bloody skills. He started using cloudy code as well.

32:48
Yeah.

