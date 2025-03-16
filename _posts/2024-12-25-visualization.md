---
layout: distill
title: Scalable Feedback Through AI and Visualization
date: 2024-12-25
description: Discover how language models and visualization tools are reshaping the way instructors engage with students, making programming education more scalable, impactful, and learner-centric.
featured: true
category: research
tags: visualization cognition
visualization: true

authors:
  - name: Xiaotian Su
    url: "https://xiaotiansu.github.io"
    affiliations:
      name: ETH Zurich

toc:
  - name: "Classroom 1.0: code clustering and monitoring students' progress in real-time"
  - name: "Classroom 2.0: enpowering instructors with AI-driven insights"
  - name: "From overwhelmed to empowered: How can AI become the co-educator?"
  - name: Balancing Automation and Autonomy
  - name: Creating a Feedback Loop Between AI and Educators

bibliography: 2024-12-25-visualization.bib
---

As programming classrooms continue to expand—both in physical size and across online platforms—the challenge of supporting large-scale learning environments becomes increasingly urgent. For example, introductory computer science courses at institutions like UC Berkeley and the University of Washington regularly enroll over a thousand students per term. This growth poses a challenge for educators: how to provide timely, personalized, and meaningful feedback to students who need help. Traditional methods, such as addressing students who raise their hands, are effective in smaller settings but falter when scaled to classes of hundreds or more. Over the years, innovative tools have emerged to help instructors manage this complexity. More recently, the advent of Large Language Models (LLMs) has ushered in transformative changes in how feedback can be generated, delivered, and scaled. This blog explores how these advancements are empowering educators to reimagine their roles and create new opportunities for engaging learners.

### Classroom 1.0: code clustering and monitoring students' progress in real-time

Before the advent of generative models, researchers explored ways to manage and analyze students' programming solutions at scale, focusing primarily on clustering techniques for massive classes. For instance, **OverCode** utilized both static and dynamic analysis to cluster similar solutions, enabling instructors to further refine and group thousands of solutions based on various criteria <d-cite key="glassman2015overcode"></d-cite>. However, it was primarily designed for post-hoc analysis, lacking real-time feedback capabilities and the means to monitor students' progress over time.

Building on the need for real-time support, **Codeopticon** introduced an interface allowing programming tutors to monitor a few hundred learners simultaneously and chat with them in real-time <d-cite key="guo2015codeopticon"></d-cite>. At a glance, tutors could observe how learners were editing and debugging their code and identify errors encountered. Despite its innovative approach, scaling feedback remained a challenge, as instructors still had to individually review each student's code.

To address these challenges, **VizProg** was developed to provide a more scalable and intuitive real-time visualization tool. It represented students’ statuses as a 2D Euclidean spatial map, encoding their problem-solving approaches and progress <d-cite key="zhang2023vizprog"></d-cite>. This visualization allowed instructors to explore both the temporal and structural evolution of students’ code and identify opportunities for feedback. However, the tool's scalability was limited, it can be applied to around 100 to 200 solutions; instructors found it overwhelming when a large number of students began working simultaneously. Moreover, understanding specific content often required manually selecting areas and examining raw code.

<div style="text-align: center;">
  {% include figure.liquid loading="eager" path="assets/img/blogs/VizProg.png" %}
  <figcaption style="text-align: center;">Comparison of different systems in VizProg</figcaption>
</div>

### Classroom 2.0: enpowering instructors with AI-driven insights

With the rise of LLMs, researchers have started leveraging these technologies to overcome the limitations of earlier tools. **CFlow**, for example, utilized LLMs for post-hoc analysis by generating line-level error information for student code <d-cite key="zhang2024cflow"></d-cite>. By providing semantic-label abstractions and a color-coded histogram, it helped instructors identify common mistakes more efficiently when presented with over 6,000 submissions. Similarly, **VizGroup** harnessed LLMs to recommend event specifications, enabling instructors to monitor key correlation patterns between collaboration metrics and coding tasks for over 100 submissions in real-time <d-cite key="tang2024vizgroup"></d-cite>. Beyond these, tools like **SPHERE** directs instructors’ attention to critical student issues, offers guided control over LLM-generated feedback, and employs visual scaffolding to enhance feedback verification and quality <d-cite key="tang2024sphere"></d-cite>. These innovations illustrate how the integration of LLMs is transforming the way instructors interact with student solutions, making feedback and analysis more scalable and actionable.

Interestingly, all the tools mentioned above were designed specifically for introductory programming courses and evaluated primarily using Python-based datasets. Looking ahead, there is a pressing need to expand these innovations to cater to a broader range of programming topics, such as web development, data science, and other specialized areas. Additionally, future tools should address the diverse needs of learners across different experience levels, including intermediate and advanced programmers, to ensure more comprehensive and inclusive support in programming education.

<div style="text-align: center;">
    {% include figure.liquid loading="eager" path="assets/img/blogs/SPHERE.png" %}
    <figcaption style="text-align: center;">Workflow overview of SPHERE.</figcaption>
</div>

### From overwhelmed to empowered: How can AI become the co-educator?

As we look ahead, the next frontier for programming education lies in creating an ecosystem where AI transcends its role as a mere assistant to become a true co-educator. This vision demands a shift from tools that provide one-off solutions to those that foster dynamic, ongoing collaboration between instructors, learners, and AI systems.

#### Balancing Automation and Autonomy

A key challenge in designing such systems is striking the right balance between automation and autonomy. While fully automated feedback mechanisms powered by LLMs can scale effortlessly to large classrooms, they risk oversimplifying nuanced pedagogical needs. On the other hand, systems that rely heavily on instructor input may fail to address the scalability issues they are meant to solve. The ideal solution lies in hybrid approaches: leveraging AI to handle routine tasks, such as identifying syntax errors or generating initial feedback drafts, while giving instructors the flexibility to refine and customize these outputs to suit individual learners' needs.

#### Creating a Feedback Loop Between AI and Educators

The long-term vision for programming classrooms involves establishing a symbiotic feedback loop where AI systems learn from instructors just as instructors benefit from AI insights. For example, instructors could provide the AI with detailed annotations or examples of effective feedback, such as suggesting alternative coding strategies to encourage creativity or asking probing questions to foster deeper collaboration among learners working in groups. These annotations might highlight when feedback should focus on enhancing problem-solving skills, encouraging innovative approaches, or building teamwork dynamics rather than merely correcting syntax or logical errors. Over time, the AI could analyze patterns in this instructor-provided feedback to refine its models, learning to prioritize actionable insights that inspire learners to explore diverse solutions, communicate more effectively, and engage in meaningful collaboration. This iterative process ensures the AI not only adapts to educators' evolving pedagogical strategies but also complements their expertise by amplifying the aspects of teaching that promote a richer, more interactive learning environment.

In the future, AI does not replace instructors but amplifies their ability to teach effectively and creatively. Together, instructors and AI co-educators can create a learning environment that is scalable, adaptive, and profoundly impactful.
