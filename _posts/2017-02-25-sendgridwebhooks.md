---
title: 'Using SendGrid Webhooks to Implement a Client’s Platform'
subtitle:
date: 2017-02-25 14:00:00
location:
description: Using SendGrid Webhooks to Implement a Client’s Platform
featured_image: '/images/post/sendgrid.jpg'
--- 

Creating awesome end-user experiences while trying to exceed expectations, is every developer’s dream. The road ahead is bound to be a rollercoaster ride. A ride full of bugs, some roadblocks, testing and even failing once in a while. The good news is, the road is also bound to be full of joy and learning. That is what I love about my job.

I always enjoy working on a team, although that is not always possible. It depends on the company size, project deadlines and resource allocation, to mention some examples. For this particular project, I was asked to work on my own. Even though I was intimidated at first, I decided to not let my fears overshadow a window of opportunity, and so I took on the challenge. Here is my story.

### Beginning Stages: Expect the Unexpected

Having a project in mind is exciting… until you hit those roadblocks.

> 1 week…
> 2 weeks…

Sometimes, it felt as if developing was taking me 10 steps ahead, while testing was taking 20 steps back.

Our platform was already setup. We were already using SendGrid’s web API to send emails through our web application. Our goal was to provide admin-level users with the flexibility of not only sending emails, but also be able to track them from beginning to end.

The solution? Digging deeper and finding a way to integrate with SendGrid.

There were two main purposes when the goal for this project was set:

1. To enhance our platform’s dashboard functionality, and
2. To provide admins with more resources and better ways to use our web application

Of course, as soon as the project began, a challenge presented itself. The SendGrid version (v2) in place, was already “old” and SendGrid’s API v3 was recommended. To take full advantage of SendGrid’s Web APIs and Event Webhooks, an upgrade was needed. This added unexpected tasks, and a roadblock to the list. A few steps needed to happen before completing the integration:

1. SendGrid migration from v2 to v3
2. Email implementation throughout our web application
3. Testing of the implementation

Next, it was decision time: to use the API or to use the event webhooks for the integration?

Thankfully, after doing some research, the answer was a few emails away. The folks over at SendGrid’s DX Team were responsive and very supportive along the way (even when responding to issues on SendGrid’s PHP helper library [Github repo](https://github.com/sendgrid/sendgrid-php) -which we use).

The final decision: Integrating with SendGrid using the event webhooks to help achieve our goal was the best way to go for our use case.

### What is a Webhook?

In short, webhooks are called reverse APIs, or technically speaking a web callback. Webhooks enable apps to push data to other applications when it becomes available. Some of these web callbacks could also happen when the data has reached certain batch size. It all depends on the application that sends the data and whether or not they give their users the flexibility to choose how often the data is sent.
In our case, SendGrid either posts events every 30 seconds or when the batch size reaches 768 kilobytes, whichever takes place first. You can check this link for more information on SendGrid’s Event Webhook Requests.

### Preliminary Tasks

At this point, one thing was clear, we were going to be using SendGrid’s webhooks for the integration. My preliminary tasks list looked something like this:

#### Migrating SendGrid from v2 to v3 API
Even though SendGrid’s v2 would have worked, upgrading to v3 was our best option. This is because v3 has the capability to deliver events as JSON arrays. It also provides more data with certain events.

#### Event notifications URL setup
This must be done in order to be able to receive notifications from SendGrid’s API. An endpoint file was also setup and configured to capture data via HTTP POST.

#### Endpoint file setup on SendGrid
Your HTTP POST URL can be setup within SendGrid’s account: Mail Settings > Event Notification > Configuration.

#### Integration testing
The endpoint file is then tested simply by clicking on the “Test Your Integration” button. When clicked, SendGrid sends a simulated POST of events to the callback URL that was defined before.

Here is an example of a decoded JSON array containing SendGrid’s email events:

```json
Array
(    
  [0] => Array        
     (            
         [meeting_name] => myMeeting1            
         [ip] => 00.00.00.00            
         [response] => 250 message accepted for delivery        
         [event] => delivered            
         [email] => myemail@something.com            
         [timestamp] => 1485811139            
         [uID] => 01130        
     )
     
 [1] => Array        
     (            
        [meeting_name] => myMeeting1 
        [event] => processed            
        [email] => myemail@something.com
        [timestamp] => 1485811026            
        [uID] => 01130        
     ) 
)
```

#### Additional testing

This was performed via cURL in order to ensure the endpoint file for the integration was working as expected. You can see an example of the endpoint file on our end:

<div><script src="https://gist.github.com/paoga87/47649d822cb7d2e1fe083441e77e2ed3.js"></script></div>

Thanks to this project, I was able to contribute to SendGrid’s documentation on Github, you can also see this example on their docs site.

#### Platform’s back-end setup
Technology was developed on the back-end to support the integration. We work on a LAMP stack, therefore using SendGrid’s PHP Helper Library was helpful.

#### Front-end implementation
Development, planning, and layout of the event data was needed to be able to efficiently display the information to end-users.

#### Beta Testing
Use cases were developed. Testing included hours of not only testing, but also discovering and fixing bugs.

---

### Other Stages, Stages in Between

Many subtasks were omitted previously, for the sake of the reader. Sometimes there is a lot of work (and stages) happening behind scenes to get to a final result.

During my early days at my current job, and even before I took on this challenge, my boss sent me an email with the following PDF attached:

![Developing a growth mindset — a gift from my boss pinned on one of my desk walls.](/images/post/sendgrid-pdf.jpg)

I printed the PDF. The message on this piece of paper really caught my attention, and immediately became one of my favorite wall decorations. One thing I did not know then, is that as simple as it seems, the message on it was going to help me accomplish ANY challenges; including this project.

I admit it. I probably went through so many different “mind stages” for every single “INSTEAD OF…” and changed my mind after “SAY[ing] THIS…” every time. I learned to confront challenges with a more positive mentality, which helped me focus to manage the project and writing code. And most importantly, I enjoyed the rollercoaster ride.

### Final Stage: Project Completion

When a project is complete, it means the project has only just started. Once you have tackled a task, you want to implement it over and over to make it work even better. It does not matter if is too easy or too hard.

You can do it.

Challenges are everywhere.

Take them on.

You will enjoy it too.