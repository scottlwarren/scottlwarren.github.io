---
layout: post
title: "Considerations for using AI in business processes"
date: 2026-10-30
categories: update
---

# AI is everywhere

It's 2026 - AI is everywhere whether we like it or not. Let me start first with a clear message - AI is a useful tool that I am not opposed to. It can create solid deliverables which can make everyone's life easier; however it does come at the cost of massive resource utilisation and increased prices for everyday electronics.

It seems that the way for a business to become modern is to have an AI USP - be it a chat bot, some tool for creating codebase or AI powered decision making. In my world of analytics, every tool has an AI integration - and with tools such as Claude Cowork and ChatGPT Codex these tools are becoming available for everyone. 

Cowork and Codex are very interesting tools. I've used them to create entire datasets from 'scratch' - and in doing so it can also create any other artifacts for a given task. Want a dataset which emulates a complex insurance claim? Cowork managed to produce 6 spreadsheets containing bordereaux from multiple, fictional insurance agents, along with email chains and internal correspondence seemingly captured from a chat tool like Slack, all within 30 minutes.

Amazing - working on complex insurance claims was one of my favourite roles, and the info produced was scarily accurate. Someone must have put some very commercially sensitive information into a LLM at some point, and it has recreated it with scary accuracy. The privacy of using these tools is not the focus of this blog, but does give lots to ponder on.

# Processes and reproducibility

Business processes are key to success. Our policies, standard operating procedures and method statements give a standardised, uniform way of working that ensures that even highly diverse teams are doing the right thing at the right time. 

My work in science has taught me the importance of reproducibility - a complete stranger being able to pick up your methodology, carry out your experiment and get similar results. Being exposed to data systems and also operational procedures, documentation and accepted methods has shown this is a truly useful transferable skill to have gained. 

In the process of learning new methods, and implementing new data architecture, I have strived through peer review to document what is being done, how to do it again, and where to look when something goes wrong. 

# The AI Blackbox

AI models are progressing (and releasing) at a rate which can be incredibly difficult to keep up with. I've included the chart below from https://aireleastracker.com/ - a site which monitors all of the major players in the space. As of September 2026, 255 models have been released.

<iframe src="https://aireleasetracker.com/embed/releases-by-lab?theme=light" title="Releases by Lab Over Time — AI Release Tracker" width="100%" height="460" style="border:0;border-radius:12px;max-width:640px" loading="lazy"></iframe>
<p style="font:13px/1.5 system-ui,sans-serif;margin:8px 0 0"><a href="https://aireleasetracker.com/analytics?utm_source=embed&utm_medium=referral&utm_campaign=releases-by-lab" target="_blank" rel="noopener" style="color:#6b7280;text-decoration:underline">Releases by Lab Over Time — via AI Release Tracker</a></p>

These releases can be broken down by vendor, and I think the biggest take away from this is that *any AI integration is built on shifting sands*. Models are changing rapidly, and also with very little warning unless you're paying attention. Importantly, we know very little about what is changing - putting change control as an unknown risk which cannot be managed.

![AI agent suggesting to summarise a paper about AI..]({{ 'images/SD_AI.jpg' | relative_url }})

When researching how this is impacting things such as scientific research, I did see the irony above in having an AI chatbot reviewing a paper about AI consistency. Would be very interesting to see how it's summary changes over time...

# How do we solve the black box issue?

My view is to use AI as a prescript tool rather than just a one stop shop with no review. Considering a workflow where AI is assisting someone to statistically analyse a dataset - some would upload their data into a tool like Gemini Notebook, and ask it to create an output. This output - the sole deliverable - is something which gives a quick result, and we can then move onto the next task.

However, for longivity, and also reproducibility, it would be sensible to ask for the codebase itself. Most AI tools are able to do this, and with an analyst reviewing, change controlling and owning the background work, there is scope for future development on existing good grounds. 

Sensible AI use will save headaches in the future, letting new staff pick up work and support businesses moving forward without completely changing the playing field.