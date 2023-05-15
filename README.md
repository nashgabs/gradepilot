# Help and advice

## Adding new items

## FAQs

### What if I need to add an extra term?

**Warning: Some of the steps are quite involved. Please follow these steps carefully or the calculator may break.**

To create a new term:

1. In the side menu, select the three dots … beside the page titled **[Template](https://www.notion.so/cfc8966259324c4b908015c660f9602e)** and select “Duplicate” from the list. Then, rename it to something meaningful to you, e.g. “Term 3”.
2. Add your assignments to this term as you would usually. 

<aside>
💡***See the “Adding new items” section in this guide.***

</aside>

1. Open the page titled **[Grade Calculator](https://www.notion.so/6663b257af944700aa482a7078813f6d)**. To the right of the table headings select the plus symbol + and click on the property type “Relation”. Select the page you just created in Step 1 (e.g. “Term 3”) then click “Add relation” and “Done”.
2. Duplicate the property named “T2 selected modules” and rename it appropriately, e.g. “T3 selected modules”.
3. In the “Edit property” window select “Relation” and change this to the property you just created in Step 3, e.g. “Term 3”.
4. Duplicate the properties named “Sum of weights in T2” and “Weighted grade total in T3” following the same method shown in Steps 4 and 5. Rename these appropriately.
5. Duplicate the property named “Grade for T2”, rename appropriately and then update its formula with the newly created property names.

<aside>
💡 **The original formula should look like this.**

```jsx
round(prop("Weighted grade total in T2") * 1 / prop("Sum of weights in T2"))
```

**After editing, the formula should look something like this.**

```jsx
round(prop("Weighted grade total in T3") * 1 / prop("Sum of weights in T3"))
```

</aside>

### How can I update the Grade Calculator with a new item?

### Some of my assignments have the same name (e.g. ‘Portfolio’), how can I tell which is the correct one in the Grade Calculator?

### I have an extension on an item, can I still enter the correct submission date?

### It seems like there is a lot of information to provide, are any of the assignment details optional?

### What if I don’t know how my items are weighted? Or, what if my items all count equally?
