# Todo
I am Mathews Jacob, trying out an Android Todo
Conceptual Overview
Generate Second Screen - Generate a new UI screen (activity) that we will use for the edit screen. Let's generate a second activity to be used as an edit form for an item. Generate the second activity by selecting File => New => Activity => Blank Activity and go through the wizard to generate the blank activity. Give the activity a descriptive name i.e EditItemActivity
Layout Edit Form - Let's setup the view for the EditItemActivity by going to res/layout/activity_edit_item.xml. Here, using the graphical editor, we need to add a multi-line text field for the item body and a save button to submit the updated text value.
Support Edit Action - Within the main activity, setup a click listener such that when I click (rather than long-click) on any item, I am taken to the Edit form screen for that item. In the click listener for the items, you need to bring up the edit form activity using an "Intent" as explained in the CodePath cliffnotes. To properly load the form data, you should pass along the text and position of that item to the second activity using "extras" as explained in the guide.
Populate Edit Form - Now when the user clicks an item, it should bring up the Edit form activity and the item body should be passed along to that activity within the intent. Pull out the todo item's body from the extras as explained in the CodePath cliffnotes and set the form text field to contain the item's initial value. Be sure the user's cursor in the text field is at the end of the current text value and is in focus by default.
Send Back Result on Save - We need to hook up the edit form to send the result back to the initial activity after the "Save" button is clicked. Hook up a click handler on the "Save" button on the edit form and send back the todo item data to the list activity. Hint: Be sure to review each step of this section and call startActivityForResult initially to launch form and then later finish to return the result to the original activity.
Update Todo Item - In the original todolist activity, handle the submitted form's result from the edit form by inserting the updated todo text for the item at the correct position in the array and "notify" the adapter such that the todo list properly reflects the change. Hint: Make sure to persist the updated text back to the file with writeItems.
