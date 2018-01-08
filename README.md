# Sharing Items App

This android app allows users to share items with their contacts.

## User stories

As a user, I can:

* add, edit, and delete an item, its image, its description and its dimension.
* assign a contact to the item by switching item's status from available to borrowed.
* add, edit, and delete a contact, contact's name, and email address.

Note: User can't delete an contact that is an active user.

## Assignments

### Week 1 - Introduction to Software Design and Architecture

It was only quizes for week 1.

### Week 2 - Design Structure

In its current state, a user of the app—the owner—is able to record the items they own and wish to share.

The owner may view all of their items, their “Available” items, or their “Borrowed” items.

The owner may change the status of an item they own from “Available” to “Borrowed” and back.

When an item’s status is changed to “Borrowed”, the owner must enter the username of the borrower.

Review the user stories, then download, examine, and run the code base provided.

After you have become familiar with the code, construct a UML class diagram that captures all the classes and relationships in the code base. For each class you should document all attributes and methods.

These classes are:

* MainActivity
* SectionsPagerAdapter
* ItemsFragment
* AllItemsFragment
* AvailableItemsFragment
* BorrowedItemsFragment
* AddItemActivity
* EditItemActivity
* ItemList
* Item
* ItemAdapter
* Dimensions

You should also include any superclasses that the above classes inherit from. However, you are NOT required to document any methods or variables from these, only their names:

* AppCompatActivity
* FragmentPagerAdapter
* ArrayAdapter<\Item\>
* Fragment

**Style guidelines for UML class diagram**

* superclasses should be drawn above subclasses
* whole things should be drawn to the left of the part
* there should be few crossing edges
* boxes should not overlap other boxes or edges
* diagram should flow from top to bottom and left to right

<div style="text-align:center"><img src="#" alt="Design Structure"/></div>

### Week 3 - Modeling Behavior

#### 1.2 UML Sequence Diagram

Review the code responsible for adding a new item.

Make a sequence diagram that captures the interactions of objects in the app when a new item is added.

Your sequence diagram should contain the following classes:

* AddItemActivity
* ItemList
* Dimensions
* Item

And contain calls of the following methods:

* onCreate()
* loadItems()
* saveItem()
* Dimensions constructor
* Item constructor
* addItem()
* saveItems()

Lastly, the activation of AddItemActivity should start with the call to “onCreate()”

Hint: you may need to use nested activations.

<div style="text-align:center"><img src="#" alt="UML Sequence Diagram"/></div>

#### 1.3 UML State Diagram

Review the code responsible for adding a new item and editing an existing item.

Remember that an item can either be “Available” or “Borrowed” and can either have an image attached or not.

In this assignment you are to make a state diagram that captures the four possible states of an item.

* Available without photo
* Available with photo
* Borrowed without photo
* Borrowed with photo

Include arrows to indicate transitions between the states and label these transitions accordingly. And, remember to include the terminal state and to indicate the starting state.

<div style="text-align:center"><img src="#" alt="UML State diagram"/></div>

This is part 1 of the capstone project from the specialization Software Design and Architecture offered by University of Alberta on Coursera.

### Week 4 - Translate UML class diagrams to equivalent Java code.

This version of the app should accommodate the new contacts feature. In particular:

ContactsActivity should be accessible from the MainActivity.

ContactsActivity should be implemented as a ListView.

* An owner should now be able to add a potential borrower (a contact) to their contacts. Each contact must have a unique username and an email.

* An owner can edit or delete a contact, but not if the contact is currently borrowing an item, i.e. the contact is a borrower.

* Owners are now required to select a contact to be the borrower of an item when changing the status of an item from “Available” to “Borrowed”. That is, it is no longer sufficient to enter the borrower’s username as a string -- now the borrower must be picked from the owner’s list of contacts.

**Part 1 Submission** will test your ability to translate the UML class diagram into Java code. When you are ready to submit your code, include the following two files in a folder:

* Contact.java
* ContactList.java

Then compress the folder into a ZIP archive. Windows users can use 7zip or WinRAR. Upload it where prompted.


**Part 2 Submission** will test the correctness of your code

In order to grade your assignment, you will need to submit a 5 minutes or less demo video of your app that shows the following steps as a continuous interaction without crashing (if possible):

1. Start the video of your app from the MainActivity.
2. From the MainActivity, navigate to the ContactsActivity.
3. From the ContactsActivity, add a new contact to your contact list. Show that you can enter a username and email, save this contact to your contact list.
4. Show that by selecting (long clicking) a contact in the contact list, you can edit this contact. Update the email address of a contact.
5. Show that you can delete one of your contacts.
6. Go back to the MainActivity and look at your available Items.
7. Add an item to your inventory (if you don't already have an available item).
8. Edit an item in your inventory by long clicking on the item. Click the "Available" toggle. The toggle should now say "Borrowed" and a box should appear below to indicate the name of the borrower. By default the box will show the username of the first contact in your contacts. If you have more than one contact in your contacts you can click this box and then select the desired contact.
9. Finally, press "Save" to return to your inventory.

For this

The video of the app can be found [here](https://www.youtube.com/watch?v=c5QYnftN8k0)
