# Help and advice

## Adding new items

## FAQs

<details>
  <summary> What if I need to add an extra term?</summary>

**Warning: Some of the steps are quite involved. Please follow these steps carefully or the calculator may break.**

To create a new term:

1. In the side menu, select the three dots … beside the page titled **Template** and select _Duplicate_ from the list. Then, rename it to something meaningful to you (e.g. “Term 3”).
2. Add your assignments to this term as you would usually. 

>:bulb:__See the '[Adding new items](#adding-new-items)' section in this guide__.

1. Open the page titled **Grade Calculator**. To the right of the table headings select the plus symbol + and click on the property type _Relation_. Select the page you just created in Step 1 (e.g. “Term 3”) then click _Add relation_ and _Done_.
2. _Duplicate_ the property named _T2 selected modules_ and rename it appropriately, e.g. “T3 selected modules”.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Module*.
     * Select _Calculate_ and change this to _Show unique values_.
4. _Duplicate_ the property named _Sum of weights in T2_ and rename it.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Weight*.
     * Select _Calculate_ and change this to _Sum_.
5. _Duplicate_ the property named _Weighted grade total in T3_ and rename it.
     * _Edit property_ then select _Relation_ and change this to _Term 3_ (for example).
     * Select *Property* and change this to *Weighted grade*.
     * Select _Calculate_ and change this to _Sum_.
6. _Duplicate_ the property named _Grade for T2_, rename appropriately and then update its formula with the newly created property names.

> :bulb:__The original formula should look like this.__
 ```jsx
 round(prop("Weighted grade total in T2") * 1 / prop("Sum of weights in T2"))
 ```
> **After editing, the formula should look something like this.**

 ```jsx
 round(prop("Weighted grade total in T3") * 1 / prop("Sum of weights in T3"))
 ```
7. Update the formula in the property _Completion_ by inserting
  ```jsx
  + prop("Sum of weights in T3")
  ```
  after the _Sum of weights in T2_.

8. Finally, update the formula for _Overall Grade_ by inserting 
  ```jsx
  + prop("Weighted grade total in T3")
  ```
  after _Weighted grade total in T2_.
</details>
<details>
  <summary> How can I update the Grade Calculator with a new item? </summary>
</details>

<details>
  <summary> Some of my assignments have the same name (e.g. ‘Portfolio’), how can I tell which is the correct one in the Grade Calculator?</summary>
</details>

<details>
  <summary> I have an extension on an item, can I still enter the correct submission date? </summary>
</details>

<details>
  <summary> It seems like there is a lot of information to provide, are any of the assignment details optional?</summary>
</details>

<details>
  <summary> What if I don’t know how my items are weighted? Or, what if my items all count equally?</summary>
</details>
