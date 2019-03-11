## Generating usernames

There are lots of websites and apps that use a username to identify you. This username is often visible to others. Usernames can also be called screen names, gamer tags, or handles. 

It’s important that your username isn’t your real name and also doesn’t include any personal information, such as your age, year of birth, or where you live. Other people will see your username, so make sure it’s polite, and consider what people will think about you when they read it. Remember that you might be using your username for a long time — will you still like it in three years? 

As you can see, it’s important to choose your username carefully. Let's create a Scratch project to generate 'AdjectiveNoun' usernames like 'DiamondIguana'. 

--- task ---

Open the Scratch [starter project](http://rpf.io/p/en/username-generator-scratch2-go){:target="_blank"} in the offline editor.

If you need to download and install the Scratch offline editor, you can find it at [rpf.io/scratchoff](http://rpf.io/scratchoff){:target="_blank"}.

You should see two lists on the stage — `adjectives` and `nouns`:

![lists with adjectices and nouns](images/usernames-lists.png)

--- /task ---

--- task ---

Click on **Data**, and then click the boxes next to `adjectives` and `nouns` to uncheck them and hide the lists.

![adjectives and nouns variables](images/usernames-hide.png)

--- /task ---

--- task ---

Add a variable called `username`.

[[[generic-scratch-add-variable]]]

--- /task ---

--- task ---

Click the box next to `username` to uncheck it and hide the variable from the stage.

![username variable](images/usernames-hide-variable.png)

--- /task ---

--- task ---

Add a person sprite — you can choose your favourite one. 

![a person sprite](images/usernames-person.png)

You can also click on **Costumes** and choose the costume you prefer.

--- /task ---

--- task ---

Add this code to your person sprite:

```blocks
when this sprite clicked
set [username v] to []
```

--- /task ---

--- task ---

You need to combine an adjective and a noun, so add a `join`{:class="blockoperators"} block inside your `set`{:class="blockdata"} block.

```blocks
when this sprite clicked
set [username v] to (join [hello] [world] :: +)
```

--- /task ---

--- task ---

Add a random adjective in the first box in the `join`{:class="blockoperators"} block.

```blocks
when this sprite clicked
set [username v] to (join (item (random v) of [adjectives v] :: +) [world])
```

--- /task ---

--- task ---

Add a random noun in the second box.

```blocks
when this sprite clicked
set [username v] to (join (item (random v) of [adjectives v]) (item (random v) of [adjectives v] :: +))
```

--- /task ---

--- task ---

Now add code blocks to get your person to say the username.

```blocks
when this sprite clicked
set [username v] to (join (item (random v) of [adjectives v]) (item (random v) of [adjectives v]))
+ say (username :: variables)
```

--- /task ---

--- task ---

Test your code by clicking on the person sprite. You should get a new random username each time. 

![person sprite saying Arctic Kestrel](images/usernames-click.png)

--- /task ---
