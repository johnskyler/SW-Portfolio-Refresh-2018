---
title: "Idea to Feature: Designing a multi-view interface to visualize content."
category:
- casestudy
- transpose
---
## Introduction

Transpose was designed from the ground up to accommodate the virtually limitless range of use cases an information management tool might encounter during use. Accordingly, its strength needed to be in its flexibility as well as its ease-of-use. This set us up for a challenge: We had to avoid abandoning our users to an unacceptably overloaded interface (make-it-do-all-the-things!), and simultaneously, we needed to facilitate interaction between a user and their data, regardless of the task they were trying to achieve.

Clearly the limited ‘Template list → Record list for a given template → Record detail page hierarchy’ we had been using up to that point was not going to cut it.

As such, we chose to design multiple view types to complement the Record List view, enabling the user to interact with multiple records at a time, in a variety of ways. But how could we track the information management challenges our users were bringing to the table?

<ul class="fonts-body-text-article"><li>My solution was to distill the substantial user research we continuously brought in (customer interviews, surveys, and in-app analytics) into a list of the 100 most frequent ‘data tasks’. A data task answered the questions, “What type of user is this?” and “Why is the user looking at this collection of records at this time?” These were things like:
</li><li>“I use Transpose for scheduling at my business, and want to change/create an event.”
</li><li>“I track my office’s finances using Transpose, and want to add a new line item to a table of expenses.”
</li><li>“I use Transpose to plan projects, and want to change who a task is assigned to.”
</li></ul>


> ![](/images/Idea%20to%20Designed%20Feature/view1.png)
> ![](/images/Idea%20to%20Designed%20Feature/view2.png)
> ![](/images/Idea%20to%20Designed%20Feature/view3.png)

## Designing Individual Views

With the list of top data tasks finalized, we needed to distill the large number of ways a given individual might be using Transpose at a given time into an accomplishable set of design targets. Working through the list of data tasks, I generated a list of views by beginning with “Record list” and adding an additional view each time the data task couldn’t be accomplished. Refinement of the resulting list became a recommendation of six primary required view types. These were:

<ul class="fonts-body-text-article"><li>Card View
</li><li>Kanban View
</li><li>Table View
</li><li>Calendar View
</li><li>Gantt chart View
</li><li>Analytics 
</li></ul>

I further fleshed out each view type with additional capabilities based upon the type of user specified by the design tasks which had inspired its creation.Armed with a list of functional requirements for each view to be designed, it was time to begin iterating on how the data would be visualized.

Each view had a primary way of organizing a user’s content based on one of the fields in the template — a date field, for instance, could be used to arrange records on a calendar view — and some views could accommodate multiple fields as editable by interacting with the view itself. For example, a project’s due date could be changed by dragging the right end of the item in Gantt Chart view. Or who it was assigned to could be changed via a popover, etc.

> ![](/images/Idea%20to%20Designed%20Feature/view4.png)
> ![](/images/Idea%20to%20Designed%20Feature/view5.png)
> ![](/images/Idea%20to%20Designed%20Feature/view6.png)

## Designing the Switcher Popover

Having designed multiple views to accommodate all of the ways our users were integrating Transpose in to their lives, we still needed to be able to switch easily between them on the fly. A project management data set could benefit equally from a Kanban view as a Gantt chart view and both might be used in a single sitting, after all. 

I needed to be confident of the full functionality of each view, so I worked with our developers to only enable views as supported by the fields a user had chosen for a given template. 

With that confidence in place, we still had to show users which views were possible currently, enable switching between them, and indicate that other, disabled view types were available. Simultaneously, the popover would need to create an association between view availability and the fields in a template.

> ![](/images/Idea%20to%20Designed%20Feature/popover1.png)
> ![](/images/Idea%20to%20Designed%20Feature/popover2.png)
> ![](/images/Idea%20to%20Designed%20Feature/popover3.png)
> ![](/images/Idea%20to%20Designed%20Feature/popover4.png)

The resulting interface was the above popover. By this stage, the engineering team was confident they would be able to predict which type of view a user would choose based its structure. We now could be confident the initial view a user encountered after constructing a template would make sense to them. As such, a deemphasized (in comparison to a user’s records) “View” button with a dropdown caret was used to summon the popover — with interface continuing to update underneath — until being dismissed when the user clicked outside of it.

Together the design of the data-sensitive views and the view switching popover enabled users to complete tasks an order of magnitude more complex from the multiple-records view. It also reduced the amount of time users needed to spend editing individual records. The result was an increase in both the overall amount of time a given user spent on Transpose and the satisfaction with which they rated their time on the platform, driven by a decrease in the amount of cognitive effort required to complete individual tasks within a given view.