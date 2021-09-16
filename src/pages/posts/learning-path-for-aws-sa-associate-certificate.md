---
title: Learning path for AWS SA Associate certificate
subtitle: '"Doing it my way"'
draft: true
date: 2021-07-16T12:57:34.642Z
thumb_img_path: /images/aws-arch.jpg
excerpt: Detailed summary of the preparation to AWS SA Associate certificate.
template: post
---
# **TLDR;**

This is a summary of my experiences preparing for AWS SA Associate exam. The post details the 

* learning process 
* useful resources 
* gotchas/pitfalls
* online exam experience

The intention is to help readers to get the certificate with minimal effort. Obviously, this is just one - although, it is proven - way to tackle this certificate, there are other ways too, which might fit better to your background and experience level.

# **Background**

I'm working as a lead dev since 10+ years. During my professional carrier I worked mostly on web applications both on BE (Java) and FE (JS), except for a short 4 years when I tasted a bit of telecommunication (C). In the last 3 years I turned my attention towards software and solution architecture and I'm still actively educate myself via self-learning. Because I didn't have any exposure to cloud based applications so far, getting the AWS SA certificate seemed to me an ideal challenge. I had zero experience with Amazon Web Services beside of a few architecture related articles read about AWS (and in general about cloud computing), no hands-on stuff though. I was also curious how long would it take to pick up the knowledge needed to pass the exam.

# Preparation

