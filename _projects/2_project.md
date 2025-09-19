---
layout: page
title: Cost and Punishment Proximity
description: Investigating how the timing of negative outcomes shapes decision-making in rodent models at the Indian Institute of Science, Bengaluru.
img: assets/img/3.jpg
importance: 1
category: work
giscus_comments: true
---

This project dives into a question we all face in different forms: **When faced with an unavoidable negative event, is it better to get it over with quickly or postpone it?** While we know a lot about how people and animals value delayed _rewards_ (most prefer a small reward now over a larger one later), we know far less about how we handle delayed _punishments_.

This research aimed to find out whether the anxiety of waiting for a negative outcome—what we might call **"dread"**—is a more powerful driver of choice than the immediate discomfort of the punishment itself. To do this, I designed and built a fully automated system to ask this very question to mice.

---

### The "How": Building a Fully Automated T-Maze

To precisely measure a mouse's decision-making without human interference, automation was key. Manually running these experiments would be slow and could introduce biases from the experimenter. So, the first major objective was to develop and validate a custom automated T-maze.

The system was designed to handle every aspect of the trial:

- **Tracking:** Five infrared (IR) sensors tracked the mouse's position, logging exactly when it started a trial, made a choice, and reached its goal.
- **Control:** An Arduino microcontroller served as the brain, running custom logic to control the experiment.
- **Actuation:** Servo-controlled doors opened and closed to guide the mouse, preventing it from turning back after making a choice.
- **Reward & Punishment:** Solenoid valves delivered a precise sucrose water reward, while LED panels delivered a bright, unpleasant light as the punishment.

This setup allowed for the collection of highly accurate, timestamped data, revealing not just _what_ the mouse chose, but also _how long_ it took to make that decision.

<div class="row justify-content-sm-center">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/t-maze-photo.jpg" title="The Automated T-Maze" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/wiring-schematic.jpg" title="Control System Schematic" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>Left:</b> The custom-built automated T-maze apparatus used in the experiments. <b>Right:</b> The wiring schematic showing the connection of sensors, servos, and LEDs to the Arduino control unit.
</div>

---

### The "Choice": A Difficult Choice for a Mouse

Once the system was built and validated, it was time to pose the central question to the mice. In the experimental phase, each mouse was presented with a choice in the T-maze:

- Go down **Path A**: Receive an immediate sucrose reward, but also an **immediate** (advanced) flash of bright light.
- Go down **Path B**: Receive the same immediate sucrose reward, but the flash of bright light is **delayed**.

In both cases, the reward was the same and the punishment was identical and inescapable. The only difference was **time**. If mice simply disliked the punishment, they should have preferred the delayed path. But if the _anticipation_ of the punishment was worse, they might choose to get it over with.

---

### The Surprising Results: A Paradoxical Preference

The findings were both clear and fascinating, revealing a deep conflict in the decision-making process.

#### Finding #1: Mice Prefer to "Get It Over With"

The mice showed a powerful and statistically significant preference for the path with the **advanced (immediate) punishment**. They consistently chose to face the unpleasant light right away rather than wait for it. This strongly suggests that the psychological cost of anticipating the delayed punishment—the "dread"—was more aversive to them than the punishment itself.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/choice-selection-graph.jpg" title="Choice Preference" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decision-time-graph.jpg" title="Decision Latency" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <b>Left:</b> Mice overwhelmingly chose the "Advanced" punishment path over the "Delayed" one. <b>Right:</b> Paradoxically, they took significantly longer to decide when they chose their preferred "Advanced" path.
</div>

#### Finding #2: The Paradox of Hesitation

Here's where it gets truly interesting. Despite their clear preference for the immediate punishment path, the mice **took significantly longer to make a decision** when they chose that path.

This hesitation reveals a profound cognitive conflict. While their ultimate goal was to minimize the period of dread (by choosing the immediate path), the immediate prospect of the punishment created a conflict that required more time to overcome. It's a classic "approach-avoidance" conflict playing out in real-time.

---

### The Takeaway

This research successfully demonstrates a key dissociation in decision-making:

> The factors that drive our **ultimate preference** (like minimizing long-term anxiety) can be different from the factors that influence the **immediate execution** of that choice (like overcoming the aversion to an imminent negative event).

By developing a robust automated platform, this project provides a powerful new framework for studying the neural basis of decision-making under aversive conflict. It opens the door for future studies to explore the specific brain circuits involved, with potential implications for understanding neuropsychiatric conditions like anxiety disorders, where the evaluation of future negative consequences is often disrupted.
