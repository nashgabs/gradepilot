# :bulb: Help and advice

## Adding new items
To create a new assignment you can choose from one of the pre-made templates or make your own.

First, go to the *Term 1* or *Term 2* page, select one of the module views or the _Overview_ and click on the blue **New** button to make your own assignment, or you can click on the dropdown box :arrow_down_small: next to this to select a template.

Next, fill out all of the editable fields:

- Assignment
- Module
- Release date
- Deadline
- Weight
- Late penalty
- Status
- Memo (for any additional notes you’d like to record)

You can change the completion status of items by dragging them into the categories in the _Overview_ panel, or manually change the status by opening the item and clicking on the _Status_ field.

To update an item’s marked grade, simply enter a value in the _Raw grade_ field and press Enter.

## :question: FAQs

<details>
  <summary> What if I need to add an extra term?</summary>

**Warning: Some of the steps are quite involved. Please follow these steps carefully or the calculator may break.**

To create a new term:

1. In the side menu, select the three dots … beside the page titled **Template** and select _Duplicate_ from the list. Then, rename it to something meaningful to you (e.g. “Term 3”).
2. Add your assignments to this term as you would usually. 

>:bulb:__See the '[Adding new items](#adding-new-items)' section in this guide__.

3. Open the page titled **Grade Calculator**. To the right of the table headings select the plus symbol + and click on the property type _Relation_. Select the page you just created in Step 1 (e.g. “Term 3”) then click _Add relation_ and _Done_.
4. _Duplicate_ the property named _T2 selected modules_ and rename it appropriately, e.g. “T3 selected modules”.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Module*.
     * Select _Calculate_ and change this to _Show original_.
5. _Duplicate_ the property named _Sum of weights in T2_ and rename it.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Weight*.
     * Select _Calculate_ and change this to _Sum_.
6. _Duplicate_ the property named _Weighted grade total in T3_ and rename it.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Weighted grade*.
     * Select _Calculate_ and change this to _Sum_.
7. _Duplicate_ the property named _Grade for T2_, rename appropriately and then update its formula with the newly created property names.

> :bulb:__The original formula should look like this.__
>
>  ```jsx
>  round(prop("Weighted grade total in T2") * 1 / prop("Sum of weights in T2"))
>  ```
> **After editing, the formula should look something like this.**
>
> ```jsx
> round(prop("Weighted grade total in T3") * 1 / prop("Sum of weights in T3"))
> ```
8. Update the formula in the property _Completion_ by inserting
  ```jsx
  + prop("Sum of weights in T3")
  ```
  after the _Sum of weights in T2_.

9. Finally, update the formula for _Overall Grade_ by inserting 
  ```jsx
  + prop("Weighted grade total in T3")
  ```
  after _Weighted grade total in T2_.
</details>
<details>
  <summary> How can I update the Grade Calculator with a new item? </summary>
  
Once your work has been marked, you can add it to the _Grade Calculator_ by clicking in the _Term 1_ or _Term 2_ field and linking the assignment.

> :bulb: __Example__
>
> You have just received your grade for the assignment 'Video Presentation' in _Term 1_ and you have updated the mark in the _Raw grade_ field:
> ![](../main/Update_grade_calculator_1.png)
>
> To add it to the _Grade Calculator_, you open _Module 1_ and add a link to _Video Presentation_ in the _Term 1_ field:
> ![](../main/Update_grade_calculator_2.png)
>
  
</details>

<details>
  <summary> Some of my assignments have the same name (e.g. ‘Portfolio’), how can I tell which is the correct one in the Grade Calculator?</summary>

Use the _Selected Modules_ properties to see the module assigned to each assignment. Since the modules appear in the order that they are linked to the calculator you should be able to link all of them and remove the ones which have the wrong module name assigned to them.

> :bulb: __Example__
>
> You have just received your grade for two Video Presentations in Term 2, one in Module 1 and the other in Module 2. You link both pages in the Term 2 field and look to the Selected Modules properties to determine their module names.
> ![](../main/Select_correct_module_1.png)
>

</details>

<details>
  <summary> I have an extension on an item, can I still enter the correct submission date? </summary>

Yes, if you would like to forgive any late penalty on an item then check the box Excuse lateness?. This way you can keep track of which items have an extension and which ones do not.
</details>

<details>
  <summary> It seems like there is a lot of information to provide, are any of the assignment details optional? </summary>

When creating a new item, there are only three essential details to complete for the calculator to work.

The required fields are:

- Assignment
- Module
- Weight

This tool works best when you input all of the information, though. The ability to track other details such as completion status or time remaining will help you to contextualise your progress and reinforce good study habits.

</details>

<details>
  <summary> What if I don’t know how my items are weighted? Or, what if my items all count equally?</summary>

This tool still works for you if you don’t know the exact weights by providing you with a mean average of your performance. To do this, simply set the weights to all of the assignments to 100%.
</details>