It is staggering to see the number of AWS services at the first time. The documentation looks never-ending, the sheer amount of concepts and topics you need to comprehend can make anybody uncertain: where to start? The journey from zero to hero will take time, if you are totally new to cloud computing it makes sense to check the entry level certificate: [Cloud practitioner](https://aws.amazon.com/certification/certified-cloud-practitioner/?ep=sec&sec=fndl), this meant to explain basic cloud concepts and make you familiar with AWS as a whole. I deliberately skipped this given my strong technical background and advancement in solution architecture. I still think I didn't lost anything with this decision.

Here is my recommendation, gain the basic knowledge from an official preparation course, (I've took semi-structured notes too to make the information stick) then start drilling with practice exams. Don't worry about the score first, you should focus on the reviews and understanding why your answer was wrong and what is the correct one (and why). After a while you will recognize recurring patterns, make sure you are not failing those. If you are facing with a question about a service you don't know anything, close the gaps with the official documentation. This is an extremely efficient way to progress. Make sure to have at least a stable 80% score before making an attempt on the real exam.

## Exam guide

Before jumping on the preparation details, let's observe our primary target:  [Solution Architect - Associate](https://aws.amazon.com/certification/certified-solutions-architect-associate/?ch=sec&sec=rmg&d=1) (SAA-C02). Best to get familiar with the [exam guide](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Exam-Guide.pdf) first to understand what is (and what is not) to be expected on the exam, make sure that you understand the main domains the exam covers. Also worth to take a look on the [sample questions](https://d1.awsstatic.com/training-and-certification/docs-sa-assoc/AWS-Certified-Solutions-Architect-Associate_Sample-Questions.pdf). 

*Note: The exam has 2 versions, SAA-C01 and SAA-C02, the latter is the only one available in 2021, main difference is that operational excellence is removed as a domain, therefore more question targets cost-effectiveness. You can consult with this [page](https://www.whizlabs.com/blog/aws-saa-c01-or-saa-c02/) for the details. The importance of knowing this will be clear when the hunting for learning resources begins.*

Amazon also recommends to have at least 1 year of hands-on experience with AWS before taking on the exam, according to my experiences this is not a must.

## Domains

The questions are centered around the main domains. The percentages tells you that roughly how many question targets a certain domain:

* Resilience - 30%
* Performance - 28%
* Security - 24%
* Cost-optimization - 18%

You will find that the different exam preparation guide's structure follows this break-down too. These 4 domains represents 4 from the 5 quality attributes (or pillars) upon AWS built his [Well-Architected framework](https://aws.amazon.com/blogs/apn/the-5-pillars-of-the-aws-well-architected-framework/). (The fifth pillar is operational excellence which was removed in SAA-C02, I believe it gets more focus in SysOps Administrator – Associate exam). You should know about the well-architected framework, every pillar has a whitepaper which introduces design principles and best practices, you can run through them once, I mostly found them dry and boring.

## Prep courses

(*Note: There are links in this article to paid/subscription based material. I won't earn a thing if you click on those, just shared what worked for me*)

You can find tons of prep-guide online for this certificate, it takes plenty of time to filter. Make sure when you are searching that the content should target SAA-C02, because there are many obsolete material out there. I preferred video material and I had two conditions, it should be around 6-8 hours (there are ones above 20h) and should be free (or really cheap). In the end I settled with [AWS Certified Solutions Architect - Associate (SAA-C02)](https://learning.oreilly.com/videos/aws-certified-solutions/9780136721246/) from O'reilly, having a free access to the learning platform through UBS. (As an alternative, there is a [free course](https://www.youtube.com/watch?v=Ia-UEYYR44s) on Youtube from freeCodeCamp which got excellent feedbacks too)

The O'reilly course takes 6+ hours. It can be that short because it does not bother to explain all the details (e.g.  networking). There are no hands-on labs included, so all you get is pure data and information on services, system setups, integrations in a neatly organized way. It does a good job to explain the basic scenarios and gives answer to the most frequently asked questions on the exams. I really liked that after every main topic it dissected a couple of real-life exam questions with detailed explanations about the correct answer.

Being extremely dense and packed with information you won't remember half of it after watching once. I realized that I need to take notes and restructure the information to make it stick (my [notes](https://docs.google.com/document/d/1ZNqCLrK7gRroSFAW-1OPIV1A2_XPEvGX4_6IMk1PdW0/edit?usp=sharing) on Google Drive). This obviously takes more time but later I turned many times to my notes and helped me a lot in the learning process. 

Some topics is hard to digest because of references that aren't introduced. To fill the gaps for the low level things I used this course: [AWS Solutions Architect Associate (SAA-C02) Exam Prep Course - 2021 UPDATED!](https://learning.oreilly.com/videos/aws-solutions-architect/9781800567054/). This course is slower-placed and explains everything in a detailed (albeit a bit verbose) way.[](https://learning.oreilly.com/videos/aws-certified-solutions/9780136721246/)

It took me  roughly 12-13 hours to get through the course with active note taking.

## Practice exams

After you finished the course you will have all the raw information which needs to be polished with practice exams. Practice exam simulates real exam as close as possible. With the set of questions you can identify recurring topics, you can get use to the way to navigate between questions and a built-in timer helps with time management and calculates a score at the end. The most important feature is the review mode where you can filter down to your failed answers and get an explanation on the good answers usually with some material linked. 

There is no shortage of practice exams on the net. I just picked the one with the best rating on Udemy: [AWS Certified Solutions Architect Associate Practice Exams](https://www.udemy.com/course/aws-certified-solutions-architect-associate-practice-tests-k/) ($10.99 - you should wait for a sale!). This contains 6 practice exams, I solved all plus reviewed all my wrong answers. The goal is that you should score above 80%. To be honest I scored around 50-60 on most or these practice exams, so I wanted to practice more. I bought another set of exams from [Whizlabs](https://www.whizlabs.com/learn/course/aws-solutions-architect-associate/153) ($6.97) just to be on the safe side. This provides another 7 exams plus questions targeting a specific service. I solved only 3 main test and some of the topic-centric ones then my final exam was due. At that time I could confidently score around 80%.

# Exam

The exam ($150) consist of 60 questions and takes 130 minutes (you can request extra 30 mins if you are a non-English speaker). You can schedule your exam through [PSI](https://awsavailability.psiexams.com/) or [Pearson VUE](https://home.pearsonvue.com/Clients/Amazon-Web-Services.aspx), you can postpone the date twice for free. COVID made the online-proctored exams very popular, this provides you the benefit of doing the exam from home albeit with many restrictions. I chose the online exam, which turned out to be of a headache due to the buggy online tools they force you to use. The online exam works the following way, you need to download a secure browser to connect to the questions, you should have a camera turned-on through the exam which records you not doing any suspicious thing. Your laptop must not run any other application. You should be alone in a closed room, no noise, no drink, no food, you can't leave your desk, your hands should be always visible. The exam starts with a proctor checking your ID and your place, you should turn the camera around to show your desk, which should be empty, no device around, you must place your phone somewhere far. This is all good so far but for me the secure browser proved to me a 

# Resources

You can find here all the resources I used.