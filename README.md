| Date              |          |
|:------------------|:---------|
| 2 October 2023 | Assigned |
| 16 October 2023    | Due      |
| Status            | [![GatorGrader](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml) |

# TURNABOUTS TO TAME TRAFFIC? `term-world` CITIZENS' TAKES ARE TEPID

**Reported by `The Reporter` from `Ix` on  2 October 2023**

(Ix) - Given the recent influx of individuals into `term-world`, traffic has been impossibly inundated, incensing impatient idlers who are, in a word, irate. The irritating impact of this impotent infrastructure was immediately identified by our incredible Mayor when he involved himself with an important inspection of the near-infinite incidence of intolerable wait times. He said in an insightful insider interview implicating inept engineers: "I'm incredulous! It's irresponsible, immoral, insidious!"

It was during this deep-dive that he delved into his daring directive to delete the downright dismal deadlock that has defiantly drawn speed demons and doddering Sunday drivers alike to a dead standstill. We've deliberately dedicated the space down below to the disclosure of his dynamic declaration:

"It's me, your Mayor! You, pen jockey, you're getting all this down, right? That was my catchphrase. It's very important. Please try and keep up. For me. Your Mayor. Anyway, where was I?"

"Ahem, in my capacity as your Mayor I've spent a tireless hour mulling over how we might fix this teeny-weeny little...er, what's a word that says, 'I see we have a problem here, but I'd rather not call it a problem'? Oh yeah, that's good...I, your Mayor, was mulling over how we might fix this teeny-weeny little traffic hiccup. And I, your Mayor, have come up with a brilliant solution!"

"You, my fair citizens, did such a wonderful job of enacting my incredible neighborhood economy proposal that I, your Mayor, figured that if you could handle that, then you could surely handle this! Hey, glasses, are you sure you're getting all this? It's important to butter the people up, you know. That's like, Mayor 101."

"Actually, I think that's everything. Let's see, we have a hiccup, you can fix it, yada yada...yeah, that should do. You got my catchphrase, right? Gotta have a soundbite for the people. Okay, good. Now scram."

## Overview

In this set of activities we cover:

* working collaboratively using Github
* branching
* merging
* issuing "Pull Requests"
* exploring a new programming concept, control statements in:
  * conditional statements
  * booleans
  * `while` loops

You'll complete several main tasks:

* Fixing four `Stoplight.py` files to work according to specifications below
* Repairing a `Car.py` to drive from point-to-point
* Returning a `Bus.py` to service (work order below)

## Learning Outcomes

In this assignment you will learn:

- Writing conditional statements in Python
- Writing repeatition statements in Python

You will also continue to practice:

- Command line navigation
- Running Python programs
- Using version control
- Technical writing in Markdown

These assignment learning outcomes contribute to the following course learning outcomes described in the [course syllabus](https://github.com/cmpsc100-allegheny-college/course_information):

1. Apply Python programming principles to execute and explain computer code that implements interactive, novel solutions to a variety of computable problems.
2. Release code consistent with industry-standard practices using professional grade IDEs, command line tools, and version control tools.
3. Analyze and suggest revisions to existing Python language code to improve or add functionality.

## Completing `traffic-circle` content

Each file contains more specific instructions _particular to that file_. The general specifications appear below.

### `Stoplight.py` files

Each directional folder features a `Stoplight.py` file. Each works a slightly different way, but they're all in need of serious repair to put them back in working order.

**Every stoplight uses a version of the variable light; this variable can be used to store one of the following four emoji values to represent the light's current status: 🟢🟡🔴⚫. All variables will be `string` values unless otherwise noted**

#### `north`

A standard stoplight, cycling through each light once.

* If the light was 🔴, it becomes 🟢
* If the light was 🟢, it becomes 🟡
* If the light was 🟡, it becomes 🔴

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🟢,🟡,🔴  |

#### `south`

A typical pattern for less-used roads, flashing red.

* If the light was 🔴, it becomes ⚫
* If the light was ⚫, it becomes 🔴

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🔴,⚫  |

#### `south-east`

A light which displays a given signal for a duration of time, accompanied by the correct crosswalk signal.

* If the light was 🔴 for `15` seconds, it becomes ⚫ and displays the 🚶 crosswalk symbol
* If the light was ⚫ for `15` seconds, it becomes 🔴 and displays the ✋ crosswalk symbol


|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🔴,⚫  |
|`countdown`| `int`, ascending  |
|`crosswalk`|🚶,✋  |

#### `south-west`

A simple light to sense a crosswalk signal.

* If the crosswalk signal is 🚶, the light becomes 🔴
* If the crosswalk signal is ✋, the light becomes 🟢

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🔴,🟢  |
|`crosswalk`|🚶,✋  |

#### `east`

A light with a timed turn signal.

* If the light was 🔴, it becomes 🟢 with a turn signal (➡️)
  * The signal picture is handled for you, all you need to do is complete the logic
  * The timing is also handled for you -- again, the logic is the key here
* When the turn signal expires after `5` seconds, the light stays 🟢
* If the light was 🟢, it becomes 🟡
* If the light was 🟡, it becomes 🔴

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🟢,🟡,🔴  |
|`turn`   | `boolean` |
|`hold`   | `boolean`  |

#### `west`

Another, simpler, timed light in which green and red last for `5` seconds. Here, the timing is also handled for you -- all you need to do is string the logic together.

* If the light was 🟡, it becomes 🔴
* After holding for `5` seconds, a 🔴 becomes a 🟢
* After holding for `5` seconds, a 🟢 becomes a 🔴

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🟢,🟡,🔴  |
|`timeout`   | `boolean` |

#### `north-west`

A full crosswalk light system in which the light slowly becomes red after a crosswalk signal has been activated

* If the light is 🟢, the crosswalk becomes ✋
* If the light is 🟡, the crosswalk stays ✋
* If the light is 🔴, the crosswalk becomes 🚶

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🟢,🟡,🔴  |
|`crosswalk`| ✋,🚶 |

#### `north-east`

Equipped with a system to detect the number of people queued up at a crosswalk, the light only turns when more than `5` people are at a crosswalk.

* If the light is 🟢 _and_ there are greater than `5` people waiting, the light turns 🟡
* If the light is 🟡, the light becomes 🔴
* If the light is 🔴, the crosswalk becomes 🚶 and resets the `people_waiting` count to `0`

|Variable | Value(s) |
|:--------|:---------|
|`light`  | 🟢,🟡,🔴  |
|`crosswalk`| ✋,🚶 |
|`people_waiting`| `int`, ascending |


### The `Car.py` and `Bus.py`

Each vehicle behaves slightly differently.

#### `Car.py`

* Goes through any 🟢 light
* Stops if lights are 🔴 or 🟡
* At a 🟢➡️, the `Car.py` should prompt the driver for a new direction
  * Directions are limited to `north`, `south`, `east`, and `west`
  
|Variable | Value(s) |
|:--------|:---------|
|`signal`  | 🟢,🟡,🔴  |
|`move_to`|`input` (i.e., `string`) |


#### `Bus.py`

* Goes through any 🟡 or 🟢 light and keeps doing so until it hits a 🔴
* Stops if lights are 🔴

It only follows a set route of `north`,`south`,`east`, and `west`. The `Bus.py` also previews some content we'll get to in time. However, you can know that the process
by which the `Bus` should move forward is (in this order):

```python
Bus.__move_bus(direction)
direction = Bus.__get_direction()
stoplight = Bus.__get_light(direction)
Bus.__report(direction, stoplight)
```

This file uses a `while` loop which _repeats_ procedures. Minus some small logic, the above is pretty much the full functionality of the vehicle.

### Collaborative reflection

**Create one branch called `reflection` to capture your work on this section of the assignment; all members should contribute to the same branch.**

When all of the above tasks completed, finish the collaborative reflection located in the `office`.

## Improvement Suggestions

Here are some suggestions for improvements you may use:

|Improvement Suggestions |Description     |
|:--------------------|:------------------|
|Create an emergency vehicle      |Add a new emergency vehicle that goes through lights differently then `Car.py` and `Bus.py` |
|Make a bicycle      |Add a bicycle that goes through traffic with more care then a automobile would |
|Make the `Bus.py` stop for new passengers      |Make the `Bus.py` stop for passengers as it drives by with 🚶 or ✋|
|Add new signals for construction   |Make the `Bus.py` and/or `Car.py` act differently for 🚧 |
|Add New signals for pedestrians   |Make the `Bus.py` and/or `Car.py` act differently for 🚶 or ✋|
|Add New signals for yellow lights   |Make the `Bus.py` and/or `Car.py` act differently for 🟡 |
|Create a new traffic light         |Create a new traffic light problem with the code used in other lights |
|Wait for timed lights in real time |For a light with a timer or countdown make users wait out the duration of the timer |

To make an improvement proposal, you must _create an issue_ on this repository. Do so by:

* clicking the `Issues` tab at the top of the page.
* clicking the green `New Issue` button
* selecting the `Improvement Proposal` template 

**Make sure to link your issue with the pull request you used to make your actually improvement.**
* If you pursue an improvement not listed above, you must discuss your improvement with a member of the Mayoral staff.
  
## Code Walkthrough

Code walkthrough a type of peer review where the writer of the code leads the process. The goal of code walkthrough is to create a shared understanding of created code, to detect any potential flaws in the code and to correct them. 

During the lab sessions on October 6th and October 13th, each member of the neighborhood will engage in the code walkthrough with TLs and the instructor. In this walkthrough, we will specifically focus on: 
- conditional statements;
- loops.

Each member of the neighborhood will be asked to open a Python program that they modified and explain parts of the program involving `if`, `elif`, and/or `while` statements.
During the walkthrough, TLs and the instructor will also ask pertinent questions about the code.

**Participation in the code walkthrough is required for this assignment. `Complete` status for the assignment can not be obtained without engaging in a walkthrough.**

## Evaluating `traffic-circle` Content

In addition to a check from the walkthrough, which evaluates understanding of the new topic of the week - `control statements`, the content for this week (and most every week to follow) is outfitted with a grader program that can be used to evaluate the rest of your work for this two week assignment. Again, in order to run the grader for this assignment's work, you will need to be in the topmost level of the `traffic-circle` folder.

Once there, run the command:

`gatorgrade`

The grader will take a few minutes to do its work, but once it's complete the program will populate your terminal window with a series of checks that gauge the overall "completeness" of your work.

There are 28 grader checks in this assignment. Participation in the walkthrough counts as an additional 29th check. All 29 checks (all of the grader checks and the walkthrough) must be completed by the due date to receive baseline credit for this assignment!

## Backup Policy Reminder

**While we may use this server to store code, you are responsible for using GitHub as your main backup.**

In the event that the `term-world` server goes down for any unforeseen reason, your work may be lost. Though this server is backed up on a regular (i.e. weekly) basis, there is no guarantee that up-to-the-minute data for your work will be restored.

Remember: to err is human; to back up your work is *divine*.
